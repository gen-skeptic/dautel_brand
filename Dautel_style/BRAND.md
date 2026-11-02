# Dautel Design System — brand rules

A professional dark operator aesthetic for **Dautel Intelligent Operations** — the public site `dautel.io` and the private portal `dautel.cloud` share it exactly. Technical, observable, under control: one-pixel topology lines on deep ink, monospace interface, three quiet accent hues.

## Using this system in a new project

Apply this brand to every new site, app or page unless told otherwise.

1. Copy `dautel.css` (in this folder) into the project and load it once (`<link rel="stylesheet" href="dautel.css">`, or `import "./dautel.css"` in a bundler). It holds every token for all five themes, the fonts, base page styling and the component classes.
2. Default to Catppuccin Mocha. Set `<html data-theme="…">` to `mocha`, `macchiato`, `frappe`, `latte` or `dautel` to switch.
3. Use the role variables (`var(--ink)`, `var(--text)`, `var(--blue)`…) and the type classes (`.display`, `.lead`, `.section-title`, `.label`, `.micro`…) — never hard-coded hex values or other fonts.
4. Build with the component classes: `.button.button-primary|secondary|small|contact`, `.section-heading` (with the `>_` span), `.panel`, `.panel-cut`, `.topology-node`, `.topology-status`, `.contact-form`, `.dot-grid`, `.container`.
5. Tailwind projects: map the theme's colors to the same variables (`colors: { ink: "var(--ink)", text: "var(--text)", blue: "var(--blue)", … }`) and keep `dautel.css` loaded.
6. For a Dautel-branded product, use the Logos assets; for anything else, keep the visual system and set the product's name in `mono` without the Dautel mark.
7. `index.html` (in this folder) is a minimal page showing the setup, with the logo and favicon.
8. Offline or no Google Fonts: also copy `fonts/web/` into the project and load `fonts/web/fonts.css` before `dautel.css`; then delete the `@import` line at the top of the project's copy of `dautel.css`.

## Identity

- The company is **Dautel Intelligent Operations**; **DAUTEL** is the wordmark; **dautel.io** the domain. Accessible name of the logo: `Dautel Intelligent Operations`.
- The logo is the **Terminal Monogram**: an angular `D` in `blue` containing the `>_` prompt, with a `mint` operational-status point. The lockup adds a `text` DAUTEL wordmark, a deliberately bold `lavender` INTELLIGENT OPERATIONS descriptor and divider, and a `mint` dautel.io domain.
- Use the files in `logos/` as-is: `dautel-intelligent-operations-logo.svg` (horizontal lockup), `dautel-intelligent-operations-mark.svg` (standalone mark), `favicon.svg` (browser icon). Copy the ones you need into the project; reference them with `<img>` and alt text `Dautel Intelligent Operations`. The SVG is canonical, never the raster concept.
- Place the logo on `ink` or another approved dark surface. Clear space ≥ ¼ of the mark's width. Lockup at **220px wide or larger**; the standalone mark at **24px or larger**.
- Never stretch, rotate, outline, add gradients or glow, recolor parts, rearrange elements, or place it over a busy image.

## Content fundamentals

- Plain, confident, first person singular for the practitioner (“I design practical agent workflows…”), imperative for actions (“Explore the work”, “Discuss a project”).
- Sentence case for headlines and buttons; UPPERCASE only inside the logo descriptor.
- Section titles are short noun phrases prefixed with the terminal prompt: `>_ Selected systems`.
- First-viewport vocabulary: *Work · Experience · Ask AI · Contact · Discuss a project · Agents · Infrastructure · Operations*.
- No emoji, no fake metrics, no decorative status theater. Status shown must be real.
- Privacy lock: never publish a street address, personal phone, personal email or a resume with contact details.

## Color

