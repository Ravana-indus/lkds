# LankaDS — Sri Lanka National Design System

**v1.1 · Draft for review** · The shared design foundation behind **Sewa**, the national super app, and every Government of Sri Lanka digital service. Built for the GovTech digital transformation programme.

> **Philosophy, fixed and ordered: easy access · inclusivity · citizen first.**
> එක ජාතියක්. එක යෙදුමක්. · ஒரு தேசம். ஒரு செயலி. · One Nation. One App.

## What makes it different

- **Unity Gold leads.** Primary actions are gold `#F0B41E` with ink text (9.54:1 AAA) — the one colour of the national flag that belongs to every community. Maroon, saffron and green are equal categorical pillars; no single community's colour leads the state's interface.
- **Trilingual by default.** Sinhala, Tamil and English designed together on the harmonised Noto superfamily, with per-script metrics (`:lang(si)` 1.75 leading, `:lang(ta)` 1.7).
- **Accessible by the numbers.** WCAG 2.2 AA mandatory; every approved colour pairing ships with its measured contrast ratio. 48 px touch targets. Ink focus ring on light, gold on dark.
- **Built for every connection.** 360 px budget-Android reference device, ≤500 KB page budget, offline-tolerant flows, SMS/USSD fallbacks.

## Repository layout

| Path | What it is |
|---|---|
| [`design.md`](design.md) | The complete written specification — principles, brand, colour, type, components, patterns, standards, governance |
| [`tokens/lankads-tokens.css`](tokens/lankads-tokens.css) | CSS custom properties (`--lk-*`) — light + dark themes, script helpers |
| [`tokens/lankads-tokens.json`](tokens/lankads-tokens.json) | W3C design-tokens format — pipe into Style Dictionary for iOS / Android / Flutter / Figma |
| [`docs/index.html`](docs/index.html) | Interactive documentation site with live components (open locally or serve via GitHub Pages) |

## Quick start

```html
<link rel="stylesheet" href="tokens/lankads-tokens.css">
<button style="
  background: var(--lk-color-action-primary);
  color: var(--lk-color-action-on-primary);   /* ink — never white on gold */
  height: var(--lk-size-control-md);
  border-radius: var(--lk-radius-md);
">Apply now · දැන් අයදුම් කරන්න · இப்போது விண்ணப்பிக்கவும்</button>
```

Teams build against **semantic** tokens only (`--lk-color-action-primary`, not `--lk-gold-500`) so core values can be tuned centrally without breaking products. Dark theme: `[data-lk-theme="dark"]`.

## Three hard rules

1. **Gold never carries white or light text** — every gold surface takes ink.
2. **Saffron-600 is large-text only** — step to saffron-700+ for body copy.
3. **Focus ring is ink on light surfaces, gold-500 on dark** — gold alone on light fails 3:1.

## Status

Draft for review. Sinhala/Tamil reference strings pending ratification by the Department of Official Languages. See `design.md` § Governance for the contribution model, versioning policy and roadmap.
