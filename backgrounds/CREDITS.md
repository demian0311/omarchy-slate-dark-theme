# Slate Dark backgrounds

Eight wallpapers at 2560 × 1600. Every one is built from the **literal** Slate
palette — the eighteen values in `colors.toml` and on
<https://diagrammo.app/slate/> — with no tints, shades or interpolated
intermediates in the design. (The generated ones are line art, so their
rasterised edges carry antialiasing between a line's colour and the ground.)

Files are numbered because Omarchy picks a theme's default background by sort
order — `01-dunefield.png` is what you get on first apply, and `omarchy theme
bg next` walks the rest from there.

## Generated fields

No source image. Each defines a scalar or vector field over the frame and draws
something true about it, then rasterises straight from SVG.

| File | What it draws |
|------|---------------|
| `01-dunefield.png` | A fractal noise field contoured at close intervals, so the lines pack and thin the way wind ripples do. |
| `02-contour.png` | Level sets of four gaussian summits, tinted the way a hypsometric map is: blue in the basins, climbing through green and yellow to red on the tops. |
| `03-quasicrystal.png` | Seven plane waves at incommensurate angles, contoured. The pattern never repeats across the frame. |
| `04-flow.png` | Particles released into a noise field and traced until they leave the frame; hue follows where each one started. |
| `05-moire.png` | Three families of concentric rings at slightly different pitches. Everything visible between them is interference, not drawn. |
| `06-phyllotaxis.png` | Dots placed at the golden angle — the packing a sunflower head uses. Hue steps outward. |

Generator: `abstract.py` in the build tree (see the theme notes). Seeds are
fixed, so a rebuild reproduces these exactly.

## Posterised pictures

Photographs and paintings put through an OKLab posteriser: the source is
flattened, its lightness mapped into the theme's tonal range, and every pixel
snapped to the nearest literal palette value. The neutral ramp carries the
tonal structure; the nine categorical hues are spent only where the source is
genuinely saturated. These files contain palette values and nothing else.

| File | Source | Licence |
|------|--------|---------|
| `08-bierstadt.png` | Albert Bierstadt, *Looking Down Yosemite Valley, California* (1865) | Public domain — faithful reproduction via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Looking_Down_Yosemite-Valley.jpg) |
| `07-vestrahorn.png` | *Klifatindur / Vestrahorn, Stokksnes, Iceland* — Böhringer Friedrich (Wikimedia Commons user [Böhringer](https://commons.wikimedia.org/wiki/User:B%C3%B6hringer)) | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |

### Share-alike notice

`07-vestrahorn.png` is a derivative of a CC BY-SA 4.0 photograph, so it
carries the same terms: keep the attribution above with it, and redistribute
any further modification of that file under CC BY-SA 4.0. The other seven files
have no such obligation.
