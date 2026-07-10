# Fcitx5 macOS Themes

Two macOS-style Fcitx5 Classic UI themes:

- `mac-light`
- `mac-dark`

![Preview](assets/preview.png)

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

## Font used in preview

```ini
Font="PingFang Relaxed SC:style=Regular 16"
MenuFont="PingFang Relaxed SC:style=Regular 16"
TrayFont="PingFang Relaxed SC:style=Regular 16"
```

Font is not included.

## License

MIT
