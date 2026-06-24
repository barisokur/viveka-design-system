# Adapter — Stitch (Google Stitch UI generation)

Stitch generates UI from a natural-language prompt and lets you set a **theme** (primary color + font). Set the theme first, then paste a concise design brief into the prompt. Stitch responds best to short, concrete instructions — keep it tight.

## Step 1 — Theme settings (in Stitch's theme/customize panel)
- **Primary color:** `#00008B` (Viveka Navy)
- **Accent / secondary:** `#64C431` (Viveka Green) — use sparingly
- **Background:** `#FFFFFF` (white)
- **Font:** Lexend (headings) / Work Sans (body). If only one font is allowed, choose **Lexend**.
- **Corner radius:** small (4–8px)
- **Mode:** Light

## Step 2 — Paste this brief into the Stitch prompt (before/after your screen description)

```
Brand: Viveka — a corporate, clean, minimal, premium strategic-innovation consultancy. Executive tone, not playful.

Design rules:
- White (#FFFFFF) backgrounds only. No full-color, gradient, or photo backgrounds.
- Navy #00008B for all headings, titles, key numbers, and primary buttons.
- Green #64C431 as a tiny accent only (dots, active states, small highlights). Never a heading color or large fill.
- Light gray #F2F2F4 only for card surfaces, table rows, and dividers.
- Body text #1A1A2E; captions/labels #6B6B7B.
- Font: Lexend for headings, Work Sans for body.
- Flat design: no shadows, no gradients, hairline borders (#E0E0E8), 4–8px corner radius.
- Generous whitespace. Outline-style icons in navy or green.
```

## Step 3 — Then describe the screen
Append your actual request, e.g.:
> "...Design a dashboard with a top nav bar, a row of 3 stat cards, and a data table below."

## Logo (important — Stitch invents logos)
Stitch can't import our exact logo mid-generation, so tell it NOT to design one:
add *"top-left logo area: leave an empty 150×40px box labelled LOGO, do not design a logo"* to the prompt.
After export, replace that box with `<img src="viveka-logo.svg">` (or inline the SVG). Never ship a Stitch-generated logo. See [`assets/logos/USAGE.md`](../assets/logos/USAGE.md).

## Tips
- If Stitch drifts toward shadows/gradients or a colored hero, add: *"flat, no shadows, white background, navy headings only."*
- Stitch may not offer Work Sans — Lexend alone is an acceptable single-font fallback for the whole UI.
- Export Stitch output to code, then swap its inline colors for the `--viveka-*` variables from [`tokens/tokens.css`](../tokens/tokens.css) to lock in exact brand values.
