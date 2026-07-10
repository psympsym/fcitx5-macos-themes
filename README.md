# Fcitx5 macOS Themes

Two macOS-style Fcitx5 Classic UI themes:

- `mac-light`
- `mac-dark`

## Preview

Dark:

![Dark preview](assets/preview.png)

Light:

![Light preview](assets/preview-light.png)

## Install

```bash
git clone https://github.com/psympsym/fcitx5-macos-themes.git
mkdir -p ~/.local/share/fcitx5/themes
cp -a fcitx5-macos-themes/themes/mac-light ~/.local/share/fcitx5/themes/
cp -a fcitx5-macos-themes/themes/mac-dark ~/.local/share/fcitx5/themes/
fcitx5-remote -r
```

Then set Fcitx5 Classic UI:

```ini
Theme=mac-light
DarkTheme=mac-dark
UseDarkTheme=True
```

## Install with your AI agent

Tell your agent:

> Install `https://github.com/psympsym/fcitx5-macos-themes` for Fcitx5 Classic UI. Follow `AGENTS.md`. Apply `mac-light` and `mac-dark`. Do not use sudo.

This repo includes [`AGENTS.md`](AGENTS.md) for agent-safe installation.

## Font used in preview

The preview uses PingFang Relaxed SC from:

```text
https://github.com/witt-bit/applePingFangFonts
```

Font config:

```ini
Font="PingFang Relaxed SC:style=Regular 16"
MenuFont="PingFang Relaxed SC:style=Regular 16"
TrayFont="PingFang Relaxed SC:style=Regular 16"
```

Font is not included.

## License

MIT
