# LankaDS — Sri Lanka National Design System

**Version 1.1 · Draft for review · 2026-06-13**
Prepared for the GovTech digital transformation programme.
Brand anchor: **Sewa**, the national super app. ශ්‍රී ලංකා ජාතික නිර්මාණ පද්ධතිය · இலங்கை தேசிய வடிவமைப்பு முறைமை

> **One nation. One design language.**
> Philosophy, fixed and ordered: **easy access · inclusivity · citizen first.**

LankaDS is the shared foundation behind Sewa and every Government of Sri Lanka digital service. It leads with **Unity Gold** — the one colour of the national flag that belongs to every community — and turns the rising-pillars identity into tokens, components and patterns, so every ministry ships services that feel like one modern, progressive, trusted government.

**Companion files**

| File | Purpose |
|---|---|
| `lankads-tokens.css` | CSS custom properties — light + dark themes, script helpers |
| `lankads-tokens.json` | W3C design-tokens format — pipe into Style Dictionary for iOS / Android / Flutter / Figma |

---

## 1. Design principles

Six commitments. They resolve disputes: when two options conflict, the higher principle wins.

1. **Citizen first, ministry second** · පුරවැසියා පළමුව · குடிமக்கள் முதலில்
   Organise around life events — a birth, a job, a business, a pension — never around departmental structure. The citizen finishes the task without learning how government is organised.

2. **Inclusive by design** · සියලු දෙනාටම · அனைவரையும் உள்ளடக்கி
   No community, language, age or ability is an edge case. The interface leads with Unity Gold — the flag's shared colour — because even a palette can take sides. Trilingual parity, assisted modes and equal pillar status are enforced at token level, not left to goodwill.

3. **Easy access for everyone** · පහසු ප්‍රවේශය · எளிதான அணுகல்
   WCAG 2.2 AA is the floor, not the ceiling. 48 px targets, plain language, journeys a first-time smartphone user finishes unaided — and assisted use at a Grama Niladhari office designed in from the start.

4. **Trilingual by default** · භාෂා තුනෙන්ම · மும்மொழிகளிலும்
   Sinhala, Tamil and English are designed together, not translated after. Every screen, error and SMS ships in all three; layouts are tested against the longest of the three strings.

5. **Built for every connection** · සෑම සම්බන්ධතාවයකටම · எல்லா இணைப்புகளுக்கும்
   Honour the 2G village and the budget Android. Pages under 500 KB, offline-tolerant flows, SMS/USSD fallbacks for critical notifications.

6. **Progressive, modern, trusted** · නවීන හා විශ්වාසනීය · நவீனமும் நம்பிக்கையும்
   Government services should feel as good as the best consumer apps — fast, warm, beautifully made. Consistency is also a security feature: when every legitimate screen looks the same, phishing stands out. Never restyle core components per ministry.

---

## 2. Brand & logo

The Sewa mark is a skyline of pillars in the four colours of the national flag — communities at different points in their journey, rising together toward a shared golden summit. It reads simultaneously as a city rising, a chart climbing, and a flame.

**Symbolism**

- **Four colours, one flag.** Maroon, saffron, gold and green carry the communities of the national flag into a single rising form — held in deliberate equality.
- **Unequal heights.** Citizens start from different places; the system exists to help every pillar rise.
- **The golden summit.** Gold is the colour the flag gives to everyone — the border that wraps all communities equally. That is why it leads the interface: every primary action a citizen takes is golden.
- **The forward lean.** Pillars shear 6° forward: progress, not monument. A government in motion.

**Usage rules**

| Rule | Specification |
|---|---|
| Clear space | ½ the mark's height on all sides, free of text, imagery, other logos |
| Minimum size — digital | 24 × 24 px; below 32 px use the simplified 4-pillar cut |
| Minimum size — print | 8 mm height |
| Co-branding | Ministry crests sit **after** the Sewa mark, separated by a 1 px stone-300 rule, never larger than the mark |
| Backgrounds | White, stone-50 canvas, or ink-900 photographic scrim tested to ≥3:1 |
| Don't | Recolour, re-order, rotate, mirror, outline, shadow, stretch, place on busy photography, or rebuild per ministry |

