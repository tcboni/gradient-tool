# Gradient Tool

A lightweight CSS gradient workbench.

**[→ Open Gradient Tool](https://tcboni.github.io/gradient-tool/)**

## Features

- **All gradient types** — `linear`, `radial`, `conic`, plus their `repeating-*` variants
- **Multiple stacked layers** with per-layer blend modes (`background-blend-mode`), visibility toggles, reordering, and duplication
- **Full color-stop editing** — draggable handles on the track, click-to-add with sampled color, per-stop opacity, and draggable **midpoint hints** (the `%`-only entries between stops)
- **Color interpolation spaces** — `in oklch`, `oklab`, `srgb`, `lab`, `lch`, `hsl`, `hwb`… with `shorter`/`longer`/`increasing`/`decreasing` hue paths
- **Geometry controls** — rotary angle dial for linear/conic, radial shape/size (keywords or custom), and a draggable crosshair on the preview for radial/conic centers
- **Tiling patterns** — per-layer `background-size` unlocks checkerboards, polka dots, stripes (see the presets)
- **Effects rack** — film grain (inline SVG `feTurbulence` layer), vignette, hue shift / saturation / brightness (`filter:`), all emitted as part of the CSS
- **Animations** — rotate (`@property` angle spin), pan (seamless forward scroll — one full period of a 200%-sized background), and hue cycle; independently toggleable and combinable, each with its own speed, all emitted as ready-to-paste `@keyframes`
- **Preview modes** — fill, gradient **text** (editable, greets you in a random language), and gradient **border**; pickable background color for judging transparency
- **Live favicon** — the browser-tab icon re-renders to match whatever gradient you're editing
- **Output formats** — colors as hex, `rgb()`, `hsl()`, or `oklch()`
- **Import** — paste any existing gradient (or a whole `background:` rule, stacked layers included) and keep editing it
- **Export** — copy CSS, download PNG (canvas render) or SVG (linear/radial layers)
- **Share links** — the whole state serializes into the URL hash
- **Presets & random** — curated presets plus a harmonious randomizer (OKLCH-based)
- **Quality of life** — undo/redo, autosave to `localStorage`, keyboard-accessible controls, pure-CSS tooltips (anchor positioning), responsive layout

## Keyboard

| Key                                                | Action                                                                   |
| -------------------------------------------------- | ------------------------------------------------------------------------ |
| <kbd>⌘/Ctrl</kbd>+<kbd>Z</kbd> / +<kbd>Shift</kbd> | Undo / redo                                                              |
| <kbd>R</kbd>                                       | Random gradient                                                          |
| <kbd>C</kbd>                                       | Copy CSS                                                                 |
| <kbd>←</kbd> <kbd>→</kbd>                          | Nudge focused stop, dial, or crosshair (<kbd>Shift</kbd> = bigger steps) |
| <kbd>Delete</kbd>                                  | Remove focused stop                                                      |

## Notes

- PNG/SVG exports interpolate in sRGB, so exotic interpolation spaces are approximated; the CSS output is always exact.
- SVG has no conic gradients, so conic layers are skipped in SVG export.
