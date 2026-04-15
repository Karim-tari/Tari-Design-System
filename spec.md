# Tari Design System

## 1. Visual Theme & Atmosphere

Tari's visual language is rooted in restraint. Every decision starts by asking what can be removed — decoration is earned, not assumed. The result is an interface that feels premium through discipline: precise spacing, confident type, and surfaces that let content breathe rather than compete for attention.

The foundational dark surface is `#0c0718` — a deep aubergine-black that reads darker than true black while retaining warmth. Against this, `#c9eb00` lime delivers sharp, almost neon contrast used sparingly as a single dominant accent. The palette is intentionally narrow: fewer colors, used more deliberately.

The type system reflects the same restraint. Druk appears only at display scale — commanding, uppercase, never decorative. Poppins carries everything else: body, labels, UI — clean and legible at every weight. Together they create a hierarchy that is expressive at the top and precise at the detail level, without noise in between.

Interactions are understated. Hover states lift by 2px. Transitions run at 150–250ms. Motion clarifies — it never entertains. Components feel physical and responsive without being animated for effect.

**Core Design Principles:**
- **Minimal first.** Every element must earn its place. If it doesn't serve the content or guide the user, remove it.
- **Clean over clever.** Prefer a well-spaced neutral surface over decorative fills, tinted backgrounds, or accent-heavy UI.
- **Hierarchy through restraint.** Use one strong accent (`#c9eb00`), one primary action style, and let everything else recede.
- **Space is the design.** Generous whitespace and consistent rhythm communicate quality more than any embellishment.
- **Subtle by default, expressive when needed.** UI chrome should be invisible. Druk, lime, and gradient are reserved for moments that matter.

**Key Characteristics:**
- Deep aubergine-black (`#0c0718`) as the foundational dark background — warmer than true black
- Warm cream (`#fbf7ef`) as the light-mode base — never pure white
- `#c9eb00` lime as the single dominant accent — used sparingly for highlights, CTAs, and active states
- Druk display font for hero headlines only — bold, uppercase, large, commanding; never decorative
- Poppins for all body, UI, and supporting text — geometric, approachable, always legible
- 50–70px border-radius on buttons — signature rounded pill aesthetic
- Blue-purple gradient for primary CTAs only — `linear-gradient(90deg, #5a63d3, #3342ff)`
- Cards with `border-radius: 16px`, soft shadow, and neutral border — no colored fills
- Secondary buttons as solid surface cards — neutral background, standard border, no color
- Form inputs as underline-only — no box, no background, lime sweep animates on focus

---

## 2. Color Palette & Roles

### Core Brand

| Token | Value | Role |
|-------|-------|------|
| `--tari-dark` | `#0c0718` | Primary dark background — deep aubergine |
| `--tari-cream` | `#fbf7ef` | Primary light background — warm cream |
| `--tari-lime` | `#c9eb00` | Primary accent — electric lime |
| `--tari-green` | `#71ee73` | Secondary accent — bright green |
| `--tari-orange` | `#ffab25` | Highlight / warning color |
| `--tari-blue` | `#3342ff` | Gradient endpoint — deep blue |
| `--tari-purple` | `#5a63d3` | Gradient start — soft purple |

### Gradient
```
--tari-gradient: linear-gradient(90deg, #5a63d3, #3342ff);
```
Used **exclusively** on primary buttons and hero CTAs. Do not apply to secondary elements.

### Neutral Scale

| Token | Value | Role |
|-------|-------|------|
| `--neutral-950` | `#0c0718` | Darkest surface |
| `--neutral-900` | `#130f22` | Secondary dark surface |
| `--neutral-800` | `#1e1836` | Elevated dark card |
| `--neutral-700` | `#2e2850` | Tertiary dark |
| `--neutral-500` | `#706a90` | Muted text on dark |
| `--neutral-400` | `#9993b0` | Placeholder / disabled |
| `--neutral-200` | `#d4cfea` | Borders on dark |
| `--neutral-100` | `#ece9f5` | Subtle surface tint |
| `--neutral-50` | `#f6f4fb` | Near-white surface |

### Semantic Roles