**The national ribbon.** A 6–8 px strip of the four colours marks the top of every official page and document — the fastest signal of authenticity. Fixed order (green → saffron → maroon → gold), fixed proportions (25% each), never re-sequenced. Token: `--lk-gradient-ribbon`.

---

## 3. Colour

All colour is sampled from the Sewa mark itself, then extended into eleven-step ramps (50–950). **Unity Gold leads; the four pillars hold equal categorical status; warm stone neutrals do the listening.**

### Why gold leads — inclusion, enforced in the palette

In the national flag, maroon, saffron and green each belong to one community. **Gold belongs to all of them** — the border that wraps every panel equally, and the shared summit of the Sewa mark. A state interface that led with any single community's colour would quietly take a side. LankaDS therefore gives the lead role to gold and uses the community pillars only as equal categorical accents. Inclusivity here is not a value statement — it is enforced in the tokens.

### The four pillars

| Pillar | Anchor value | Role |
|---|---|---|
| **Gold — the lead** | `#F0B41E` · gold-500 | Unity. The primary action colour — buttons, selections, progress. **Always carries ink text, never white.** |
| **Maroon** | `#8D153A` · maroon-600 | Heritage and gravitas. Equal categorical pillar — identity & documents, data viz. Never the lead. |
| **Saffron** | `#DC580A` · saffron-600 | Energy and momentum. Equal pillar — "action needed" states, promotional accents. |
| **Green** | `#005A32` · green-700 | Growth and confirmation. Equal pillar — success, completed steps, "approved". |

### Supporting colours

| Name | Value | Role |
|---|---|---|
| Stone canvas | `#FAF8F4` · stone-50 | Page background (warm paper white, sampled from brand sheet) |
| Surface white | `#FFFFFF` · stone-0 | Cards, sheets |
| Ink | `#16181A` | Primary text, sampled from the Sewa wordmark |
| Danger scarlet | `#C42B1C` · danger-600 | Errors only — deliberately distinct from maroon |
| Link blue | `#1158A6` · info-600 | Links, information |
| Sunrise gradient | `#FFD95A → gold-500 → saffron` | Marketing surfaces and app header only, never UI chrome |

Full 50–950 ramps for every family live in the token files.

### Semantic roles

| Role | Token | Value | Used for |
|---|---|---|---|
| Primary action | `--lk-color-action-primary` | gold-500 | Primary buttons, selected controls, active language, progress |
| On-primary | `--lk-color-action-on-primary` | ink | Text/icons on gold. Gold never carries white text (1.87:1 fails) |
| Focus ring | `--lk-color-focus-ring` | ink · gold-500 on dark | 3 px ring, 2 px offset, every focusable element |
| Success | `--lk-color-success-solid` | green-700 | Approved, paid, complete, downloaded |
| Warning | gold-50 / gold-400 / gold-900 | tints only | Pending, expiring. Tints only, so warnings never read as buttons |
| Danger | `--lk-color-danger-solid` | danger-600 | Errors, rejection, destructive actions. Never maroon |
| Information | `--lk-color-info-solid` | info-600 | Links, neutral notices, help |
| Action needed | saffron-100 / saffron-900 | tint + deep text | Citizen must act — documents missing, payment due |
| Category accents | the four pillars | equal status | identity & documents = maroon · transport = saffron · payments = gold · agriculture = green |

### Contrast — measured, not estimated

WCAG 2.2: 4.5:1 body text · 3:1 large text and non-text UI.

