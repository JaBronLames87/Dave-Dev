# Three directions, three hypotheses

The two axes Anderson named in the Nov 24 call are TYPE (grown-up vs playful) and COLOR (warm/ScanCafe-adjacent vs a new shared purple system). The third axis is CO-BRANDING (how ScanCafe and Kinoke sit together). Each variant takes a different position on all three, so the test spans the range. Each page differs in everything, so a winner tells you which overall direction resonates, not which single element did it. Follow-up tests isolate elements.

| | 1. Heirloom | 2. Kitchen Table | 3. Movie Night |
|---|---|---|---|
| Hypothesis | A grown-up, nostalgic page converts scanning customers best | Warm colors + a playful typeface keep the fun without looking childish, so it reaches both "mom" and "college-age niece" | One shared purple brand family makes ScanCafe -> Kinoke feel seamless and positions Kinoke for the wider market |
| Primary reader | ScanCafe customer, 50-75 | Parents of young kids + their parents | 20-40, broader market beyond scanning |
| Type | Grown-up serif + clean sans | Soft, chunky playful serif + friendly sans + handwriting for captions | Wide, confident grotesk + clean sans + mono for slide labels |
| Color | Plum on cream (Dave's v1) | Berry plum, marigold, apricot, cream | Deep aubergine (ScanCafe concept) + bright violet (Kinoke) on dark |
| Co-brand | "ScanCafe x Kinoke" lockup | "Kinoke, from the family behind ScanCafe" | "Kinoke, a ScanCafe company" + concept recolor of ScanCafe logo in purple |
| Headline | Your family's photos, with the stories that go with them. | The family group chat for the photos that matter. | Not for everyone. Just for your people. |

## Direction: landing-page-1 "Heirloom" (control; refined version of Dave's PDF)
- Stays close to Dave's PDF so it serves as the control, but fixes its problems: removes the all-caps eyebrow labels; ONE primary CTA in the hero instead of three equal purple buttons; fixes the broken step-3 image (half black in the PDF); adds the missing features (questions, video set to music, AI people suggestions, Discover, TV slideshow); fills the trust content.
- Fonts: "Libre Baskerville" (display, 400/700 + italic) + "DM Sans" (body 400/500/700). (Matches the PDF.)
- Colors: plum #4A2A4F (headings/primary buttons), plum-deep #3A2140 (closing band), cream #FBF6F0 (page), sand #F3ECE2 (alt sections), rose-tan #9C5F45 (small accents, italic trial line), ink #2E2630, ink-soft #6B6170, line #E6DCD0, card #FFFCF8.
- Imagery: hero-table.webp as the hero (it is the video poster; add a play button over the phone and a "Watch the 90-second tour" caption card), photo-family for step 1, vintage prints for features. Two-column hero on desktop (copy left, image right, image bleeds to the right edge), stacked on mobile (image first, then copy).
- Feature section: tabbed (Topics / Stories / Questions / People / Books / TV) like the PDF, but tabs must work with no JS (use radio inputs + :checked CSS, or show all panels stacked on mobile). Each panel: short copy + a simple illustrative "app card" built in HTML/CSS in the page's own palette (not a screenshot of the current bright app UI).
- Tone: calm, warm, unhurried.

## Direction: landing-page-2 "Kitchen Table" (Anderson's hybrid: warm color + playful type)
- Idea: the page looks like photos spread on the kitchen table during the holidays, with family talking over them. Scrapbook energy, but tidy and adult.
- Fonts: "Fraunces" with SOFT=100 and WONK=1 at weight 700-800 for display (it is ScanCafe's heading face, so it bridges the brands, but the soft/wonky axes make it playful); "Figtree" for body (400/500/700); "Caveat" (500/600) ONLY for handwritten photo captions written "on the back of the print" (e.g. "Lake house, summer '85"). Load Fraunces with the SOFT and WONK axes: `family=Fraunces:opsz,wght,SOFT,WONK@9..144,400..900,0..100,0..1`.
- Colors: berry #7A2E6B (primary), berry-deep #4E1C45, marigold #F2A93B (highlight, stickers), apricot #F9DDBF (section fill), cream #FFF8EE (page), sage #7E9C83 (small accents), ink #2A1A28, ink-soft #6A5A66, white-warm #FFFDF8.
- Layout ideas: hero with a cluster of slightly rotated vintage prints (CSS rotate, white borders, soft shadow) with Caveat captions, plus a chat-bubble thread overlapping them showing a real Topic conversation: Grandma: "That's your great-uncle Leo, he built that boat himself." / Maya (college): "WAIT he built it??" / Dad: "Summer '85. I was 9." with small reaction chips. Use the conversation as the proof of "group chat for the photos that matter".
- Must show BOTH generations: grandma's 70s slides AND a young family's toddler videos (use labeled placeholder slots for modern photos).
- Big section for the TV slideshow: "Put it on the TV this Thanksgiving." A simple CSS TV frame cycling through the vintage prints (CSS-only keyframe crossfade, disabled under prefers-reduced-motion; static first frame visible at rest). Copy point: only the favorites your family chose, so nothing unexpected from your camera roll shows up on the big screen.
- Sticker-like rounded pills (marigold) for small facts: "Unlimited family", "No ads, ever", "Works on any phone".
- Tone: warm, a little funny, conversational. Never cutesy.

## Direction: landing-page-3 "Movie Night" (Anderson's rebrand thought experiment: one purple family)
- Idea: "Kino" means cinema. The page is a dark living room with family photos playing on the big screen like a slideshow. It leans into the TV app and the "video set to music" feature and speaks to a younger, broader audience: the space between public feeds (Instagram/Facebook) and disappearing messages (Snapchat). Stuff you don't want everyone to see but do want to remember.
- Shows the rebrand concept: a deep aubergine for ScanCafe and a brighter violet for Kinoke, side by side. Use `assets/logo-scancafe-purple-concept-light.png` (on dark) and `logo-kinoke-light.png`. Label the recolored ScanCafe logo somewhere unobtrusive as "Concept color" so no one mistakes it for an approved logo.
- Fonts: "Archivo" using its width axis, expanded (wdth 112-125) at 700-800 for display headlines; "Instrument Sans" (400/500/600) for body; "IBM Plex Mono" (400/500) for slide labels and small metadata, styled like slide-mount stamps: "SLIDE 014 · SUMMER 1978". Load Archivo with `family=Archivo:wdth,wght@62..125,400..800`.
- Colors (dark-first, single theme): night #140D22 (page), aubergine #2A1B4A (ScanCafe concept / raised sections), plum-panel #1E1433 (cards), violet #A47BFF (Kinoke accent, primary buttons with dark text #140D22), violet-soft #C9B3FF, glow #FFD9A8 (warm projector light, used sparingly for highlights), text #F4EFFF, text-soft #B8ADCF, line #3A2C5C. No purple-to-blue gradient hero on white.
- Layout ideas: hero = a big "screen" (aspect 16:9) showing a vintage print (hero-table or photo-family) with a subtle warm glow around it as if lit by a projector/TV, slide label in mono beneath, headline beside/above. A horizontal "film strip" row of prints with mono labels. Section contrasting three apps: "Public feeds: everyone sees it" / "Disappearing apps: no one remembers it" / "Kinoke: your people see it, and it stays". Feature grid with the TV slideshow and "short video set to music" first.
- Tone: confident, a bit cheeky, short sentences. Still kind; no snark about other platforms by name in headlines (naming Meta/Instagram in body copy is fine sparingly).
