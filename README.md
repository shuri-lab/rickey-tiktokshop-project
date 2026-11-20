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