| Pairing | Ratio | Verdict |
|---|---|---|
| Ink on white / canvas | 17.8 / 16.78 | AAA |
| **Ink on gold-500 — the primary button** | **9.54** | **AAA** |
| Ink on gold-600 (primary hover) | 7.14 | AAA |
| Ink on gold-700 (primary active) | 4.56 | AA |
| Gold-800 brand text on white | 6.39 | AA |
| Ink focus ring on canvas | 16.78 | AAA |
| Maroon-600 categorical text on canvas | 8.6 | AAA |
| Green-700 on white · white on green-700 | 8.37 | AAA |
| Link blue info-600 on white | 7.07 | AAA |
| Danger-600 on white | 5.66 | AA |
| Stone-600 secondary text on canvas | 5.37 | AA |
| Saffron-600 on white | 3.86 | Large text only |
| Saffron-700 on white (small text) | 5.36 | AA |
| White text on gold-500 | 1.87 | **Forbidden** |
| Gold-900 on gold-50 (warning text) | 9.72 | AAA |
| Dark: gold-500 button on `#1E1B18` | 9.18 | AAA |
| Dark: `#F5F2EC` on `#141210` | 16.72 | AAA |

**Three hard rules from the maths**

1. Gold never carries white or light text — every gold surface takes ink (9.54:1 on gold-500).
2. Saffron-600 may carry headlines and graphics, never body text — step down to saffron-700+.
3. The focus ring is ink on light surfaces and gold-500 on dark surfaces — gold alone on light fails 3:1.

### Usage proportion

A government screen is calm paper with deliberate colour: **~80%** stone neutrals & white · **~12%** unity gold actions and highlights · **~8%** pillars as equal category accents. **No single community pillar may visually dominate a screen** — if a layout starts reading maroon, saffron or green, rebalance it. Full-strength pillars appear together only in the mark and the national ribbon.

---

## 4. Typography

One harmonised superfamily across three scripts — open licensed (OFL), metrically compatible, excellent at small sizes on budget screens:

- Latin: **Noto Sans**
- Sinhala: **Noto Sans Sinhala**
- Tamil: **Noto Sans Tamil**
- Mono (code, reference numbers): **Noto Sans Mono**

### Type scale (Latin sizes; si/ta inherit size, gain line-height)

| Style | Size / line | Weight | Usage |
|---|---|---|---|
| Display 1 | 57 / 64 | 800 | Landing heroes only |
| Display 2 | 45 / 52 | 800 | Section heroes, campaigns |
| Heading 1 | 36 / 44 | 700 | Page titles — one per page |
| Heading 2 | 28 / 36 | 700 | Section titles |
| Heading 3 | 22 / 30 | 600 | Card titles, sub-sections |
| Heading 4 | 18 / 26 | 600 | List headers, field groups |
| Body large | 18 / 28 | 400 | Ledes, service descriptions |
| Body | 16 / 26 | 400 | Default. Never smaller for labels or legal text citizens must read |
| Body small | 14 / 22 | 400 | Secondary metadata, helper text |
| Caption | 12 / 18 | 500 | Timestamps, footnotes — sparingly |

### Rules for three scripts

- **Line height by script** — body leading: Latin 1.6 · **Sinhala 1.75** (stacked diacritics: combuva, papilla, hal kirīma) · **Tamil 1.7**. Apply via `:lang(si)` / `:lang(ta)`. Never clip ascenders in fixed-height containers.
- **No capitals, no italics** — Sinhala and Tamil have no case and no italic tradition. Never apply all-caps styling or synthetic italics to localised strings; emphasise with weight (600/700) or colour. Disable Latin letter-spacing tricks for si/ta.
- **Length expansion** — Sinhala and Tamil run 20–40% longer than English. Design every button, tab and nav label against the longest of the three translations. Truncating an official term is a defect.
- **Numerals, dates, currency** — Latin digits in all three locales. Currency: `Rs. 1,250.00` (LKR). Dates: `2026-06-13` in data; "13 June 2026 · 2026 ජූනි 13 · 13 ஜூன் 2026" in prose.

### Reference UI strings

| English | සිංහල | தமிழ் |
|---|---|---|
| Continue | ඉදිරියට යන්න | தொடரவும் |
| Apply now | දැන් අයදුම් කරන්න | இப்போது விண்ணப்பிக்கவும் |
| Birth certificate | උප්පැන්න සහතිකය | பிறப்புச் சான்றிதழ் |
| National Identity Card | ජාතික හැඳුනුම්පත | தேசிய அடையாள அட்டை |
| My profile | මගේ පැතිකඩ | எனது சுயவிவரம் |
| Search government services | රාජ්‍ය සේවා සොයන්න | அரசாங்க சேவைகளைத் தேடுங்கள் |

