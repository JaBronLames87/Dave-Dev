# Kinoke landing-page variants: shared build brief

Static HTML mockups of the three test variants Mitch asked for (app.kinoke.com/landing-page-1/2/3).
They are built as self-contained HTML first because the kinoke-frontend repo isn't reachable yet;
each will be ported to `apps/web/app/landing-page-N/page.tsx` once it is.

## Rules every variant follows (from Mitch's instructions)
- One self-contained HTML file per variant: `landing-page-N.html` in this folder. Images referenced
  relatively from `assets/`. Fonts from Google Fonts only. No JS libraries. Minimal inline JS only
  where a section truly needs it (e.g. feature tabs); the page must be complete without JS.
- Start each file with `<!doctype html>`, `<meta charset>`, `<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">`, its own `<title>`,
  a meta description, Open Graph tags (og:title, og:description, og:type, og:url), and
  `<meta name="robots" content="noindex, nofollow">` (mirrors `robots: { index:false, follow:false }`).
- Single-theme (each variant is its own brand world). Set every color explicitly on body.
- Mobile first. Must work at 375px with NO horizontal scroll, and at 1440px desktop. Side gutters >= 16px.
- Buttons/links (tag every one with its variant number N):
  - Primary "Get started" / sign up: `https://app.kinoke.com/login?from=landing-page-N` (becomes `/login?from=landing-page-N` in Next.js)
  - App Store: `https://apps.apple.com/app/id1644637937`
  - Google Play: `https://play.google.com/store/apps/details?id=com.scancafe.kinoke`
  - ScanCafe: `https://www.scancafe.com/` with `data-href="scanCafeLink()"` (in Next.js this must come from scanCafeLink() in @kinoke/shared/scancafe; never hand-write it)
  - Add `data-variant="landing-page-N"` and a `data-cta="<name>"` on every CTA so clicks can be compared.
- Logos are fixed brand assets: use `assets/logo-*.png`, never retype "kinoke" or "ScanCafe" as styled text in place of a logo. They are low-res (195px / 347px wide), so display kinoke at <= 120px wide and ScanCafe at <= 160px wide.
- Photos are small crops: photo-beach 227x200, photo-toddler 258x174, photo-wedding 376x188, photo-mountain 387x194, photo-family 732x438, hero-table 1277x1100, lilac-band 1277x560. Never display a photo larger than ~1.5x its pixel width or it will look soft. Use `loading="lazy"`, width/height attributes, and good alt text.
- Where a modern/contemporary family photo is needed and we have none, use a designed placeholder slot (tinted box, aspect-ratio set) with a small visible label like "Photo needed: toddler at the beach, 2024". Do not fake one.
- Hero video: a poster area with a play button and a caption "Watch the 90-second tour". It is a placeholder for Dave's new tour video (not playable in the mockup).
- Copy voice: plain, warm, specific, short sentences. No tracked-out ALL-CAPS eyebrow labels above every heading, no "→" on every link, no emoji, no lorem ipsum. Sentence case headings. Number steps only for the real 3-step process.
- Accessibility: visible focus states, contrast >= 4.5:1 for body text, semantic headings (one h1), `prefers-reduced-motion` respected.

## Content every variant must cover (from the 2026 tour-video script + Dave's PDF)
Order and emphasis may differ per variant, but all of this must appear:
1. Hero: headline, one-sentence subhead, ONE clearly primary CTA, App Store + Google Play as secondary, "Open on the web" as tertiary text link, trial line, tour video poster.
2. Trust: private by design (only people you invite see a Topic) / invite as many people as you like / never sold or shared, no ads.
3. How it works (the real 3-step sequence): Start a Topic -> Invite your people -> Keep it (book).
4. Features (from the app today):
   - Stories behind any photo by voice, video or text, in their own words
   - Ask questions; family can answer from anywhere
   - Comments and reactions ("like a family group chat, just for the moments that matter")
   - Kinoke suggests who's in each photo; tag anyone yourself; search by person
   - Turn a Topic into a short video set to music
   - Printed hardcover book (photo book or story book) made in the app; scan a page's QR code to hear the story in their own voice
   - Discover: learn more about the people you love, including stories you never thought to ask about
   - NEW: TV app slideshow. Put any Topic on the big screen during the holidays; only your curated favorites, nothing from the rest of your camera roll pops up.
   - Dates however you'd say them: "Summer 1985", "the 60s"
5. ScanCafe: "When your ScanCafe scans are ready, they show up in Kinoke automatically" (sign in with the same email as your order) + "Still have boxes at home? Digitize with ScanCafe" CTA.
6. Pricing: free 30-day trial, then $14.99/month or $149.99/year. Unlimited family members. Books sold separately. Keep the trial sentence in ONE element with `data-copy="trial-terms"` because the trial start rule is under discussion (may change to start when scans arrive, or 60 days).
7. FAQ: Who can see my photos? / How do my ScanCafe scans get into Kinoke? / Can I use Kinoke on a computer? (yes, at kinoke.com) / How does photo tagging handle my privacy? [Answer pending: Mitch] / How do I cancel, and what happens to my photos? [Answer pending]. Show pending answers as a visibly marked placeholder. Use native `<details>` for the accordion.
8. Closing CTA band + small footer (ScanCafe relationship line, privacy/terms links as "#").

## Variant-specific direction
See the "Direction" section for your variant in DIRECTIONS.md.
