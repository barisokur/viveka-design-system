# Adapter — Google Slides

Google Slides has no native Avenir, so use the **digital** font stack: **Lexend** for titles, **Work Sans** for body (both available via Slides → Font → "More fonts"). Everything else matches the PPTX system.

## A. Set up the Theme (do this once per deck)
`Slide → Edit theme` (master view), then:
1. **Colors** (`Theme colors` dropdown → choose a slot → custom hex):
   - Text 1 / Dark 1: `#1A1A2E`
   - Background 1 / Light 1: `#FFFFFF`
   - Accent 1: `#00008B` (navy)
   - Accent 2: `#64C431` (green)
   - Accent 3: `#F2F2F4` (light gray)
   - Accent 4: `#6B6B7B` (muted)
2. **Fonts:** add Lexend and Work Sans via "More fonts". Set title placeholders to **Lexend Bold/ExtraBold, color navy**; body placeholders to **Work Sans, color #1A1A2E**.
3. Set every master layout background to **white**. Delete any default colored bands/shadows.

## B. Build the same 8 master layouts as PPTX
Cover · Section divider · 2-column content · Stat/data · Services grid · Quote · Timeline · Closing. (See [`pptx.md`](pptx.md) for the per-layout spec — use it verbatim, just swap Avenir → Lexend and apply sizes as pt.)

## C. If generating with AI (Gemini in Slides, or an export-to-Slides tool)
Paste this brief:

```
Create Google Slides for Viveka, a corporate/clean/minimal/premium strategic-innovation consultancy. Executive tone.
- Every slide background pure white (#FFFFFF). No full-color, gradient, or photo backgrounds.
- Navy #00008B for ALL titles, section headings, big numbers, table headers.
- Green #64C431 as tiny accents only (dots, dividers, icons). Never a title color or large fill (<10% weight).
- Light gray #F2F2F4 only for cards/table rows/dividers. Body text #1A1A2E, captions #6B6B7B.
- Fonts: Lexend (titles), Work Sans (body).
- Flat: no shadows, no gradients, hairline borders #E0E0E8, 8px rounded corners. Generous whitespace.
- Logo: navy "viveka" wordmark + green dot under the "i", navy-on-white, top-left or bottom-right.
- Tagline "Designs · Delivers · Executes"; contact meet@viveka.com.tr · viveka.com.tr.
```

## Logo
Never draw the logo. `Insert → Image → Upload from computer` → `assets/logos/viveka-logo.svg` (or `Viveka-Logo-PNG.png`); use `viveka-logo-white.svg` on navy. Place it on the master so every slide inherits it. See [`assets/logos/USAGE.md`](../assets/logos/USAGE.md).

## Tip
Save the finished deck as **"Viveka — Master Template"** and use `File → Make a copy` for every new deck so the theme stays locked.
