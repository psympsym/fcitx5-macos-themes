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

## AI agents

This repository is small and file-based. AI coding agents should follow [`AGENTS.md`](AGENTS.md) when editing or packaging the themes.

To install with an AI agent, paste the normal install commands above and ask it to apply the Fcitx5 Classic UI settings. Fonts are separate; see below.

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