| Role | Dark Mode | Light Mode |
|------|-----------|------------|
| Background | `#0c0718` | `#fbf7ef` |
| Surface | `#130f22` | `#ffffff` |
| Surface raised | `#1e1836` | `#f6f4fb` |
| Text primary | `#fbf7ef` | `#0c0718` |
| Text secondary | `#9993b0` | `#706a90` |
| Text muted | `#706a90` | `#9993b0` |
| Border | `#2e2850` | `#d4cfea` |
| Accent | `#c9eb00` | `#c9eb00` |
| Accent hover | `#b8d600` | `#b8d600` |

### Status Colors

| State | Color | Hex |
|-------|-------|-----|
| Success | Bright green | `#71ee73` |
| Warning | Orange | `#ffab25` |
| Error | Red | `#ff4545` |
| Info | Blue | `#3342ff` |

---

## 3. Typography Rules

### Font Families

- **Display:** `'DrukWideFont', 'Druk Wide', 'Druk', Arial, sans-serif` — uppercase only, large sizes, maximum weight. Never use below 40px.
- **Primary:** `'Poppins', system-ui, -apple-system, sans-serif` — all UI text, body copy, labels, headings under 40px
- **Monospace:** `'JetBrains Mono', monospace` — code, technical strings, token values

### Type Scale

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display XL | Druk Wide | 120px | 800 | 0.9 | -2px | Hero headlines, uppercase only |
| Display L | Druk Wide | 80px | 800 | 0.92 | -1px | Section heroes, uppercase only |
| Display M | Druk Wide | 56px | 700 | 0.95 | -0.5px | Sub-hero, uppercase only |
| Heading 1 | Poppins | 48px | 700 | 1.1 | -0.5px | Section titles |
| Heading 2 | Poppins | 36px | 700 | 1.15 | -0.3px | Card titles, sub-sections |
| Heading 3 | Poppins | 24px | 600 | 1.25 | -0.25px | Feature headers |
| Heading 4 | Poppins | 20px | 600 | 1.30 | 0 | List headers, callouts |
| Body L | Poppins | 17px | 500 | 1.55 | -0.3px | Intro paragraphs |
| Body | Poppins | 15px | 400 | 1.45 | -0.25px | Default body text |
| Body S | Poppins | 13px | 400 | 1.5 | 0 | Supporting text, captions |
| Label | Poppins | 11px | 600 | 1.4 | 0.8px | Eyebrows, section labels, nav |
| Code | JetBrains Mono | 13px | 400 | 1.6 | 0 | Technical strings, tokens |

### Typography Rules

- Druk is **display only**. Never use it below 40px. Always uppercase. Never use it for anything functional.
- Poppins semibold (600) is the default for any heading under 32px.
- Body weight is 400 at 15px, 500 at 17px — Poppins holds legibility well at these weights.
- Minimum contrast ratio: 4.5:1 for body text, 3:1 for large text.
- Avoid centered body text beyond 2 lines. Left-align for readability.
- Limit line length to 65–75 characters for body copy.
- Never mix font families within a single component — pick display or body, not both.

---

## 4. Component Styling

### Buttons

The button hierarchy is designed to create clear visual weight from most to least dominant. Only one primary CTA should appear per primary action area. Secondary and ghost buttons should feel like they belong to the background, not competing for attention.

**Primary (Gradient)** — one per action context
```css
background: linear-gradient(90deg, #5a63d3, #3342ff);
color: #ffffff;
border-radius: 60px;
padding: 12px 28px;
font-family: 'Poppins', sans-serif;
font-size: 14px;
font-weight: 600;
border: none;
cursor: pointer;
transition: opacity 0.2s ease, transform 0.18s cubic-bezier(0.34, 1.56, 0.64, 1);
```
Hover: `opacity: 0.88; transform: translateY(-2px)`
Active: `transform: translateY(1px) scale(0.97)` — 0.07s snap, spring release

