# CSS Tooltip Library

A library of **pure-CSS tooltips** in 8 directions with fade and slide reveals — no JavaScript, no dependencies. Click any tooltip to view and copy its CSS.

Built with [Astro](https://astro.build).

## Features

- **Pure CSS** — one element, two pseudo-elements (`::before` arrow, `::after` bubble). No JavaScript required.
- **8 directions** — top, bottom, left, right, and the four corners.
- **Fade & slide reveals** — animated on hover and keyboard focus.
- **Single source of text** — the tooltip content lives in a `data-tip` attribute.
- **One-token theming** — recolour any tooltip by overriding the `--tip-bg` CSS custom property.
- **Accessible** — respects `prefers-reduced-motion`.
- **Copy & paste** — grab the self-contained CSS for any tooltip, or a ready-made prompt to have a coding agent recreate it.

## Usage

Every tooltip is built from a shared `.tip` base plus one direction/reveal modifier class. The bubble text comes from the `data-tip` attribute:

```html
<button class="tip tp-1" data-tip="Copy to clipboard">Hover me</button>
```

Recolour with a single token:

```css
.tip {
  --tip-bg: #6d28d9; /* bubble + arrow */
  --tip-fg: #ffffff; /* bubble text */
}
```

## Development

```bash
npm install      # install dependencies
npm run dev      # start the dev server (http://localhost:4321)
npm run build    # build for production into dist/
npm run preview  # preview the production build locally
```

## Project structure

```
src/
  data/tooltips.ts          # tooltip definitions + derived live CSS and copy snippets
  layouts/Layout.astro      # base HTML layout
  pages/index.astro         # the tooltip gallery
  pages/tooltip-data.json.ts# JSON endpoint for the copy modal
  styles/global.css         # site styling
public/fonts/               # self-hosted fonts
```

## License

[MIT](LICENSE) © Csaba Kissi
