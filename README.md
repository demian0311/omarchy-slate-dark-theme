# Slate Dark

An Omarchy theme. Colors in `colors.toml`, wallpapers in `backgrounds/`.

## Install on another machine

    omarchy theme install ssh://anchor/home/demian/git/omarchy-slate-dark-theme.git

On anchor itself, use the local path instead — it can't SSH to itself:

    omarchy theme install /home/demian/git/omarchy-slate-dark-theme.git

## Update everywhere

    omarchy theme update    # pulls every git-installed theme

## Editing

eagle holds the working copy at `~/src/omarchy-slate-dark-theme`, symlinked into
`~/.config/omarchy/themes/slate-dark`. The symlink is deliberate: `omarchy theme extras`
skips symlinked themes, so `omarchy theme update` won't pull over uncommitted
edits. Commit and push here, then `omarchy theme update` on the other machines.

Keep this theme free of code-bearing files (`*.lua`, `alacritty.toml`,
`foot.ini`, `kitty.conf`, `ghostty.conf`, `vscode.json`) — Omarchy drops those
from cloned themes and regenerates them from `colors.toml`. Per-app overrides
belong in `~/.config/omarchy/themed/<name>.tpl` instead.