**Secondary (Surface card)** — clean, neutral, never colored
```css
background: var(--surface-1);       /* white on light, #130f22 on dark */
color: var(--text-primary);
border: 1px solid var(--border-default);
border-radius: 60px;
padding: 12px 28px;
font-family: 'Poppins', sans-serif;
font-size: 14px;
font-weight: 500;                   /* lighter than primary — intentionally less dominant */
transition: background 0.2s ease, transform 0.18s cubic-bezier(0.34, 1.56, 0.64, 1);
```
Hover: steps up one surface level (`surface-2`), border unchanged

**Ghost (Text-level)** — transparent, minimal presence
```css
background: transparent;
color: var(--text-secondary);       /* muted by default — recedes further than secondary */
border: 1px solid transparent;     /* invisible border maintains sizing, avoids layout shift */
border-radius: 60px;
padding: 12px 28px;
font-weight: 500;
```
Hover: fills to `surface-2`, text steps up to `text-primary`, `border-subtle` rim appears

**Accent (Lime)** — brand emphasis, use sparingly
```css
background: #c9eb00;
color: #0c0718;
border-radius: 60px;
padding: 12px 28px;
font-weight: 600;
```
Hover: `background: #b8d600`

**Sizes:**
- Small: `padding: 7px 18px; font-size: 12px`
- Default: `padding: 12px 28px; font-size: 14px`
- Large: `padding: 16px 40px; font-size: 16px`

**Tactile press state (all variants):**
```css
:active {
  transform: translateY(1px) scale(0.97) !important;
  transition-duration: 0.07s !important;
  transition-timing-function: ease !important;
}
```

### Cards

Cards are neutral containers. They do not use accent colors as fills, tinted backgrounds, or decorative borders. The card surface is always one step above the page background — no more.

```css
/* Dark mode */
background: #130f22;
border-radius: 16px;
padding: 24px;
border: 1px solid rgba(46, 40, 80, 0.6);
box-shadow: 0 4px 12px rgba(0,0,0,0.3);
transition: transform 0.2s ease, box-shadow 0.2s ease;
```
Hover: `transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,0,0,0.4)`

```css
/* Light mode */
background: #ffffff;
border: 1px solid #d4cfea;
box-shadow: 0 2px 8px rgba(12, 7, 24, 0.06);
```

Card variants (accent only used on top border, never fill):
- Default: neutral border
- Accent: `border-top: 2px solid var(--tari-lime)` — one line of color, rest neutral

### Form Inputs

Inputs use underline-only style. No box, no background fill. This keeps forms open and airy — the page surface shows through, reducing visual noise.

```css
/* Input field */
display: block;
width: 100%;
padding: 8px 0 10px;
background: transparent;
border: none;
border-bottom: 1px solid var(--border-default);
border-radius: 0;
font-family: 'Poppins', sans-serif;
font-size: 14px;
color: var(--text-primary);
outline: none;
```

Focus state — animated lime sweep via `::after` on the wrapper:
```css
.input-wrap { position: relative; }
.input-wrap::after {
  content: '';
  position: absolute; bottom: 0; left: 0;
  width: 100%; height: 2px;
  background: #c9eb00;
  transform: scaleX(0);
  transform-origin: left center;
  transition: transform 0.28s cubic-bezier(0.4, 0, 0.2, 1);
}
.input-wrap:focus-within::after { transform: scaleX(1); }
```

### Badges

Badges are minimal: pill shape, neutral border, muted text. The dot carries semantic color — not the entire element.

```css
display: inline-flex;
align-items: center;
gap: 6px;
padding: 3px 10px 3px 8px;
border-radius: 999px;
font-size: 11px;
font-weight: 500;
letter-spacing: 0.2px;
border: 1px solid var(--border-default);
background: transparent;
color: var(--text-secondary);
```

Dot `::before` carries the semantic accent color. Title and background stay neutral.

### Toast / Alert Notifications

Notifications are neutral cards elevated above the surface — they do not use tinted backgrounds or colored fills. The icon carries the semantic meaning.

```css
display: flex;
align-items: flex-start;
gap: 11px;
padding: 13px 14px;
background: var(--surface-1);
border: 1px solid var(--border-subtle);
border-radius: var(--radius-lg);
box-shadow: 0 8px 28px rgba(12,7,24,0.1), 0 2px 6px rgba(12,7,24,0.05);
```