*Reference strings are illustrative; final terminology is ratified with the Department of Official Languages before release.*

---

## 5. Spacing & layout

4 px base grid; 8 px working rhythm. The reference device is a **budget Android at 360 px** — design mobile-first.

**Spacing scale (px):** 4 · 8 · 12 · 16 · 20 · 24 · 32 · 40 · 48 · 64 · 80 · 96
Defaults: 16 inside components · 24 between related blocks · 48–64 between page sections. When unsure, go one step larger — generosity reads as trustworthy.

**Breakpoints & grid**

| Token | Range | Columns | Margin | Typical device |
|---|---|---|---|---|
| base | 0–599 | 4 · gutter 16 | 16 | Budget Android (reference) |
| sm | 600–904 | 8 · gutter 24 | 32 | Large phones, small tablets |
| md | 905–1239 | 12 · gutter 24 | auto, max 840 content | Tablets, kiosk portrait |
| lg | 1240–1439 | 12 · gutter 32 | auto, max 1200 | Laptops, office desktops |
| xl | 1440+ | 12 · gutter 32 | auto, max 1200 | Counter-service monitors |

Reading measure: cap body text at **72ch**. Forms: **single column**, max 480 px field width — multi-column forms are prohibited (they collapse under trilingual labels and confuse tab order).

---

## 6. Shape & elevation

**Corner radius:** xs 4 (chips, tags) · sm 8 (compact inputs) · **md 12 (buttons, inputs — the workhorse)** · lg 16 (cards) · xl 24 (sheets, modals) · pill 999 (badges, search, language switcher) · circle (avatars, step dots).

**Elevation (warm ink-tinted shadows, shallow):**

| Level | Value | Use |
|---|---|---|
| 1 | `0 1px 2px rgba(28,27,24,.06), 0 1px 3px rgba(28,27,24,.08)` | Resting cards, list rows |
| 2 | `0 2px 6px rgba(28,27,24,.07), 0 4px 12px rgba(28,27,24,.08)` | Raised cards, sticky bars |
| 3 | `0 8px 24px rgba(28,27,24,.12)` | Toasts, menus, popovers |
| 4 | `0 16px 48px rgba(28,27,24,.16)` | Modals, bottom sheets |

**Motion:** 120 ms state changes · 200 ms standard · 320 ms sheets/modals · easing `cubic-bezier(0.2, 0, 0, 1)` · always honour `prefers-reduced-motion`.

---

## 7. Iconography

Outlined, rounded, optimistic. Base library: **Material Symbols Rounded**, extended with a custom national set (Grama Niladhari services, samurdhi, paddy land, tuk licensing, pilgrimage passes).

| Rule | Specification |
|---|---|
| Grid | 24 × 24 px keylines, 2 px live-area padding |
| Stroke | 2 px, rounded caps and joins |
| Style | Outlined at rest · filled for active/selected nav |
| Sizes | 20 dense · 24 default · 32 feature · 46 px tinted service tile (12 px radius) |
| Colour | Inherit text colour. Category tiles use the four pillars as **equal** tints |
| Accessibility | Never icon-only without a programmatic label; never icon-only for primary actions |

---

## 8. Components

All interactive elements: **48 px minimum touch target**, ink focus ring (gold on dark), labels authored in three languages.

### Buttons

| Variant | Anatomy | Rules |
|---|---|---|
| Primary | gold-500 fill · **ink label** · radius 12 · heights 56/48/40 | **One per view.** Hover gold-600, active gold-700 — label stays ink at every state |
| Secondary | 2 px ink border, transparent fill, ink label | Alternative actions beside a primary |
| Tertiary | ink label, underlined | Low-stakes actions, card footers |
| Danger | danger-600 fill, white label | Destructive only — always behind a confirmation |
| Disabled | stone-200 fill, stone-500 label | Keep visible; explain why nearby |
| Focus (all) | 3 px ink ring, 2 px offset (gold-500 on dark) | ≥3:1 on every approved surface |

