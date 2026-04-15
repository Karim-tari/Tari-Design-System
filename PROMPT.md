# Tari Design System — Agent Prompt

Copy the prompt below into Claude, Cursor, or any AI coding tool. It gives the agent everything it needs to generate UI that looks native to the Tari ecosystem.

---

## Quick Prompt (paste this for most tasks)

```
Use the Tari design system. Key rules:

PHILOSOPHY: Minimal and sleek. Every element earns its place. Space is the design. No decorative fills, no accent-colored backgrounds — surfaces are always neutral.

FONTS:
- Display (headlines 40px+): DrukWideFont / Druk Wide — uppercase always, weight 700–800
- Body / UI: Poppins — weight 400 (body), 500 (UI), 600 (headings), 700 (bold)
- Mono: JetBrains Mono
- Google Fonts: https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;0,600;0,700;1,500&family=JetBrains+Mono:wght@400;500&display=swap

COLORS (dark theme):
- Page bg:        #0c0718  (deep aubergine-black)
- Surface:        #130f22
- Surface raised: #1e1836
- Border:         #2e2850
- Text primary:   #fbf7ef
- Text secondary: #9993b0
- Text muted:     #706a90
- Accent:         #c9eb00  (lime — use sparingly)
- Gradient CTA:   linear-gradient(90deg, #5a63d3, #3342ff)

COLORS (light theme — swap these):
- Page bg:        #fbf7ef  (warm cream — never pure white)
- Surface:        #ffffff
- Surface raised: #f6f4fb
- Border:         #d4cfea
- Text primary:   #0c0718
- Text secondary: #4a4468

BUTTONS:
- Primary:   gradient (#5a63d3→#3342ff), white text, weight 600, 60px radius — one per action area
- Secondary: neutral surface bg + border-default, text-primary, weight 500 — NOT blue, never gradient
- Ghost:     transparent bg, text-secondary, no visible border — recedes into background
- Accent:    #c9eb00 bg, #0c0718 text, weight 600

CARDS: neutral surface-1 bg, border-subtle or border-default border, 16px radius, soft shadow. No colored fills ever.

INPUTS: underline-only (border-bottom, no box). On focus: 2px lime line sweeps in from left via scaleX(0)→scaleX(1) animation.

ALERTS / TOASTS: neutral card (surface-1 bg, border-subtle). Semantic color on icon only — title and body text stay neutral.

RADIUS: buttons 60px pill, cards 16px, small components 6–12px.

SPACING: 8px base unit. Use multiples of 4/8.
```

---

## Full Prompt (use when starting a new project or layout from scratch)

