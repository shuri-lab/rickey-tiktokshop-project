# Rickey · Game Tape · TikTok Shop project

Everything for Rickey's TikTok Shop offers in one place: the live Offer 1 sales page, its images and source files, and all the project files (strategy, offer stack, deliverables, research, branding, videos).

## Offer 1 sales page: TikTok Shop Headstart ($27)

- **Live preview (GitHub Pages):** https://shuri-lab.github.io/rickey-tiktokshop-project/ (works once Pages is turned on: Settings → Pages → Branch `main`, folder `/ (root)`)
- **Page file:** `index.html` (one self-contained HTML file: all styles and scripts are inside it). It loads images from `images/`, fonts from Google Fonts, and the 5 TikTok videos from Cloudinary (`res.cloudinary.com/fje4fcoe`, a lighter 12-second, muted version via URL settings).
- **Built mobile first:** checked on iPhone 16 (393×852), 1280×800, 1440×900 and 1920×1080.

### What Offer 1 includes (final)
1. The 7-Day Headstart Course ($57 value)
2. The 30-Day First Sale Challenge, the 30-day plan ($47 value)
3. The Rickey Army Private Channel, a private WhatsApp channel ($97 value)

Total value $201, today $27. Order bump at checkout: The Starter Product List, $17. Guarantee: do the 30-day challenge, post every day, and if there's no sale within 90 days, full refund.

### How the buttons work (for the Stripe setup)
- Every "GET INSTANT ACCESS · $27" button jumps to the offer stack on the page (`#buy`).
- **Only one button goes to checkout:** the one inside the offer stack. Its link is currently the placeholder `PASTE-YOUR-CHECKOUT-LINK`. Search `index.html` for that text and replace it with the Stripe checkout URL.
- The $17 Starter Product List is shown on the page as "Add at checkout for $17", so it should be the order bump in the checkout.
- A sticky "Instant access · $27" bar appears on phones after the hero and hides while the offer stack is on screen.

### Still open
- Stripe checkout link, order bump and the one-click upsell (the upsell offer is in `project-files/Rickey-TikTokShop-Deliverables/Game Tape - Offer Stack-v11.pdf`).
- Footer disclaimers are drafts; the client needs to approve them.
- Images are full-size originals (some PNGs are ~2 MB). Compress them before sending paid traffic.
- `images/rickey-photo.jpg` looks like a cropped Getty Images photo: confirm the license before going live.
- FAQs to be added.

## Folders

| Folder | What's in it |
|---|---|
| `index.html` + `images/` | The Offer 1 sales page, ready to host |
| `offer-1-sales-page/` | Source files: `copy.md` (approved page copy), `copy-original.md` (first copy draft), `brand-kit.md` (colors and fonts), `learned-rules.md` (every client decision and rule so far), `image-prompts.md` (ChatGPT image prompts), `body-src.html` (page body source), `paste-ready.html` (version for a page builder's HTML block) |
| `project-files/` | All Rickey TikTok Shop project files: branding (Game Tape guidelines and logos), deliverables (course decks, challenge, product list, offer stack), research and transcripts, TikTok videos and screenshots, brand logos, and all page images |

## Brand
Game Tape: red `#D30805`, black `#101017`, white. Page fonts: Poppins (headings), Lato (body), Caveat (handwritten notes).

## GoHighLevel funnel (live, Nov 20 2026)

Funnel "Rickey · TikTok Shop Headstart" in the Hot Pursuit LLC sub-account, on davidhsai.com:

| Step | URL | How it's built |
|---|---|---|
| Sales page | /headstart-page | Custom Code loader → `offer-1-sales-page/ghl-sales-page.html` |
| Checkout | /headstart-checkout | Left: loader → `offer-1-sales-page/ghl-checkout-left.html`. Right: GHL order form, $27 + $17 bump checkbox |
| Upsell | /headstart-upsell | Loader → `offer-2-upsell/ghl-upsell.html` + native GHL YES button (one-click upsell, $97 product "Rickey · My $4M TikTok Shop System") + NO link to the thank-you page |
| Thank you | /headstart-thank-you | Loader → `offer-1-sales-page/ghl-thank-you.html` (links in `GT_LINKS` at the bottom) |

- **Course:** Memberships → "TikTok Shop Headstart" (Start here + Day 1 to Day 7, videos to upload). Login: the client portal.
- **Workflows:** "Rickey · Headstart delivery" (order with the $27 product → grant course → delivery email) and "Rickey · Starter Product List delivery" (order with the bump → download email).
- **Downloads:** `downloads/` (public for now; move to GHL Media before making the repo private).
- **Still to fill:** WhatsApp channel link (thank-you `GT_LINKS.whatsapp` + delivery email `WHATSAPP-LINK-GOES-HERE`), support email (`GT_LINKS.support`), course thumbnail and videos, sender name/email.

### Speed (Nov 20 update)
- Every page image is served as WebP at its display size from `images/opt/` (built by the image optimizer; originals stay in `images/`). Full-scroll image weight: ~1.2 MB on phones, ~1.5 MB on desktop (was ~15 MB).
- Carousel videos: Cloudinary `w_320,q_auto:eco,du_10,f_auto`, loaded only near the viewport; the loop duplicates reuse the cached file.
- The checkout's after-purchase setting is "Go to the next funnel step" (Checkout → Upsell → Thank You).