Gold fill + ink text is the brand handshake — the same pairing as the Sewa spotlight card.

### Language switcher — the signature control

Pill group: සිංහල · தமிழ் · English (compact: සිං · த · EN). Present on every screen. Each language renders **in its own script**. Active language sits on a **gold pill with ink text**. Switching is instant, never resets the journey, persists across all government properties.

### Form fields

- Anatomy: label (16/600, never floats) → hint → control 56 px / radius 12 → error below.
- Borders: 1.5 px stone-400 rest · ink border + 3 px ink ring focus · 2 px danger-600 error.
- Errors say what happened **and how to fix it**, in the user's language; icon + text, never colour alone; never clear the citizen's input.
- One topic per page · mark *optional*, not required · autosave every step.

### Service card / quick action

46 px tinted icon tile (category pillar at 50-tint) + title + one-line context + chevron. Full-row tap target, radius 16, elevation 1 (hover 2). The core navigation unit of Sewa.

### Status badges — fixed national vocabulary

`Draft → Submitted → Pending → Action needed → Approved / Rejected`
Dot + tinted pill + deep text (AAA pairs). Ministries must not invent new status words.

### Notifications & alerts

| Type | Behaviour |
|---|---|
| Toast | Elevation 3, auto-dismiss 6 s (pause on hover/focus), `role="status"`. Success only — never errors |
| Inline alert | info / success / warning / danger tints; persistent until resolved; danger uses `role="alert"` |
| Push / SMS | Same string in-app, push and SMS. SMS fallback mandatory for status changes |

### Progress stepper

Done = green + check · current = **gold dot + ink number + gold halo** · remaining = stone. Used both for multi-step forms and for tracking submitted applications — government progress is visible, not a black box.

### Mobile shell (Sewa)

Sunrise header (gold gradient, ink text — 12.9:1 at its lightest) with trilingual greeting · search-first home · quick-action cards · 5-tab bottom nav with centre QR scan. Active tab: filled icon, ink label, gold indicator bar. Labels always visible — icon-only nav fails first-time users.

---

## 9. Patterns

### The service journey — five acts, every transactional service

1. **Start page** — what you'll get, what you'll need (documents listed up front), fee, processing time. One primary button.
2. **Identity** — sign in once via the national digital ID; never re-collect what government already knows. Assisted mode lets an officer act on a citizen's behalf, visibly logged.
3. **Form** — one topic per page · autosave · plain language · resume from SMS link on any device.
4. **Review & pay** — full summary with per-item edit links; itemised fees before payment; instant receipt number.
5. **Confirmation** — green panel, reference number in large type, what happens next + expected date, download/SMS receipt. Trackable in "My applications".

### Low-bandwidth & offline

- Page budget ≤ 500 KB including fonts (subset per script); images lazy-loaded; no decorative video.
- Drafts persist locally; submissions queue and retry; a dropped connection never loses work.
- Core journeys function without JavaScript; enhancement is progressive.
- Critical notifications mirror to SMS; key services define a USSD/counter equivalent.

### Errors & empty states

Error pages take responsibility, offer retry + path home + the **1919** Government Information Center line. Empty states explain what will appear and offer the first action.

---

## 10. Accessibility — non-negotiables (WCAG 2.2 AA mandatory)

| Requirement | Standard |
|---|---|
| Contrast | 4.5:1 body · 3:1 large text and UI — approved pairs only |
| Touch targets | ≥ 48 × 48 px, 8 px separation |
| Focus | 3 px ink ring, 2 px offset (gold-500 on dark). Never `outline: none` without replacement |
| Screen readers | Correct `lang` per string so TalkBack/NVDA switch voices; landmarks, labels, live regions |
| Keyboard | Full journeys keyboard-only; logical order; skip links; no traps |
| Reflow & zoom | Functional at 400% zoom / 320 px; text resizes 200% |
| Motion & time | `prefers-reduced-motion`; sessions warn before expiry, never expire mid-payment |
| Plain language | Grade-8 target in all three languages; sentences ≤ 25 words |
| Assisted use | Every flow operable by an officer on a citizen's behalf with explicit, logged consent |

