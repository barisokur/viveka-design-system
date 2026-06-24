# Adapter — OpenAI (ChatGPT) & Google Gemini

**You do NOT need a different design brief per AI vendor.** The Viveka rules (colors, fonts, layout, logo) are identical no matter which model writes the code. The brief below is the same one as [`claude.md`](claude.md) — it works verbatim in ChatGPT and Gemini. Only *how you load it* differs, plus one important caveat for **image generation** (§3).

---

## 1. The brief (same as Claude — paste this in)

```
You are designing for Viveka, a strategic innovation consultancy in Turkey. The look is corporate, clean, minimal, premium, executive — never playful or startup-casual. Follow this design system exactly.

THE ONE RULE: every background is pure white (#FFFFFF). No full-bleed navy/green/gray/gradient/photo backgrounds, ever. Color enters only via small shapes: cards, table headers, badges, dots, thin lines. Whitespace is the main layout tool.

COLORS
- Navy #00008B — PRIMARY: all headlines, titles, big stat numbers, table headers, thin borders, compact accent shapes.
- Green #64C431 — ACCENT ONLY: bullet/separator dots, dividers, icons, stat highlight lines, tags. Never a headline color, never a large fill. Keep under ~10% of visual weight.
- Light Gray #F2F2F4 — supporting fill for cards/table-rows/callouts only, never the canvas.
- White #FFFFFF — mandatory background.
- Ink #1A1A2E — body text. Muted #6B6B7B — captions/labels. Border #E0E0E8 — hairlines.

TYPOGRAPHY (web/digital)
- Headlines: Lexend (700–800), color navy. Body: Work Sans (400–600), color ink. Both via Google Fonts.
- Hierarchy from size + weight + whitespace, not decorative bars.

STYLE RULES
- Geometric only: rectangles, rounded rectangles (4–8px radius), circles.
- NO drop shadows, NO gradients, NO glows, NO texture. Separation = borders + fills + whitespace.
- Icons: outline or minimal-filled, navy or green.
- Max two text colors per view. Never white headlines.
- LOGO: never draw, redraw, or recreate the Viveka logo. It is a provided asset. Embed the exact file: viveka-logo.svg (navy, on light) or viveka-logo-white.svg (on navy/photo), via inline <svg> or <img src="viveka-logo.svg">. If no file is attached, leave a clearly-labelled empty logo placeholder — do NOT invent a logo.

BRAND
- Tagline: "Designs · Delivers · Executes" (green dots as separators).
- Contact: meet@viveka.com.tr · viveka.com.tr

When writing CSS/HTML, prefer CSS variables --viveka-navy, --viveka-green, etc. (see tokens.css) over hardcoded hex.
```

---

## 2. How to load it (chat / code generation)

### ChatGPT (OpenAI)
- **One-off:** paste the brief at the top of the chat, then describe the screen/asset.
- **Reusable → Custom GPT:** create a GPT, paste the brief into **Instructions**, and upload `viveka-logo.svg` + `tokens.css` to its **Knowledge**. Now the whole team gets a "Viveka Designer" GPT.
- **Canvas:** use it for HTML/React output, same as Claude artifacts.
- **Logo:** attach `viveka-logo.svg` to the message and say *"Use this exact file as the logo, do not recreate it."*

### Gemini (Google)
- **One-off:** paste the brief, then your request.
- **Reusable → Gem:** create a **Gem**, paste the brief into its instructions; attach the logo + tokens.
- **In Google Workspace:** Gemini in **Slides/Docs** can apply the brief, but the master theme set in [`google-slides.md`](google-slides.md) is more reliable — use both.
- **Logo:** upload `viveka-logo.svg` and instruct *"use as-is, never redraw."*

> Both accept file uploads, so the logo rule (embed the real file, never generate) works the same as Claude.

---

## 3. ⚠️ Image generation — different rules (DALL·E / GPT-4o images / Imagen / "Nano Banana")

Image generators **paint pixels**. They **cannot** place the exact logo or reproduce exact brand hex — they will approximate and get both wrong. So:

- **Never** generate a final asset that must contain the logo or exact brand colors.
- **Do** use image-gen only for *backgrounds, abstract visuals, illustrations, or photographic scenes* — then composite the **real logo (SVG)** and **exact colors** on top afterward (in Figma, Canva, PowerPoint, or HTML).
- If a layout needs the logo, generate the scene **without** any logo, then add `viveka-logo.svg` / `viveka-logo-white.svg` over it.
- You can mention the palette as *direction* ("navy #00008B and a green #64C431 accent on white"), but **verify the hex by hand** — assume the output drifted.
- Prefer **code-based** output (HTML/SVG) over image-gen whenever the result needs real text, real colors, or the logo — because code can use the exact tokens and embed the exact logo.

**Rule of thumb:** code generation = brand-exact (use it for UI, slides, docs, PDFs). Image generation = inspiration / backdrops only, never the finished branded asset.
