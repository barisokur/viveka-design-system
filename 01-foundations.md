# Viveka Design System — Foundations (the "constitution")

This is the human-readable brand law. Every adapter (Claude, Stitch, HTML/PDF, PPTX, Slides) must obey it. The machine-readable equivalent lives in [`tokens/tokens.json`](tokens/tokens.json). Everything here is **verified against the official Logo Guideline and the logo artwork** — see [`reference/brand-reference.md`](reference/brand-reference.md).

Viveka is a strategic innovation consultancy based in Turkey. The visual system must feel **corporate, clean, minimal, premium, and executive** — never playful or startup-casual. Audience: corporate leadership, UNDP / World Bank, public agencies (İSTKA, ministries), and enterprise clients.

---

## 1. The rule that defines the document/deck system

**For executive decks and documents, the canvas is white.** Every slide and page background is pure white (`#FFFFFF`); color enters only through small shapes — cards, table headers, badges, dots, thin lines. White space is the primary layout tool. This keeps long-form, client-facing material calm and premium.

If you remember nothing else for decks/docs: **white canvas, navy for hierarchy, green for tiny accents.**

> **Scope note.** This white-canvas rule is a *template* decision for PPTX / Word / PDF / reports. At the **brand** level, navy and photo backgrounds are perfectly legitimate — the official guideline's own cover and closing pages are navy, and social-media graphics use photo/colored backgrounds with the white or green logo. So: white for documents & decks; navy/photo allowed for covers, closings, social, and event graphics. Don't let an adapter for one context leak its rule into another.

---

## 2. Color

| Token | Hex | What it is for |
|---|---|---|
| **Navy** | `#00008B` | Primary. All headlines, slide/page titles, section titles, big stat numbers, table headers, thin borders, compact accent shapes. |
| **Green** | `#64C431` | Accent **only**. Bullet/separator dots, dividers, icons, stat highlight lines, category tags. **Never** a headline color. **Never** a large background. Keep under ~10% of any view's visual weight. |
| **Light Gray** | `#F2F2F4` | Supporting fill. Card fills, table even-rows, callouts, subtle dividers. **Never** the full canvas. |
| **White** | `#FFFFFF` | The mandatory canvas. |
| Ink | `#1A1A2E` | Body text. |
| Ink Soft | `#4A4A5A` | Secondary body / card descriptions. |
| Muted | `#6B6B7B` | Captions, labels, dates, metadata, footnotes. |
| Border | `#E0E0E8` | Card hairline borders. |
| Border Soft | `#D0D0D8` | Table cell borders. |

> **Official vs extended.** The official guideline defines **only three** brand colors plus white: Navy `#00008B`, Green `#64C431`, Light Gray `#F2F2F4`. Both navy and green are pixel-verified against the logo artwork. Everything below the line (ink, ink-soft, muted, borders, tints) is **our deliberate extension** for readable documents and UI — consistent with the brand, but not in the official guideline.

Max two text colors per view. On a navy/photo cover use the white or green logo and white text — but in the white-canvas document system, headlines are always navy.

---

## 3. Typography

The official guideline names **two brand fonts: Avenir and Work Sans** (both sanctioned). Avenir is not available on the web or in AI tools — only in native PowerPoint on the Mac — so we use two stacks. (In practice the current sales deck is built almost entirely in Work Sans.)

| Role | Native / Office (PPTX) | Digital (Stitch, Claude, HTML, PDF, Slides) |
|---|---|---|
| Display / headlines | **Avenir Black / Heavy** | **Lexend** (700–800) |
| Body | **Work Sans** | **Work Sans** (400–600) |
| Word/.docx (special case) | — | **Lexend for everything** |

Both digital fonts are on Google Fonts. When a tool can't load a custom font, fall back to `system-ui, "Segoe UI", Arial, sans-serif`.

Hierarchy is created by **size + weight + space**, not by decorative bars under titles.

---

## 4. Visual language — do / don't

**Do**
- Keep every background white, including cover pages.
- Use navy for all main headlines and primary titles.
- Use green sparingly so it reads as intentional and premium.
- Use generous whitespace between sections.
- Geometric shapes only: rectangles, rounded rectangles (4–8px radius), circles.
- Outline-style or minimal-filled icons, in navy or green.
- Use the navy-on-white logo by default.

**Don't**
- No full-color / gradient / photo / texture backgrounds.
- No drop shadows, no glows, no gradients on text.
- No decorative ribbons, thick colored bars, or header/footer color stripes.
- No green headlines, no green large fills.
- No more than two text colors in one view.
- No clip art or generic stock icons.
- Never stretch, recolor, rotate, or crop the logo.

---

## 5. Logo

> **Never recreate the logo.** It is a fixed asset, not something to generate or describe-for-redraw. AI tools invent wrong logos from descriptions — always EMBED the real file. Vector: [`assets/logos/viveka-logo.svg`](assets/logos/viveka-logo.svg) (navy, default) and [`assets/logos/viveka-logo-white.svg`](assets/logos/viveka-logo-white.svg) (on navy/photo). Full per-tool instructions: [`assets/logos/USAGE.md`](assets/logos/USAGE.md).

Lowercase `viveka` wordmark in navy with a small green dot below the "i". Place with generous clear space; never stretch, recolor, rotate, crop, or add effects.

**Four approved lockups** (from the guideline): logo on **light gray**, on **navy**, on a **photo**, and on **green**.
- **Documents & decks default:** navy wordmark + green dot on **white**.
- **Navy background:** use the white logo. **Green/photo background:** use the white logo (keep the green dot legible).

**Usage modes:**
- **Singular** — logo stands alone (stationery, social, solo appearances). Standard clear-space / size / palette rules apply.
- **Partner** — logo beside a partner's logo (sponsorships, collaborations). Balance both for equal visual weight; neither dominates; increase clear space to avoid clutter.

Files: see [`assets/logos/`](assets/logos). The official guideline pages are in [`assets/brand-guideline/`](assets/brand-guideline).

---

## 6. Brand constants

- Tagline: **Designs · Delivers · Executes** (green dots as separators).
- Contact: **meet@viveka.com.tr · viveka.com.tr**

---

## 7. How to change the brand

1. Edit the value in [`tokens/tokens.json`](tokens/tokens.json) (and mirror in `tokens/tokens.css`).
2. The CSS-based outputs (HTML, PDF, Claude/Stitch HTML artifacts) update automatically via the variables.
3. Re-paste the affected adapter into the AI tool, or bump the hex in the office templates.
4. Bump `$meta.version` in `tokens.json`.