---

## 11. Content & language

Voice: **a capable officer who respects your time** — warm, direct, never bureaucratic, never cute.

- Address the citizen as "you"; government is "we". Active voice.
- Verbs first on actions: "Apply now", "Download receipt", "Track application".
- No unexplained abbreviations; expand on first use — "Grama Niladhari (GN)".
- Honest about time: "Usually 3 working days" beats silence; if delayed, say so and why.

**Trilingual parity:** all three languages authored together at the same release; terminology follows the Department of Official Languages glossary; translations reviewed by native speakers **on the screen**, not in a spreadsheet; proper nouns keep native script beside Latin where space allows.

**Microcopy reference**

| Moment | Write this | Not this |
|---|---|---|
| Success | "Application submitted. Your reference: SLG-2026-118843. We'll SMS you within 3 working days." | "Your request has been successfully processed by the system." |
| Error, user-fixable | "Enter the 10-digit mobile number you use, starting 07." | "Invalid input." |
| Error, our fault | "Something went wrong on our side. Your draft is saved — try again in a few minutes, or call 1919." | "Error 500." |
| Fees | "Fee: Rs. 1,250.00 (includes postage)" | "Charges may apply as per gazette." |

---

## 12. Design tokens

Three layers — teams build against **semantic** only; core values may be tuned centrally without breaking products.

```css
/* layer 1 — core: the fact */
--lk-gold-500: #F0B41E;

/* layer 2 — semantic: the meaning (what teams use) */
--lk-color-action-primary: var(--lk-gold-500);
--lk-color-action-on-primary: var(--lk-ink);   /* never white on gold */

/* layer 3 — component: the application */
--lk-button-primary-bg: var(--lk-color-action-primary);

/* scripts get correct metrics via lang attributes */
:lang(si) { font-family: var(--lk-font-sinhala); line-height: 1.75; }
```

Naming: `--lk-{category}-{concept}-{variant}`. Dark theme ships as `[data-lk-theme="dark"]` — app-first, opt-in on web (primary stays gold-500 + ink, 9.18:1; focus ring becomes gold).

---

## 13. Governance & roadmap

| Mechanism | How it works |
|---|---|
| Ownership | Core systems team inside GovTech owns tokens, components, docs; cross-ministry design council reviews monthly |
| Versioning | SemVer. Patch = fixes · minor = additive · major = breaking, with 6-month migration windows |
| Contribution | Any ministry may propose a component with evidence of need in ≥ 2 services; core team generalises and ships for everyone |
| Compliance | Pre-release service assessment: tokens, WCAG 2.2 AA audit, trilingual review, page-weight budget, status-vocabulary check |
| Distribution | Figma libraries, npm web components, Flutter/Compose/SwiftUI packages — all generated from one token source |

**Roadmap**

1. **Foundation (now)** — ratify tokens, accessibility rules and trilingual type with GovTech + Dept. of Official Languages; publish Figma core library; pilot two Sewa journeys (birth certificate, vehicle licence).
2. **Components** — coded library (web + Flutter); migrate Sewa home, identity, payments; stand up the service assessment.
3. **Scale** — ministry portals; dark theme GA; national icon set; USSD/SMS content standards; public changelog.

---

## Changelog

**v1.1** — Unity Gold leads. Primary actions are gold-500 with ink text (9.54:1 AAA); no single community's colour leads the interface. Maroon, saffron and green become equal categorical pillars. Focus ring: ink on light, gold-500 on dark. Principles rewritten around the fixed philosophy — easy access · inclusivity · citizen first — plus "Progressive, modern, trusted."

**v1.0** — Initial draft: brand foundation from the Sewa mark, sampled palette, trilingual typography, token architecture, components, patterns, standards.

---

*එක ජාතියක්. එක යෙදුමක්. · ஒரு தேசம். ஒரு செயலி. · One Nation. One App.*
