# Brand Reference — verified against source assets

This file records what the **official sources** actually say, so the tokens stay honest. Sources reviewed:
- `Viveka-Logo.png` (the logo artwork) — pixel-sampled.
- `VivekaInhouse-Communication-Branding-Logo-Usage-Guideline.pdf` — the official **Logo Guideline** deck, Nov 2023, 10 pages (rendered to [`../assets/brand-guideline/`](../assets/brand-guideline)).
- `[GUNCEL-2026]About-Viveka-Sales-Deck-Services.pptx` — the current 35-slide sales deck.

---

## 1. Colors — verified

Pixel-sampled directly from the logo artwork (dominant pixel value):
- **Navy `#00008B`** — 45,762 px. ✔ exact.
- **Green `#64C431`** — 1,155 px. ✔ exact.

The official guideline's "Color Palette" page lists **exactly three** brand colors plus white:

| Official | Hex |
|---|---|
| Green | `#64C431` |
| Navy | `#00008B` |
| Light Gray | `#F2F2F4` |
| (White) | `#FFFFFF` |

> Everything else in `tokens.json` (ink `#1A1A2E`, muted `#6B6B7B`, borders, tints) is a **deliberate extension** for readable documents/UI. They are not in the official guideline but are consistent with it. Keep them, but know they are ours, not canon.

## 2. Typography — verified
The guideline's "Typography" page shows **two official fonts**: **Avenir** and **Work Sans**. Both are sanctioned. So:
- Avenir is NOT a mistake — it is an official brand font (native/print use).
- In practice the sales deck is built almost entirely in **Work Sans** (Work Sans 1366 runs, + SemiBold/Light/Medium); Avenir does not appear in the deck file.
- Lexend is our addition for Word/digital where a single Google-Fonts family is wanted. Acceptable, but not in the official guideline.

## 3. Logo usage — from the guideline
- **Four approved lockups:** logo on light gray, on navy, on a photo, and on green. (So navy / photo / green backgrounds ARE allowed for the logo — see §5.)
- **Default** for documents & decks: navy wordmark + green dot on white.
- **Singular usage:** logo stands alone (stationery, social, solo appearances). Standard clear-space, size, and palette rules apply.
- **Partner usage:** logo shown beside a partner's logo (sponsorships, collaborations). Balance the two for equal visual weight; adjust clear space to avoid clutter. Neither logo should dominate.
- Never stretch, recolor, rotate, crop, or add effects.
- Contact for edge cases: meet@viveka.com.tr · viveka.com.tr.

## 4. Sales deck content inventory (reference for templates & adapters)
35 slides. Useful real content for placeholders and examples:
- **Headline stats:** 16 years · 150+ partners · 7,000+ startups · 280+ programs · 100+ experts · high PoC success rate.
- **Positioning:** "Designs · Delivers · Executes" — end-to-end innovation, leadership, sustainability programs.
- **Services:** Strategic Innovation Services · AI-Powered Innovation · Early-Stage Investment · Human Capital & Leadership Transformation · Access to Innovation & Technology.
- **AI layer:** Innovation Intelligence Layer — Strategy Design, Governance, Innovation Accounting, Corporate Memory & Competency.
- **Methodology:** Deep Analysis → Strategy & Governance → Strategy-Aligned Program Delivery → Fast Time-to-Value.
- **Programs / clients:** Anadolu Efes BrewFuture, Philip Morris Futuremark Startup Challenge, World Bank + Ministry of Industry & Technology, Enerjisa İVME, Kalyon PV Solar, Pasha Holding + IDDA, PAL Global, Colendi, AÇDAŞ/BEDAŞ/CEDAŞ DİNAMİK.

## 5. White-canvas rule — scope clarification (important)
The official guideline is a **logo** guideline; it does NOT mandate white backgrounds everywhere. Its own cover and closing pages use **navy** backgrounds, and the social-media samples use **photo/colored** backgrounds with the white/green logo.

So:
- **"Every background is white"** is a **template-level rule** chosen for executive **decks and documents** (per `Viveka_Design_Prompts_Final.md`) — it keeps long-form, client-facing material calm and premium. Keep it for PPTX / Word / PDF / reports.
- **Brand-level**, navy and photo backgrounds are legitimate for **covers, closing slides, social media, and event/launch graphics** — using the white or green logo lockups.

The adapters reflect this: deck/doc adapters enforce white; a future "social/marketing" adapter can use the navy/photo lockups.

## 6. Known drift to fix (when the deck is next revised)
The current sales deck has inconsistencies vs the official palette — standardize on revision:
- **Green:** appears as `#63C531` (149×), `#64C431` (24×), `#63C431` (14×). → standardize to **`#64C431`**.
- **Navy:** mostly `#00008B`, some `#00008A`/`#000089`. → standardize to **`#00008B`**.
- **Body text:** uses `#595959` (281×), `#404040`, `#666666` grays. → align to `#1A1A2E` (body) / `#6B6B7B` (captions), or formally adopt `#595959` as a token if preferred.
- Leftover **Arial / Calibri / Courier** runs from editing. → normalize to Work Sans / Avenir.
