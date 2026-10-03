<!--
THESIS: A dark-first, light-capable studio surface where a recruiter scans proof of craft in one vertical pass; refuses the neon-portfolio rut by making green→mint→cyan a precise signal layer over near-black studio surfaces.
OWN-WORLD: Layered near-black surfaces (#040605 → #1C201F), hairline rgba(255,255,255,.08) borders, green/mint/cyan as the only chromatic roles, General Sans + Inter fallback, radius 12/18/24/999, 250ms motion, fade+slide-up reveals, soft green glow reserved for the hero.
STORY: The visitor knows in seconds who Alejandro is (Ingeniero en Ciencias Informáticas, full-stack frontend-first), believes it from the system's restraint and the shipped projects, and acts: downloads the CV or writes via the contact form.
FIRST VIEWPORT: Full-viewport hero: availability pill, oversized name, role + one-line pitch, primary gradient CTA (Contáctame) + secondary (Descargar CV), soft green radial glow, abstract avatar right of the text; transparent nav that gains blur + hairline border on scroll.
FORM: The brief-pinned direction (Arounda/Linear/Vercel/Raycast/Stripe/Apple register); no concept roll. Light mode is a derived daylight variant of the same world that preserves the existing ThemeToggle + localStorage behavior.
-->

# Design — alex.dev (Alejandro Yero)

<!-- impeccable:design-schema 1 -->

## Mode

**Experience** (portfolio/showcase), with a Persuade reflex on the first viewport: the artifact must lead, but the visitor still needs a clear action (CV download, contact) within seconds.

## Visual World

Dark-first studio system inspired by Arounda, Linear, Vercel, Raycast, Stripe and Apple: generous whitespace, hairline borders, soft rounded corners, restrained gradients, large type, clean components. Green→mint→cyan is the single chromatic family; it carries the brand signal and appears nowhere as decoration.

Color strategy: **Committed** — one saturated family (green/mint/cyan) carries the brand over near-black (dark) or warm-white (light) studio neutrals. Gradients are reserved for the primary action and the hero presence, never scattered across headings.

## Tokens

### Dark (default, first)

| Role | Value |
|---|---|
| Background | `#040605` |
| Background secondary | `#0B0F0E` |
| Surface | `#151917` |
| Card | `#1C201F` |
| Border | `rgba(255,255,255,0.08)` |
| Primary green | `#169A50` |
| Accent mint | `#55D396` |
| Cyan accent | `#00D4C4` |
| Dark emerald | `#0F3D2E` |
| Text primary | `rgba(255,255,255,0.95)` |
| Text secondary | `rgba(255,255,255,0.65)` |
| Text muted | `rgba(255,255,255,0.45)` |
| Disabled | `rgba(255,255,255,0.25)` |

### Light (derived daylight variant)

The same world under light: warm-white neutrals replace the near-black scale, the green family keeps its hue roles, and text alphas flip to dark ink. Contrast must hold AA (≥4.5:1 body, ≥3:1 large text).

| Role | Value (starting point, settle after build) |
|---|---|
| Background | `#F7F8F6` |
| Background secondary | `#EEF1EE` |
| Surface | `#FFFFFF` |
| Card | `#FFFFFF` |
| Border | `rgba(4,6,5,0.10)` |
| Primary green | `#0F7A3F` (hover `#0C6B36`) |
| Text primary | `rgba(4,6,5,0.95)` |
| Text secondary | `rgba(4,6,5,0.85)` |
| Text muted | `#587663` (green-tinted ink; plain alpha fails 4.5:1 on `#F7F8F6`) |

## Gradients

- **Principal:** `linear-gradient(135deg, #040605 0%, #169A50 45%, #55D396 75%, #00D4C4 100%)` — brand moments only (hero presence, signature strokes).
- **Glow:** `radial-gradient(circle, rgba(85,211,150,.25), transparent 70%)` — hero background only.
- **Button:** `linear-gradient(90deg, #169A50, #55D396)` — primary action only.

## Typography

- **Family:** General Sans (Fontshare) with `Inter, system-ui, sans-serif` fallback.
- **Weights:** 300, 400, 500, 600, 700.
- **Scale:** Hero 72px / Title 48px / Subtitle 28px / Section title 20px / Body 16px / Small 14px / Caption 12px. Display max 6rem, tracking floor -0.04em.
- Body measure 65–75ch. More space above a heading than below it.

## Radii / Shadows

- Radius: small 12px, medium 18px, large 24px, pill 999px.
- Card: `0 10px 30px rgba(0,0,0,.25)`; Glow: `0 0 50px rgba(85,211,150,.20)`; Hover: `0 15px 40px rgba(0,0,0,.35)`.

## Components

- **Buttons:** primary gradient `#169A50→#55D396` with dark ink text `#05251A` (white text measures ~2.6:1 mid-gradient; ink holds ≥4.5:1), radius 16px, padding 16px 28px; secondary transparent with `rgba(255,255,255,.12)` border (light: `rgba(4,6,5,.18)`), hover `rgba(255,255,255,.05)`. Hover/focus/active states, AA contrast, keyboard focus visible.
- **Brand icons:** always rendered monochrome via `currentColor` (`.icon-mono` utility) so the green/mint/cyan family stays the only chromatic role; raw brand hex is never shipped.
- **Cards:** `#151917`, 1px `rgba(255,255,255,.08)` border, radius 24px, padding 32px, hover lift + very subtle green glow, 250ms transition.
- **Navigation:** transparent; on scroll → blur background, semi-transparent black bg, very subtle bottom border.
- **Hero:** near-full viewport; availability pill, oversized name, role, CTA pair, green glow, illustration.
- **Sections:** wide vertical spacing, alternating backgrounds, smooth gradients. Order: Hero, Sobre mí, Tecnologías, Experiencia, Proyectos, Contacto.
- **Icons:** outline (Lucide / Heroicons register), never heavy filled glyphs.

## Motion

- Duration 250ms; hover `scale(1.02)`; cards `translateY(-4px)`; buttons smooth color change; appearance fade + slide up; smooth scroll.
- One authored entrance moment in the hero; section reveals share one quiet system, never a different animation per section.
- Respect `prefers-reduced-motion`: disable reveal/motion, keep content visible by default.

## Responsive

Desktop-first. Breakpoints: 1536 / 1280 / 1024 / 768 / 480. The layout must stay clean and uncluttered on mobile (stack hero, shrink type scale, keep CTAs full-width tappable).

## Accessibility

WCAG 2.1 AA as the floor: contrast on body and placeholders ≥4.5:1 (large ≥3:1), visible hover/focus/active on every control, keyboard navigation, reduced-motion respected. On colored surfaces, tint secondary text from that hue or the foreground — never gray.
