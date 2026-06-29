# Estrateg[IA] — Design System

The brand system for **Estrateg[IA]**, Rosa Kethllyn's ecosystem of AI applied to strategy for healthcare management. It teaches managers (free YouTube), sells ready-made Claude skills, and builds custom agents.

The look is **editorial-technical**: a hot orange-red on near-black, giant Funnel Display headlines, JetBrains-Mono bracket labels `[ … ]`, and a strict rhythm of alternating **dark / light "dobras"** (folds). Energetic but disciplined — confident motion, never noisy.

---

## How to use this system

- **Stylesheet:** link `styles.css` (it `@import`s every token file). Then use the `--*` custom properties — never hard-code a hex that has a token.
- **Fonts:** loaded from Google Fonts in `tokens/fonts.css` (Funnel Display · Poppins · JetBrains Mono).
- **Assets:** in `assets/` (Rosa portrait duotone, natural portrait, hero poster). Reference brand specimens from the original PDF are in `assets/brand-spec-*.png`.
- **Specimens:** `guidelines/*.html` are live, self-contained cards (colors, type, spacing, brand mark, components, motion).

---

## 1. Brand essence

| | |
|---|---|
| **Who** | Rosa Kethllyn — founder, mentor ("[ Sua mentora ]"). |
| **For** | Managers of clinics, hospitals, labs, consultories, health networks; founders & coordinators. |
| **Promise** | Takes the health manager out of the operational and gives back time, strategic clarity, ready tools. |
| **Line** | *"A IA trabalha pra você, não o contrário."* |
| **Three layers** | `[ 01 ]` Canal (teach, free) · `[ 02 ]` Skills prontas (self-serve) · `[ 03 ]` Serviço sob medida. |

The **`[IA]` bracket** is the core motif. It recurs everywhere as a labelling device: `[ 01 ]`, `[ DOC.04 ]`, `[ SUA MENTORA ]`, `[ COMO FUNCIONA ]`.

---

## 2. Color

Orange-red is the **only** brand hue; everything else is a neutral (near-black or warm cream). Functional colors exist but are used sparingly — the brand stays dominant.

- **Brand:** `--brand` #E63B16 · `--brand-bright` #FF6A3D (on-dark links/accents) · `--brand-hover` #FF5A2C · gradient `--gradient-brand`.
- **Dark folds:** `--ink-900` … `--ink-card-2` (#070605 → #15110E).
- **Light folds:** `--paper` #F4F2EF · `--paper-warm` #EFECE7 · `--paper-card` #fff.
- **Text:** on-dark `--on-dark` / `--on-dark-muted` / `--on-dark-subtle`; on-light `--on-light` / `--on-light-body` / `--on-light-subtle`.

See `guidelines/color-*.html`.

### The dobra rule
Sections strictly alternate dark and light — **never two of the same background in a row.** Reference order on the site: hero (black) → manifesto (cream) → pillars (black) → features (cream) → journey (black) → service (cream) → products (black) → testimonials (cream) → about (black) → FAQ (cream) → final CTA (black).

---

## 3. Typography

- **Funnel Display** — display & headings. Weight 800, line-height ~.86, letter-spacing −.03em. Goes UPPERCASE and *huge* for the hero (`--type-hero`, up to 168px).
- **Poppins** — body & UI, 400/500/600.
- **JetBrains Mono** — bracket labels & technical micro-copy. UPPERCASE, wide tracking (`--track-mono` .22em).

Scale tokens in `tokens/typography.css`; specimen in `guidelines/typography.html`.

---

## 4. Spacing, radius, layout

Base-4 spacing. Sections breathe — vertical padding `--section-pad-y` clamp(56px,7vw,110px). Containers cap at `--container-max` 1280px (narrow 1040px). Radii: pill 999, card 18/22, sm 14, xs 12. See `guidelines/spacing.html`.

---

## 5. Components

| Component | File | Notes |
|---|---|---|
| Button | `guidelines/button.html` | Solid (brand + glow), Ghost (hairline), Text-link (mono, animated arrow). Magnetic hover. |
| Bracket label & badge | `guidelines/badge.html` | `[ … ]` labels, live-dot status pill, chips, "Mais procurado" hot badge. |
| Product card | `guidelines/product-card.html` | Dark card + featured variant (orange gradient, hot badge, lifts on hover). |
| Mentor card | `guidelines/mentor-card.html` | Signature portrait card: orange duotone, name + role lockup, `>>>`. 3D-tilts and opens a bio modal on click. |

---

## 6. Motion & interaction

Confident, slow easing (`--ease-out` cubic-bezier(.16,1,.3,1)). Patterns: scroll-reveal (rise 28px + fade, staggered), horizontal **marquees**, **magnetic** CTA hover, **3D tilt** portrait, **draggable** testimonial carousel (black dots, active stretches to brand), animated counters, blinking "VOCÊ ESTÁ AQUI". Respect `prefers-reduced-motion`. See `guidelines/motion.html`.

---

## 7. Voice & content

- **Portuguese (BR), direct, warm, anti-corporate.** Short sentences.
- **No em-dashes (`—`)** anywhere — they read as AI. Use commas, colons, or parentheses.
- Don't fabricate metrics. The channel is new ("inscreva-se e acompanhe"), so lead with the mission, not vanity numbers.
- Technical labels in brackets carry the "engineered" tone; keep them in mono uppercase.

---

## File index

```
styles.css                 → links all tokens
tokens/  fonts colors typography spacing effects (.css)
assets/  rosa-portrait.png  rosa-natural.png  hero-poster.jpg  brand-spec-*.png
guidelines/  color-brand color-dark color-light color-semantic
             typography spacing brand-mark
             button badge product-card mentor-card motion (.html)
```
