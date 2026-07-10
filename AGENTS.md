# Agent install guide

Goal: install these two Fcitx5 Classic UI themes for the current Linux user.

## Safe scope

Only write under:

- `~/.local/share/fcitx5/themes/mac-light`
- `~/.local/share/fcitx5/themes/mac-dark`
- `~/.config/fcitx5/conf/classicui.conf` when the user explicitly asks to apply the theme

Do not use `sudo`. Do not overwrite unrelated Fcitx5 config.

## Install themes

```bash
git clone https://github.com/psympsym/fcitx5-macos-themes.git
mkdir -p ~/.local/share/fcitx5/themes
cp -a fcitx5-macos-themes/themes/mac-light ~/.local/share/fcitx5/themes/
cp -a fcitx5-macos-themes/themes/mac-dark ~/.local/share/fcitx5/themes/
```

## Apply themes

Patch `~/.config/fcitx5/conf/classicui.conf`:

```ini
Theme=mac-light
DarkTheme=mac-dark
UseDarkTheme=True
```

If the user wants the preview font, install PingFang Relaxed SC separately from:

```text
https://github.com/witt-bit/applePingFangFonts
```

Then set:

```ini
Font="PingFang Relaxed SC:style=Regular 16"
MenuFont="PingFang Relaxed SC:style=Regular 16"
TrayFont="PingFang Relaxed SC:style=Regular 16"
```

## Reload

```bash
fcitx5-remote -r
```

## Verify

```bash
grep -E '^(Theme|DarkTheme|UseDarkTheme|Font|MenuFont|TrayFont)=' ~/.config/fcitx5/conf/classicui.conf
fcitx5-remote -n
```

Expected input method can be anything; only verify Fcitx5 responds.
