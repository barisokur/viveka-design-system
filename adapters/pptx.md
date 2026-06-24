# Adapter — PowerPoint (.pptx)

Derived from [`tokens/tokens.json`](../tokens/tokens.json) + [`01-foundations.md`](../01-foundations.md). This is the office/native context — the **only** place Avenir is used (it is installed in PowerPoint on the Mac). Headlines = Avenir Black/Heavy, body = Work Sans.

Use this prompt with a deck-generating tool (Claude + the pptx skill, Gamma, etc.), or as the spec when building the master slides by hand.

> **Sync note:** colors/tagline/contact come from the tokens file. If a token changes, update the hex values below.

---

```text
Create a professional PPTX presentation template for Viveka, a strategic innovation consultancy based in Turkey. The template must feel corporate, clean, minimal, premium, and executive — suitable for strategic innovation consulting, corporate transformation, startup-corporate collaboration, policy work, and executive client communication.

CRITICAL DESIGN RULES
- Every slide background must be pure white (#FFFFFF). No full-slide navy, green, gray, beige, cream, gradient, or image backgrounds.
- All headlines, slide titles, section titles, and cover titles must be Navy Blue (#00008B).
- Navy (#00008B): headlines, section titles, large numbers, key labels, table headers, thin borders, compact accent shapes.
- Green (#64C431): small accent only — bullets, dots, icons, dividers, CTA details, data highlights. Max ~10% of a slide's visual weight.
- Light Gray (#F2F2F4): only inside cards, boxes, dividers, table rows. Never the full slide canvas.
- Use the navy logo on white. White logo only inside a small navy shape/badge. No white text unless inside a small navy shape, table header, or badge.

COLOR PALETTE
- Navy #00008B (primary) · Green #64C431 (accent) · Light Gray #F2F2F4 (fill) · White #FFFFFF (background) · Dark text #1A1A2E (body) · Secondary #6B6B7B (captions/labels)

TYPOGRAPHY
- Headline font: Avenir Heavy / Avenir Black — slide titles, cover title, section titles, large stat callouts.
- Body font: Work Sans Regular / SemiBold — body, captions, labels, bullets.
- Cover title: Avenir Black 48–56pt navy. Slide titles: Avenir Heavy 34–44pt navy. Section headers: 22–28pt navy. Stat callouts: Avenir Black 60–72pt navy. Body: Work Sans 14–16pt #1A1A2E. Captions: Work Sans 11–12pt #6B6B7B.

VISUAL LANGUAGE
- White is the dominant canvas; whitespace is the main layout tool. Navy for hierarchy, green for precise emphasis.
- No drop shadows, gradients, decorative flourishes, or texture. Shapes: rectangles, rounded rectangles (8px), circles only.
- No decorative bars under every title — use spacing and typographic hierarchy. Icons: outline or minimal-filled, navy or green.
- Margins 0.5" / 1.27cm. Left-align body. Max 5–7 lines of body text per slide.

BUILD THESE 8 MASTER LAYOUTS
1. TITLE/COVER — white bg; navy logo top-left w/ clear space; main headline navy Avenir Black 48–56pt; subtitle Work Sans 18–20pt; small green dot/line accent; client/date bottom-right 12pt #6B6B7B.
2. SECTION DIVIDER — white bg; large section number Avenir Black 80–100pt in #F2F2F4 or low-opacity navy outline; section title Avenir Heavy 40–44pt navy; optional 1–2 line descriptor; optional small green dot/line.
3. CONTENT (2-COLUMN) — white bg; left 55% title navy Avenir Heavy 32–36pt + body Work Sans 15pt; right 45% image/diagram/card placeholder (rounded 8px, #F2F2F4 fill); navy logo bottom-right small.
4. STAT/DATA — white bg; title navy Avenir Heavy 28–34pt; 2–3 horizontal stat cards (white/#F8F8FA fill, optional 1pt #E0E0E8 border); big number Avenir Black 60–72pt navy; label Work Sans 13pt #6B6B7B; optional 4–5px green line above number.
5. SERVICES/FEATURE GRID — white bg; title navy 32–36pt; 2x2 or 3x2 cards (#F8F8FA fill, #E0E0E8 border); small green dot/outline icon 20–24px; card header Work Sans SemiBold 15pt navy; description Work Sans 13pt #4A4A5A.
6. QUOTE/TESTIMONIAL — white bg; large decorative quotation mark in #F2F2F4 behind the quote; quote Work Sans Italic 18–22pt navy; name Work Sans SemiBold 14pt #1A1A2E; title/company 12pt #6B6B7B; navy logo bottom-right.
7. TIMELINE/PROCESS — white bg; title navy 32–36pt; horizontal 4–5 steps; numbered navy circles w/ white number Avenir Black 18pt; step title Work Sans SemiBold 14pt navy; one-liner 13pt #4A4A5A; green connector lines/arrows.
8. CLOSING/THANK YOU — white bg; navy logo centered large; thank-you headline navy Avenir Heavy 36–44pt; tagline "Designs · Delivers · Executes" Work Sans 18pt with green dot separators; contact "meet@viveka.com.tr | viveka.com.tr" 14pt #6B6B7B; optional thin green line above contact.

DON'T: full-color/gradient/photo slide backgrounds; white headlines on color; decorative ribbons/thick bars/colored stripes; >2 text colors per slide; green for large fills; stretching/recoloring the logo.
```
