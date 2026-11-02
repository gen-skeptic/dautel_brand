# Dautel brand

Brand identity and design system for **Dautel Intelligent Operations**: a professional dark operator aesthetic with one-pixel topology lines, monospace interface text and Catppuccin color themes.

Everything lives in [`Dautel_style/`](Dautel_style/). Start with [`Dautel_style/BRAND.md`](Dautel_style/BRAND.md).

| Path | What |
| --- | --- |
| [`BRAND.md`](Dautel_style/BRAND.md) | Brand rules: identity, voice, color, type, shape, motion, icons, components |
| [`dautel.css`](Dautel_style/dautel.css) | Drop-in stylesheet: five themes, fonts, base styles and components |
| [`index.html`](Dautel_style/index.html) | Example page using the stylesheet, logo and favicon |
| [`logos/`](Dautel_style/logos/) | Canonical Terminal Monogram logo, mark and favicon (SVG) |
| [`fonts/install/`](Dautel_style/fonts/install/) | JetBrainsMono Nerd Font, 16 styles, to install on your computer |
| [`fonts/web/`](Dautel_style/fonts/web/) | Manrope and JetBrains Mono web fonts plus `fonts.css`, for offline projects |

## Use it in a project

1. Copy `Dautel_style/dautel.css` into the project and load it once:

   ```html
   <link rel="stylesheet" href="dautel.css">
   ```

2. Pick a theme on the root element: `mocha` (default), `macchiato`, `frappe`, `latte` or `dautel` (the original dautel.io palette).

   ```html
   <html data-theme="mocha">
   ```

3. Style with the CSS variables (`var(--ink)`, `var(--text)`, `var(--blue)`…), the type classes (`.display`, `.lead`, `.section-title`…) and the component classes (`.button-primary`, `.section-heading`, `.panel-cut`…). Never hard-code colors or fonts.

4. Copy the logo files you need from `logos/`. Their alt text is `Dautel Intelligent Operations`.

For offline use, also copy `fonts/web/` and load `fonts/web/fonts.css` before `dautel.css`.

## Brand at a glance

- **Fonts:** JetBrainsMono Nerd Font for interface text, labels and headings; Manrope for prose.
- **Colors:** Catppuccin Mocha by default. Blue is the primary action and focus color, green (mint) means live or healthy, mauve (lavender) marks Operations, and peach is for contact actions only.
- **Shape:** small radii, 12px clipped corners, 1px hairlines, no shadows, gradients or glow.

## Source

Extracted from [gen-skeptic/dautel.io](https://github.com/gen-skeptic/dautel.io) (`apps/dautel-io/src/styles.css`, `docs/BRAND.md`, `design/DESIGN_SPEC.md`). The online version of this design system is at https://claude.ai/artifact/TbPoRVLANSdVx3SujjkpTC.

## Licenses

The fonts are under the SIL Open Font License 1.1 (see `Dautel_style/fonts/install/JetBrainsMono-NerdFont/OFL.txt` and `Dautel_style/fonts/web/LICENSE-*.txt`). The logos are the property of Dautel Intelligent Operations.