Icon colors per variant (icon only — title and body text stay neutral):
- Success: `#1a5c1c` (light) / `#71ee73` (dark)
- Warning: `#7a4400` (light) / `#ffab25` (dark)
- Error: `#8c1a1a` (light) / `#ff7070` (dark)
- Info: `#1a28cc` (light) / `#8b94ff` (dark)

### Navigation

```css
position: sticky;
top: 0;
background: rgba(12, 7, 24, 0.85);
backdrop-filter: blur(12px);
-webkit-backdrop-filter: blur(12px);
border-bottom: 1px solid var(--border-subtle);
padding: 0 24px;
height: 52px;
```

Nav links: `color: var(--text-secondary)` default, `color: var(--text-primary)` active, `font-weight: 500`

### Checkboxes & Radios

Custom-styled selection controls. Spring animation on check (`cubic-bezier(0.34, 1.56, 0.64, 1)`) — brief, physical, non-decorative.

Checked state on dark: `background: #c9eb00` with **black** (`#0c0718`) checkmark. Never white on lime — contrast fails.
Checked state on light: `background: #3342ff` with white checkmark.

### Toggle Switch

```css
.toggle-track {
  width: 44px; height: 24px;
  border-radius: 40px;
  background: var(--surface-3);
  transition: background 0.2s ease;
}
.toggle-track::after {
  content: '';
  position: absolute;
  width: 18px; height: 18px;
  border-radius: 50%;
  background: var(--text-muted);
  top: 3px; left: 3px;
  transition: transform 0.25s cubic-bezier(0.34, 1.56, 0.64, 1);
}
input:checked ~ .toggle-track { background: #c9eb00; }
input:checked ~ .toggle-track::after {
  transform: translateX(20px);
  background: #0c0718;        /* always dark thumb on lime track */
}
```

---

## 5. Layout Principles

### Grid System

- **Base unit:** 8px
- **Columns:** 12-column grid, `gap: 24px`
- **Max content width:** 1200px, centered with `margin: auto`
- **Page padding:** 24px mobile, 48px tablet, 80px desktop
- **Section spacing:** 100–160px between major sections

### Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--sp-1` | 4px | Micro gaps, icon padding |
| `--sp-2` | 8px | Base unit, tight spacing |
| `--sp-3` | 12px | Input padding, small gaps |
| `--sp-4` | 16px | Component padding |
| `--sp-5` | 20px | Card inner spacing |
| `--sp-6` | 24px | Grid gap, section padding |
| `--sp-8` | 32px | Card padding, content blocks |
| `--sp-10` | 40px | Section sub-spacing |
| `--sp-12` | 48px | Section margins |
| `--sp-16` | 64px | Large section gaps |
| `--sp-20` | 80px | Page-level padding |
| `--sp-24` | 96px | Major section breaks |
| `--sp-32` | 128px | Hero padding |

### Layout Patterns

**Hero:** Full-width, `padding-top: 140px`, Druk display type. Minimal chrome — type and a single CTA. No decorative fills, no busy backgrounds.

**Feature Grid:** 3-column on desktop, 2-column tablet, 1-column mobile. Cards with neutral borders, hover lift. No colored card backgrounds.

**Content Width:** Body copy maxes at 680px. Full-width for visual/showcase sections.

**Sidebar Layouts:** Fixed 220px sidebar, scrollable main content, IntersectionObserver scrollspy.

---

## 6. Depth & Elevation

Depth is communicated through surface layering and shadow — not through color. Avoid using accent tints to express elevation. The surface stack (`surface-0` → `surface-1` → `surface-2` → `surface-3`) provides all the depth needed.

### Shadow Scale

| Level | Value | Usage |
|-------|-------|-------|
| None | none | Flat elements, text, labels |
| 1 (subtle) | `0 1px 4px rgba(0,0,0,0.08)` | Inline cards, separators |
| 2 (base) | `0 4px 12px rgba(0,0,0,0.10)` | Default cards |
| 3 (raised) | `0 8px 24px rgba(0,0,0,0.12)` | Elevated cards, dropdowns |
| 4 (floating) | `0 8px 32px rgba(0,0,0,0.45)` | Toasts, popovers (dark) |
| 5 (overlay) | `0 16px 48px rgba(0,0,0,0.16)` | Modals |

