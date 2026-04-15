# Tari Design System

The visual foundation for apps built on the Ootle. Drop `tokens.css` into your project and attach `spec.md` to your AI agent — you're ready to build.

---

## Files

| File | What it is |
|------|------------|
| `tokens.css` | **Start here.** All CSS custom properties, @font-face declarations, and a base reset. Drop directly into any project. |
| `spec.md` | Full design system documentation — philosophy, token roles, component patterns, do's and don'ts. Feed this to your AI agent. |
| `PROMPT.md` | **Ready-to-copy agent prompts.** Quick version for everyday tasks, full version for new projects. |
| `Tari-Agentic-Design-Template-Dark.html` | Live reference — full token catalog in dark mode. Open in a browser. |
| `Tari-Agentic-Design-Template-Light.html` | Live reference — full token catalog in light mode. Open in a browser. |

---

## Quickstart

**1. Add the tokens**

Copy `tokens.css` into your project and link it:
```html
<link rel="stylesheet" href="tokens.css">
```
Or paste the `:root` block from `tokens.css` into your existing stylesheet.

**2. Add the fonts**

Paste this into your HTML `<head>` (already included in `tokens.css` as a comment):
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;0,600;0,700;1,500&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
```
Druk Wide loads automatically via the `@font-face` rules in `tokens.css`.

**3. Tell your agent**

Open `PROMPT.md` and paste the **Quick Prompt** into your AI tool before your task. For a new project or full layout, use the **Full Prompt** instead.

---

## Using with AI Agents

### Claude (claude.ai or Claude Code)
Drag `spec.md` into the conversation or add it as a project-level instruction. Paste the Quick Prompt from `PROMPT.md` before describing your task.

### Cursor
Reference `spec.md` with `@spec.md` in chat, or add it to `.cursorrules`.

### Any other tool
Paste the full contents of `spec.md` as a system prompt, then start your request.

**Pro tip:** With `tokens.css` already in your codebase, the agent has live token names to reference (`var(--surface-1)`, `var(--tari-lime)`, etc.) — no guesswork, no hallucinated hex values.

---

## Design Language at a Glance

| | Dark | Light |
|---|---|---|
| Page background | `#0c0718` — deep aubergine | `#fbf7ef` — warm cream |
| Surface | `#130f22` | `#ffffff` |
| Text | `#fbf7ef` | `#0c0718` |
| Accent | `#c9eb00` — electric lime | same |
| Primary CTA | `linear-gradient(90deg, #5a63d3, #3342ff)` | same |

**Fonts:** Druk Wide (display, 40px+, uppercase) · Poppins (all UI) · JetBrains Mono (code)

**Radius:** 60px buttons · 16px cards · 6–12px small components

**Core principle:** Minimal and sleek. Neutral surfaces, one accent, earned decoration.
