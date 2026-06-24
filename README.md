# Viveka Design System

> ## ⚠️ ÖNEMLİ — LOGO (önce bunu oku)
> **Logoyu asla AI'a çizdirme.** Claude/Stitch gibi araçlar tariften logo uydurur ve yanlış çıkar.
> **Pratikte en sık kullanacağın akış:** logo SVG dosyasını ([`assets/logos/viveka-logo.svg`](assets/logos/viveka-logo.svg) — navy; navy/foto zemin için [`viveka-logo-white.svg`](assets/logos/viveka-logo-white.svg)) sohbete **ekle** ve şunu de: **"Bu dosyayı aynen kullan, logoyu yeniden çizme."**
> PowerPoint / Slides / Word'de ise `Insert → Picture` ile dosyayı ekle — şekille çizme.
> Detaylı, araç-araç kılavuz: [`assets/logos/USAGE.md`](assets/logos/USAGE.md).

One brand, every output. A single source of truth (design tokens) feeds tool-specific "adapters" so Viveka looks identical whether it comes out of Claude, Google Stitch, an HTML page, a PDF, a PowerPoint deck, or Google Slides.

```
viveka-design-system/
├── README.md            ← you are here
├── 01-foundations.md    ← the brand "constitution": rules, do/don't, rationale
├── tokens/
│   ├── tokens.json      ← SOURCE OF TRUTH — colors, fonts, spacing, radius
│   └── tokens.css       ← the same values as CSS variables (--viveka-*)
├── adapters/            ← copy-paste briefs, one per tool
│   ├── claude.md        ← paste into a Claude prompt or Project
│   ├── stitch.md        ← theme settings + brief for Google Stitch
│   ├── pptx.md          ← PowerPoint master-template prompt (Avenir)
│   ├── google-slides.md ← Slides theme setup + AI brief (Lexend)
│   └── html-pdf/        ← working index.html + print.css starter
├── reference/
│   └── brand-reference.md  ← what the OFFICIAL sources actually say (verified)
└── assets/
    ├── logos/           ← link to the official Viveka logo files
    └── brand-guideline/ ← the official Logo Guideline, rendered page-by-page
```

> All brand values are **verified against the source assets**: navy `#00008B` and green `#64C431` were pixel-sampled from the logo; the palette and fonts (Avenir + Work Sans) match the official Logo Guideline. The official palette is just those colors + white; everything else is a documented extension. See [`reference/brand-reference.md`](reference/brand-reference.md).

## The core idea
Design decisions (navy is `#00008B`, headlines are bold, no shadows…) live in **one place**: `tokens/tokens.json`. Every adapter just references those decisions. Change a token once → regenerate/re-paste the adapters → the whole system stays consistent. No more re-deciding the brand per tool.

## How to use it, by tool

| You want to… | Open | Then |
|---|---|---|
| Generate HTML / React / SVG with **Claude** | `adapters/claude.md` | Paste the block into your prompt (or a Claude Project). Attach `tokens/tokens.css` for HTML. |
| Generate UI in **Stitch** | `adapters/stitch.md` | Set the theme colors/font, paste the brief, describe the screen. |
| Make a **PDF** or **web page** | `adapters/html-pdf/` | Open `index.html`, edit content, Print → Save as PDF. |
| Build a **PowerPoint** deck | `adapters/pptx.md` | Feed the prompt to a deck tool, or build the 8 masters by hand. |
| Build **Google Slides** | `adapters/google-slides.md` | Set the theme once, copy the master for each new deck. |

## Non-negotiables (the short version)
- **White background, always.** No full-color / gradient / photo canvases.
- **Navy `#00008B`** for all headlines & hierarchy.
- **Green `#64C431`** for tiny accents only (<10% of the view). Never a headline, never a big fill.
- **No shadows, no gradients.** Separation = borders + fills + whitespace.
- Fonts: **Avenir** (PowerPoint only) / **Lexend** (everywhere digital) for headlines; **Work Sans** for body.

Full rules and rationale: [`01-foundations.md`](01-foundations.md).

## Maintenance
Edit a value in `tokens/tokens.json` **and** mirror it in `tokens/tokens.css`, bump `$meta.version`, then re-paste the affected adapter. Keep this folder in version control (or shared drive) as the canonical brand reference — `v1.0.0`.