### Border Radius Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | 6px | Small inputs, chips |
| `--radius-md` | 12px | Inputs, small cards |
| `--radius-lg` | 16px | Cards, panels, toasts |
| `--radius-xl` | 24px | Large cards, containers |
| `--radius-pill` | 60px | Buttons, tags |
| `--radius-full` | 9999px | Avatars, status dots |

---

## 7. Do's and Don'ts

### Do

- **Start with less.** Default to fewer elements, less color, less decoration. Add only when clarity demands it.
- Use `#c9eb00` lime as the primary accent — sparingly, for one active or primary element per section
- Apply Druk only at display sizes (40px+), always uppercase, never for decoration
- Use Poppins 400–600 for all body and UI text — weight does the work, embellishment doesn't
- Keep buttons minimal: pill radius, generous padding, only one gradient button per action area
- Use `surface-1` / `border-default` for secondary buttons — clean surface card, no color
- Use underline-only inputs — the open style keeps layouts light and readable
- Keep cards neutral: `surface-1` background, `border-subtle` border, shadow for elevation only
- Keep notifications neutral: icon carries semantic color, background and text stay neutral
- Prefer `backdrop-filter: blur(12px)` over opaque surfaces for sticky navs and overlays
- Maintain the cream (`#fbf7ef`) background for light mode — never pure white

### Don't

- **Don't add color to communicate hierarchy** — use size, weight, and spacing instead
- Don't tint card backgrounds with accent colors — cards are always neutral surfaces
- Don't use colored backgrounds on alerts, toasts, or notifications — icon color is enough
- Don't make secondary buttons blue — they should be invisible until needed
- Don't use more than one accent color per view — pick lime or green, not both
- Don't use `#ffffff` pure white as a background in light mode — always `#fbf7ef`
- Don't use Druk below 40px or for anything functional — it's display-only
- Don't apply the gradient to secondary, ghost, or accent buttons — primary CTA only
- Don't use flat shadows in dark mode — they won't read
- Don't use system blue for links — use `#c9eb00` (dark mode) or `#3342ff` (light mode)
- Don't center-align body paragraphs — center only for short headlines and CTAs
- Don't add decorative elements to fill space — the palette and type do the work
- Don't reduce `border-radius` below 10px on cards — rounded corners are a brand signal

---

## 8. Responsive Behavior

### Breakpoints

| Name | Width | Target |
|------|-------|--------|
| Mobile | < 640px | Phones |
| Tablet | 640px – 1024px | Tablets, small laptops |
| Desktop | 1024px – 1280px | Standard desktop |
| Wide | 1280px+ | Large monitors |

### Scaling Rules

- **Display type (Druk):** Scale from 48px mobile → 80px tablet → 120px desktop
- **Heading 1 (Poppins):** 28px mobile → 36px tablet → 48px desktop
- **Grid:** 1-column mobile → 2-column tablet → 3-column desktop
- **Buttons:** Full-width on mobile (max 100%), inline on tablet+
- **Cards:** `border-radius: 16px` maintained across all sizes — do not reduce for mobile
- **Nav:** Collapse to hamburger below 768px
- **Section padding:** 48px top/bottom on mobile → 100px on tablet → 140px on desktop
- **Sidebar layouts:** Sidebar collapses below 768px; content takes full width

### Mobile Adjustments

```css
@media (max-width: 640px) {
  .display-xl { font-size: 48px; }
  .section-padding { padding: 48px 20px; }
  .btn { width: 100%; justify-content: center; }
  .card-grid { grid-template-columns: 1fr; }
}
```

---

## 9. Agent Prompt Guide

Use the following when prompting AI agents to generate Tari-native UI.

### System Prompt Snippet