```
You are building UI for the Tari ecosystem. The design language is minimal and sleek — clean surfaces, generous whitespace, restrained color. Every element must earn its place.

━━━ PHILOSOPHY ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

- Minimal first. Default to less. Add only when clarity demands it.
- Neutral by default. Only the primary CTA, active states, and icons carry accent color.
- No tinted backgrounds on cards, alerts, or secondary UI — surfaces are always neutral.
- Secondary buttons are quiet surface cards. Ghost buttons are nearly invisible.
- One gradient button per action context maximum.
- Space is the design. Generous whitespace communicates quality.

━━━ FONTS ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Google Fonts link (add to <head>):
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;0,600;0,700;1,500&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

Druk Wide @font-face (add to CSS — loads from tari.com CDN):
@font-face { font-family:'DrukWideFont'; src:url('https://www.tari.com/_next/static/media/e03750ebf8ed0d54-s.p.ttf') format('truetype'); font-weight:500; font-style:normal; font-display:block; }
@font-face { font-family:'DrukWideFont'; src:url('https://www.tari.com/_next/static/media/1f00708acd790523-s.p.ttf') format('truetype'); font-weight:700; font-style:normal; font-display:block; }
@font-face { font-family:'DrukWideFont'; src:url('https://www.tari.com/_next/static/media/d15778d6fa440100-s.p.ttf') format('truetype'); font-weight:800; font-style:italic; font-display:block; }

--font-display: 'DrukWideFont', 'Druk Wide', 'Druk', Arial, sans-serif;
--font-body:    'Poppins', system-ui, sans-serif;
--font-mono:    'JetBrains Mono', monospace;

Rules:
- Druk: display only, 40px+, UPPERCASE, weight 700–800, line-height 0.9–0.95
- Poppins: everything else — weight 400 body, 500 UI, 600 headings <32px, 700 headings >32px
- Body defaults: font-size 15px, line-height 1.45, letter-spacing -0.25px

━━━ CSS TOKENS ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

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

  /* Dark theme surfaces */
  --surface-0: #0c0718;
  --surface-1: #130f22;
  --surface-2: #1e1836;
  --surface-3: #2e2850;

  /* Dark theme text */
  --text-primary:   #fbf7ef;
  --text-secondary: #9993b0;
  --text-muted:     #706a90;

  /* Dark theme borders */
  --border-subtle:  rgba(46,40,80,0.5);
  --border-default: #2e2850;

  /* Radius */
  --radius-sm:   6px;
  --radius-md:   12px;
  --radius-lg:   16px;
  --radius-xl:   24px;
  --radius-pill: 60px;

  /* Spacing */
  --sp-1: 4px;  --sp-2: 8px;   --sp-3: 12px;
  --sp-4: 16px; --sp-6: 24px;  --sp-8: 32px;
  --sp-10: 40px; --sp-12: 48px; --sp-16: 64px; --sp-20: 80px;
}

/* Light theme overrides */
[data-theme="light"] {
  --surface-0: #fbf7ef;
  --surface-1: #ffffff;
  --surface-2: #f6f4fb;
  --surface-3: #ece9f5;
  --text-primary:   #0c0718;
  --text-secondary: #4a4468;
  --text-muted:     #8a84a8;
  --border-subtle:  #e8e4f4;
  --border-default: #d4cfea;
}

━━━ COMPONENTS ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

BUTTONS — hierarchy from dominant to invisible:

/* Primary — one per action context */
.btn-primary {
  background: var(--tari-gradient);
  color: #fff; font-weight: 600;
  padding: 12px 28px; border-radius: var(--radius-pill);
  border: none;
}
.btn-primary:hover { opacity: 0.88; transform: translateY(-2px); }

/* Secondary — neutral surface card, not blue */
.btn-secondary {
  background: var(--surface-1);
  color: var(--text-primary); font-weight: 500;
  border: 1px solid var(--border-default);
  padding: 12px 28px; border-radius: var(--radius-pill);
}
.btn-secondary:hover { background: var(--surface-2); }

/* Ghost — transparent, recedes into background */
.btn-ghost {
  background: transparent;
  color: var(--text-secondary); font-weight: 500;
  border: 1px solid transparent;
  padding: 12px 28px; border-radius: var(--radius-pill);
}
.btn-ghost:hover { background: var(--surface-2); color: var(--text-primary); }

/* Accent — lime, use sparingly */
.btn-accent {
  background: var(--tari-lime);
  color: var(--tari-dark); font-weight: 600;
  padding: 12px 28px; border-radius: var(--radius-pill);
  border: none;
}

/* All buttons — tactile press feel */
.btn:active {
  transform: translateY(1px) scale(0.97) !important;
  transition-duration: 0.07s !important;
}

CARDS — always neutral, never tinted:

.card {
  background: var(--surface-1);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-lg);
  padding: 24px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.3); /* dark */
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.card:hover { transform: translateY(-2px); }

/* Accent variant — lime top border only, rest neutral */
.card-accent { border-top: 2px solid var(--tari-lime); }

FORM INPUTS — underline only, open and airy:

.input-wrap { position: relative; }
.input-wrap::after {
  content: ''; position: absolute; bottom: 0; left: 0;
  width: 100%; height: 2px;
  background: var(--tari-lime);
  transform: scaleX(0); transform-origin: left center;
  transition: transform 0.28s cubic-bezier(0.4, 0, 0.2, 1);
}
.input-wrap:focus-within::after { transform: scaleX(1); }

.form-input {
  display: block; width: 100%;
  padding: 8px 0 10px;
  background: transparent;
  border: none; border-bottom: 1px solid var(--border-default);
  border-radius: 0;
  font-family: var(--font-body); font-size: 14px;
  color: var(--text-primary); outline: none;
}

ALERTS / TOASTS — neutral card, semantic icon only:

.alert, .toast {
  display: flex; align-items: flex-start; gap: 11px;
  padding: 13px 14px;
  background: var(--surface-1);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-lg);
  box-shadow: 0 8px 28px rgba(0,0,0,0.1), 0 2px 6px rgba(0,0,0,0.05);
}
/* Icon color only — title/body stay neutral */
.alert-success .icon, .toast-success .icon { color: var(--color-success); }
.alert-warning .icon, .toast-warning .icon { color: var(--color-warning); }
.alert-error   .icon, .toast-error   .icon { color: var(--color-error);   }
.alert-info    .icon, .toast-info    .icon { color: var(--color-info);    }

━━━ ANIMATION ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Spring easing (checkboxes, toggles, buttons):
  cubic-bezier(0.34, 1.56, 0.64, 1)

Directional sweep (form inputs, underlines):
  cubic-bezier(0.4, 0, 0.2, 1)

Standard ease (hover, opacity, background):
  0.2s ease

Fast snap on active/press:
  0.07s ease — then spring release on mouse-up

━━━ RULES ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✓  Use var(--tari-lime) as the single active/accent color — sparingly
✓  Cards, alerts, secondary buttons — always neutral backgrounds
✓  One gradient button per action area maximum
✓  Druk = display only (40px+, uppercase). Poppins = everything else
✓  Checkmark/icon on lime background must be #0c0718 (dark) — never white

✗  No colored card backgrounds
✗  No tinted alert/toast backgrounds — icon color is enough
✗  No secondary buttons in blue or gradient
✗  No Druk below 40px
✗  No pure white (#ffffff) as page background in light mode — use #fbf7ef
✗  Never white text on lime (#c9eb00) — use #0c0718
```

---

## Attaching the Design System

**Claude (claude.ai or Claude Code):**
Drag `spec.md` into the conversation, or add it as a project instruction. Then paste the Quick Prompt above before your task.

**Cursor:**
Add `spec.md` to your `.cursorrules` file or reference it with `@spec.md` in the chat.

**Any other tool:**
Paste the full contents of `spec.md` as a system prompt, then start your request.

**Pro tip:** For new projects, start with `tokens.css` already in your codebase. Then attach `spec.md` to your agent context. The agent has live token names to reference — no guesswork.
