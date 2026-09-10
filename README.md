# Slate Dark

An [Omarchy](https://omarchy.org/) theme. Colours in `colors.toml`, wallpapers
in `backgrounds/`.

Slate is a palette built to be read on a screen in a meeting — nine categorical
hues that stay distinct from one another, on a calm blue-grey ground. See
<https://diagrammo.app/slate/>. A light counterpart lives at
[omarchy-slate-light-theme](../../../omarchy-slate-light-theme).

## Install

    omarchy theme install https://github.com/REPLACE-ME/omarchy-slate-dark-theme.git

Then pick it from the theme menu, or:

    omarchy theme set slate-dark

## The backgrounds

Eight wallpapers at 2560 × 1600, every one built from the **literal** Slate
palette — the eighteen values in `colors.toml`, with no tints, shades or
interpolated intermediates in the design.

Six are generated fields: define a scalar or vector field over the frame, then
draw something true about it — its level sets, the paths through it, its
interference. Two are photographs and paintings put through a posteriser that
puts the tonal structure on the neutral ramp and spends the nine hues only where
the source is genuinely saturated.

Files are numbered because Omarchy picks a theme's default background by sort
order, so `01-dunefield.png` is what you get on first apply. `omarchy theme bg
next` walks the rest.

Sources, per-file licensing and the share-alike notice for `07-vestrahorn.png`
are in [`backgrounds/CREDITS.md`](backgrounds/CREDITS.md). Terms are in
[`LICENSE`](LICENSE) — MIT for the theme definition, CC BY 4.0 for the generated
backgrounds, and the source images' own terms for the two posterised ones.

## Updating

    omarchy theme update

That runs `git pull` on every git-installed theme. **It does not re-apply
them**, and Omarchy serves backgrounds from a staged copy under
`~/.local/state/omarchy/current/theme/`, so new or renamed wallpapers will not
appear until you also run:

    omarchy theme set slate-dark

## Editing

eagle holds the working copy at `~/src/omarchy-slate-dark-theme`, symlinked into
`~/.config/omarchy/themes/slate-dark`. The symlink is deliberate:
`omarchy theme extras` skips symlinked themes, so `omarchy theme update` won't
pull over uncommitted edits. Commit and push here, then `omarchy theme update`
on the other machines.

Any change here — backgrounds, `colors.toml`, anything — needs
`omarchy theme set slate-dark` afterwards to take effect, for the staging reason
above.

Keep this theme free of code-bearing files (`*.lua`, `alacritty.toml`,
`foot.ini`, `kitty.conf`, `ghostty.conf`, `vscode.json`) — Omarchy drops those
from cloned themes and regenerates them from `colors.toml`. Per-app overrides
belong in `~/.config/omarchy/themed/<name>.tpl` instead. This theme ships none
of them, so it installs byte-for-byte.
