# Urban Room — Design System

> **DEVELOP WITH CONFIDENCE.**
> Urban Room Co., Ltd. — Khon Kaen, Thailand. An urban-content & real-estate development practice. English-only first version.

---

## About Urban Room

**Urban Room Co., Ltd.** is an urban content services and real-estate development firm based in Khon Kaen, Thailand. The studio works as a **multidisciplinary partnership** — pulling in urban planners (3DOT DESIGN), architects (Z56), and other specialists per project — to support city-scale visions, master plans, and feasibility for public and private clients.

### Services
1. **Urban Study and City Branding** — research that informs policy decisions and estate-development visions.
2. **Master Planning** — design for building groups and large real-estate projects, including architectural detail and participation processes.
3. **Feasibility and Market Study** — financial analysis: FIRR, EIRR, SROI for investor decision-making.

### Project archive (11)
Pocket Park · ISAN Showcase (Isan Creative Festival 2023) · School Yard Lunch · Ban Ped – Safe Road · Sukhothai Learning Center · Khon Kaen Innovation District · Peafowl Learning Center · Walkable Kangsadan · Phetchabun City · Lam Luk Ka City · Eco Innovation Park.

### Contact
Urban Room Co., Ltd. · 92/18 Mittrapap Rd., Nai Mueang, Mueang Khon Kaen, Khon Kaen 40000 · `info@urbanroom.org` · YouTube `@Urbanroom2023` · Facebook `urbanroomth` · Instagram `urbanroomstudio` · © 2020.

---

## Index

| File / folder | Purpose |
|---|---|
| `README.md` | This file. |
| `SKILL.md` | Agent skill definition. |
| `colors_and_type.css` | Tokens — color, type, spacing, motion, shadow. |
| `site-data.json` | Canonical content. |
| `assets/` | Logo SVG family: `mark`, `horizontal`, `stacked`, `wordmark`, and `urbanroom-logo` (alias of mark). |
| `preview/` | Design-system specimen cards. |
| `ui_kits/website/` | Marketing site, recreated. |
| `CI Exploration/` | The CI exploration that led here. |

---

## The mark — INTERLOCK

A **square** (architecture, the built room) meets a **circle** (the public realm, the urban). Their **intersection is filled solid** — the "urban room", the space where the firm operates. Two pure geometric primitives, no decoration.

### Lockup family (`assets/`)
| File | Use |
|---|---|
| `urbanroom-mark.svg` (= `urbanroom-logo.svg`) | Mark only. Default for favicons, social avatars, small badges. |
| `urbanroom-horizontal.svg` | Mark + URBAN ROOM stacked to the right. Use for nav bars, signatures. |
| `urbanroom-stacked.svg` | Mark above wordmark. Use for hero / large signage / merchandise. |
| `urbanroom-wordmark.svg` | Wordmark only — URBAN / ROOM stacked. Use when mark and wordmark are separated. |

### Rules
- **Minimum size:** mark 16px wide, horizontal lockup 96px wide, stacked lockup 60px wide.
- **Clear space:** at least ½ mark height around the lockup on all sides.
- **Color:** ink on paper (default); paper on ink (reverse); paper on clay (reverse on accent). Never accent on paper, never tinted strokes, never gradient fills.
- **Strokes scale:** stroke weight is 8 in the 200-viewBox (4% of width). At smaller sizes use 6, 4, 2.5, 1.5 for 64 / 40 / 24 / 16px.

---

## Content fundamentals

Urban Room's voice is **plain, infrastructural, and confident**. The voice of a firm presenting a master plan to a mayor.

