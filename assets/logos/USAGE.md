# Logo usage — READ THIS FIRST

**The #1 rule: never let an AI tool draw, redraw, "recreate," or approximate the Viveka logo. The logo is a fixed asset — you always EMBED the real file, never generate it.**

AI tools (Claude, Stitch, Midjourney, etc.) will happily invent a wrong logo from a text description. So we never describe it for re-creation — we hand them the actual file.

## The official files (use these, nothing else)
| File | Use on |
|---|---|
| [`viveka-logo.svg`](viveka-logo.svg) | white / light backgrounds (DEFAULT) — navy wordmark + green dot |
| [`viveka-logo-white.svg`](viveka-logo-white.svg) | navy / photo / green backgrounds — white wordmark + green dot |
| `Viveka-Logo-PNG.png` | when a tool needs a raster (PNG) instead of SVG |
| `Viveka-Logo-White-Background.png` / `...Blue-Background.png` / `...Green-Background.png` | pre-made lockups |

SVG is preferred everywhere it's accepted — it's vector, stays crisp at any size, and carries the exact brand colors (`#00008B`, `#64C431`).

---

## How to embed, per tool

### Claude (HTML / React / artifacts)
Two reliable ways — **do NOT** ask Claude to "make a viveka logo":
1. **Attach the SVG file to the chat** and say: *"Use this exact file as the logo. Embed it as-is — do not redraw or modify it."*
2. **Inline the SVG**: open `viveka-logo.svg`, copy its entire `<svg>…</svg>`, paste it directly into the HTML. Or reference it: `<img src="viveka-logo.svg" alt="Viveka" width="150">`.

> Tip: tell Claude *"The logo is a provided asset, never generated"* in the prompt. The Claude adapter already says this.

### Stitch
Stitch generates mockups and **cannot import our exact SVG** mid-generation. So:
1. In the prompt, use a **placeholder**: *"top-left logo area — leave an empty 150×40px box labelled LOGO, do not design a logo."*
2. After exporting Stitch's code, **replace the placeholder** with `<img src="viveka-logo.svg">` (or the inline SVG).
3. If your Stitch version supports image upload, upload `Viveka-Logo-PNG.png` and place it — still don't let it auto-generate one.

### PowerPoint / Google Slides / Word
Never draw the logo with shapes/text. Always **Insert → Picture → From file** and pick `viveka-logo.svg` (PowerPoint & Slides accept SVG) or `Viveka-Logo-PNG.png`. Put it on the slide master so every slide inherits the real logo.

### PDF (from the HTML starter)
Already handled — `adapters/html-pdf/index.html` embeds `viveka-logo.svg` via `<img>`. Just edit content; the real logo carries through to the PDF.

---

## Placement & integrity rules (from the brand guideline)
- Default position: top-left or bottom-right, with generous clear space around it.
- Pick the version that matches the background: navy logo on light, white logo on dark/photo.
- **Never** stretch, squish, rotate, crop, recolor, add shadows/outlines, or place on a busy/low-contrast area.
- Keep proportions locked (scale width & height together).