```
You are generating UI for the Tari ecosystem. The design language is minimal and sleek — clean surfaces, generous whitespace, restrained color use. Every element must earn its place.

PHILOSOPHY:
- Minimal first. Remove before adding. Space is the design.
- Neutral by default. Only the primary CTA, active states, and icons carry accent color.
- No tinted backgrounds on cards, alerts, or secondary UI — surfaces are always neutral.
- Secondary buttons are quiet surface cards. Ghost buttons are nearly invisible. Only one gradient button per action context.

COLORS:
- Dark background: #0c0718 (deep aubergine-black)
- Light background: #fbf7ef (warm cream — never pure white)
- Primary accent: #c9eb00 (electric lime — use sparingly)
- Secondary accent: #71ee73 (bright green — status/success only)
- Highlight: #ffab25 (orange — warning only)
- Primary CTA gradient: linear-gradient(90deg, #5a63d3, #3342ff) — primary button only

TYPOGRAPHY:
- Display headlines: Druk Wide font, uppercase, 800 weight, 40px+ only
- All other text: Poppins, 400–600 weight
- Body defaults: Poppins 400, line-height 1.45, letter-spacing -0.25px
- No decorative type — Druk is reserved for hero moments only

BUTTONS:
- Primary: gradient background (#5a63d3 → #3342ff), 60px border-radius, white text, weight 600
- Secondary: neutral surface background (surface-1), standard border (border-default), text-primary, weight 500 — NOT blue, NOT gradient
- Ghost: fully transparent, text-secondary color, no visible border — recedes into background
- Accent: #c9eb00 background, #0c0718 text, 60px radius, weight 600
- All buttons have tactile press: translateY(1px) scale(0.97), 0.07s snap, spring release

CARDS:
- Background: neutral surface (surface-1) — never tinted with accent color
- Border-radius: 16px
- Border: 1px solid border-subtle or border-default
- Shadow for elevation only — not decoration
- Hover: translateY(-2px), shadow steps up one level

INPUTS:
- Underline-only — no box, no background fill
- Focus: 2px lime line sweeps in from left using scaleX animation
- Border-bottom only, transparent background

NOTIFICATIONS / ALERTS:
- Neutral card background (surface-1) — never tinted
- Semantic color on icon only — title and body text stay neutral (text-primary / text-secondary)
- Same card treatment as toasts: border-subtle border, elevated shadow

SPACING:
- 8px base unit, multiples of 8 for all spacing
- Section padding: 100–140px top/bottom
- Content max-width: 1200px

OUTPUT:
- Generate valid HTML + inline or embedded CSS
- Include Google Fonts import for Poppins (400,500,600,700)
- Note where Druk would be used (licensed font — substitute Impact or a bold sans for preview)
- Prefer semantic HTML: nav, main, section, article, aside, footer
- When in doubt, use less — a clean neutral surface beats a busy decorated one
```

### Quick Reference Tokens

```css
:root {
  /* Brand */
  --tari-dark:     #0c0718;
  --tari-cream:    #fbf7ef;
  --tari-lime:     #c9eb00;
  --tari-green:    #71ee73;
  --tari-orange:   #ffab25;
  --tari-blue:     #3342ff;
  --tari-purple:   #5a63d3;
  --tari-gradient: linear-gradient(90deg, #5a63d3, #3342ff);

  /* Surfaces (dark) */
  --surface-0:  #0c0718;
  --surface-1:  #130f22;
  --surface-2:  #1e1836;
  --surface-3:  #2e2850;

  /* Text (dark) */
  --text-primary:   #fbf7ef;
  --text-secondary: #9993b0;
  --text-muted:     #706a90;

  /* Borders */
  --border-subtle:  rgba(46, 40, 80, 0.6);
  --border-default: #2e2850;

  /* Radius */
  --radius-sm:   6px;
  --radius-md:   12px;
  --radius-lg:   16px;
  --radius-xl:   24px;
  --radius-pill: 60px;

  /* Spacing */
  --sp-1:  4px;
  --sp-2:  8px;
  --sp-3:  12px;
  --sp-4:  16px;
  --sp-6:  24px;
  --sp-8:  32px;
  --sp-10: 40px;
  --sp-12: 48px;
  --sp-16: 64px;
  --sp-20: 80px;
}
```
