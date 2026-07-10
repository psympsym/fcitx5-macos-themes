# AGENTS.md

## Goal

Maintain two Fcitx5 Classic UI themes:

- `themes/mac-light`
- `themes/mac-dark`

Keep both themes visually in sync unless the change is explicitly light-only or dark-only.

## Safe Scope

Allowed paths:

- `themes/**`
- `assets/**`
- `README.md`
- `LICENSE`
- `AGENTS.md`

Do not modify the user's live Fcitx5 config from this repository task.
Do not use `sudo`.
Do not include fonts in this repo.

## Preview Assets

- `assets/preview.png` — dark theme preview
- `assets/preview-light.png` — light theme preview

If a theme visual changes, update the matching preview image.

## Theme Conventions

The highlight capsule is controlled by each theme's `highlight.svg`.
Current tuned geometry:

```xml
<rect width="41" height="40" x="-1" y="2" rx="10"/>
```

Keep light/dark geometry identical; only colors should differ.

## Verify

```bash
git diff --check
find themes -type f | sort
```

Manual verification requires copying themes into `~/.local/share/fcitx5/themes/` and reloading Fcitx5, but do that only when the user asks.