- **English only**, US/UK neutral spelling. No Thai script in v1 copy. Place names stay as proper nouns.
- **Sentence case** for headings; **ALL CAPS with wide tracking (≈0.18em)** for tagline and eyebrows only.
- **The tagline is sacrosanct:** `DEVELOP WITH CONFIDENCE.` — full caps, period, the period is clay-accent.
- **First-person plural ("we") for the firm; second person ("you") for clients.** Never "I".
- **Specifics over adjectives.** "Khon Kaen Innovation District" beats "a major hub".
- **Acronyms spelled on first use:** FIRR (Financial Internal Rate of Return), EIRR (Economic IRR), SROI (Social Return on Investment).
- **No exclamation marks. No emoji.**

### Vibe in three words
**Architectural. Civic. Plain-spoken.**

---

## Visual foundations

### Palette — sand · ink · clay
| Token | Hex | Use |
|---|---|---|
| `--ur-bg` (paper) | `#F2EDE3` | page surface |
| `--ur-bg-soft` | `#ECE5D6` | card / inset |
| `--ur-bg-muted` | `#E3DAC6` | section band |
| `--ur-bg-bright` | `#FAF6EC` | lifted highlight |
| `--ur-ink` (ink) | `#1B1A17` | primary text, mark |
| `--ur-ink-3` | `#6B6359` | secondary text |
| `--ur-accent` (clay) | `#C2563A` | accent — sparingly |
| `--ur-accent-deep` | `#9A3F26` | accent hover / error |
| `--ur-accent-soft` | `#E8B8A6` | accent tint backgrounds |

A warm sand surface carries a deep warm-black ink. The single clay accent appears no more than once per screen — typically the period after a key sentence (`confidence.`), the active arrow on a CTA, or the underline on the active nav link.

### Typography — Manrope
- **Display & UI** — *Manrope* 400 / 500 / 600 / 700 / 800. A modern geometric humanist sans. Use 700/800 at display sizes with tracking `-0.05em`; 400/500 at body sizes.
- **Mono** — *JetBrains Mono* for FIRR/EIRR figures, project codes, technical captions.
- **No Thai script in v1.** Manrope handles Thai if v2 reintroduces it.

### Spacing & rhythm
**8-point grid**, 4pt half-step. Section vertical air: 64–144px. Layout caps at 1240px. Generous whitespace is on-brand.

### Surfaces
- Default: flat sand (`--ur-bg`).
- Inset sections: `--ur-bg-soft` or `--ur-bg-muted`.
- Imagery: full-bleed; never decoratively cropped.
- **No gradients** except a black 0→40% bottom scrim over imagery to seat caption text.

### Imagery direction
Real Thai urban + civic photography — markets, streets, plazas, walkable infrastructure. Warm-neutral grading. People at scale, in context.

### Corner radii
- **0px** — image containers, major plates.
- **2–4px** — buttons, inputs.
- **8px** — soft cards (data tiles, partner chips).
- **Pill (999px)** — filter chips, status pills.

### Shadows
`--ur-shadow-1` (1px hairline lift) is the default. `--ur-shadow-2` for floating CTAs. Rarely needed.

### Motion
- Easing: `cubic-bezier(0.16, 1, 0.3, 1)` entrances, `cubic-bezier(0.22, 0.61, 0.36, 1)` in-out.
- Durations: 120ms / 220ms / 420ms / 800ms.
- Fade-and-rise for entrances. No parallax, no bounces, no Lottie.

### Layout rules
- 12-column grid, 32px gutter, 1240px cap.
- Asymmetric splits welcome (7/5, 8/4).
- One accent element per screen.

---

## Iconography

Low-icon brand. Where icons are needed, use thin geometric line icons — Lucide via CDN, 1.5px stroke, 24px artboard. Ink only. Sizes 16 / 20 / 24 / 32 px. No emoji.

---

## Open questions / asks

- [ ] **Photography** — 6–10 representative project images (Pocket Park, Khon Kaen Innovation District, Walkable Kangsadan first). Currently using tonal placeholders.
- [x] **Logo** — Interlock SVG family delivered.
- [x] **Fonts** — Manrope (display + UI) + JetBrains Mono (mono), via Google Fonts.
- [x] **Accent** — clay `#C2563A`, used sparingly.