- Five themes share one set of role names: **Catppuccin Mocha** (default), **Macchiato**, **Frappé**, **Latte** (light), and **Dautel Original** — the codebase's exact palette. Build against role tokens, never flavor hex values, so a theme switch is a `data-theme` change.
- Catppuccin mapping: `ink` base · `ink-soft` mantle · `surface` crust · `surface-strong` surface0 · `surface-hover` surface1 · `text` text · `muted` subtext0 (Latte subtext1) · `quiet` overlay1 (Latte overlay2) · `rule` surface1 · `blue` blue · `mint` green · `lavender` mauve · `peach` peach · `danger` red.
- Ground every page in `ink`; alternate bands in `ink-soft`; raise panels to `surface`, then `surface-strong`; hover with `surface-hover`.
- Text in `text`; secondary prose and labels in `muted`. Keep `quiet` for icons and large text — it sits just under 4.5:1 on `ink` in every theme. `surface-hover` is a transient fill; don't park `muted` text on it.
- Accents carry meaning, one per element:
  - `blue` — primary action, the `>_` prefix, focus, Agents.
  - `mint` — live/healthy status, secondary action, success, Infrastructure.
  - `lavender` — the descriptor, Operations.
  - `peach` — contact actions only.
  - `danger` — errors, always with a word.
- Filled accent buttons put `on-accent` text on the accent (crust in the dark flavors, ≥6.5:1).
- **Latte caveat:** Catppuccin Latte's green and peach are under 3:1 on its base, so in Latte they work only as fills, outlines and icons beside words in `text`; Latte blue is 4.34:1, fine for large text and focus rings.
- The logo SVGs keep their fixed Dautel inks in every theme. They read on all dark flavors; on Latte, place them on a `surface-strong` or Dautel `ink` panel.
- `rule` draws every hairline and field border; `rule-soft` draws the 80px page grid. Neither is strong enough to be a control's only boundary — keep the label and the `blue` focus ring.

## Type

- Two families: **Manrope** (`sans`) for prose; **JetBrainsMono Nerd Font** (`mono`) for navigation, controls, labels, diagrams and short headings. The Nerd Font is the preferred face (it adds the powerline/devicon glyphs); install it from `fonts/install/JetBrainsMono-NerdFont/` (`JetBrainsMono Nerd Font` / `JetBrainsMono NF`). The stack falls back to plain JetBrains Mono from Google Fonts / Fontsource, which has the same letterforms but no icon glyphs, so don't rely on Nerd glyphs for meaning on the web.
- `display` is the hero headline only — Manrope 650, tight `-0.062em`, leading .98. An emphasised phrase inside it switches to `mono` at .88em in `blue`.
- `section-title` (mono 620) always starts with a `blue` `>_` at .72em.
- `lead` and `body` run at 1.7 line height in `muted` / `text`.
- UI sizes: `nav` 16px/620, `button` 13.28px/560, `field` 13.12px, `label` 12px, `micro` 11.52px.

## Shape, space and structure

- Small radii only: `radius-xs` fields, `radius-sm` buttons and status lines, `radius-md` icon tiles. `radius-dot` is for status dots. **No pills.**
- Feature panels and topology nodes use a clipped corner of `corner-cut` (12px chamfer) instead of rounding.
- Every line is `stroke-hairline` (1px). Topology lines connect nodes with 7px square terminals.
- Patterns are drawn, never washed: a 1px dot grid (24px pitch in the topology, 18px in the hero corner) and the 80px line grid. CSS gradient functions are used only to draw these grids — no color washes, glassmorphism, neon glow or bento-grid defaults.
- Content max width `content-width` (1500px); page gutter `clamp(space-row, 4vw, page-gutter-max)`.
- No shadows.

## Motion and states

- Transitions 160ms ease on color, background, border and a 1–2px lift (`translateY(-2px)` on buttons, `-1px` on nav).
- Buttons invert on hover: filled → outline, outline → filled.
- Focus: `stroke-focus` solid `blue` outline, 4px offset, on every interactive element.
- Motion is limited to line tracing, small reveals and state changes; `prefers-reduced-motion` disables it.

## Iconography

- **Lucide** SVG icons, `stroke-icon` (1.6px), color inherited from the accent of their row. Not included in this folder — install `lucide` (or `lucide-react`) from npm in the project.
- The `>_` prompt glyph is typographic, set in `mono`.
- Status is an 8px `mint` dot (`radius-dot`), or the 2px-bar signal meter.

## Components

The components are the dautel.io site's own markup, included in `dautel.css`. Use the same class names in code: `.button.button-primary`, `.section-heading`, `.topology-node`, `.topology-status`, `.contact-form`.
