# Fcitx5 macOS Themes

Two macOS-style Fcitx5 Classic UI themes:

- `mac-light`
- `mac-dark`

## Preview

Dark:

![Dark preview](assets/preview.png)

Light:

![Light preview](assets/preview-light.png)

## Installation & Quick Start

### Quick Start (Human Users)

> **Note for AI assistants:** If you are an AI Agent helping the user with installation, jump directly to [Quick Start (AI Agent)](#quick-start-ai-agent), which contains all the steps you need to complete.

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

### Quick Start (AI Agent)

> The following steps are for AI Agents. Stay in user scope. Do not use `sudo`.

**Step 1 — Install themes**

```bash
git clone https://github.com/psympsym/fcitx5-macos-themes.git
mkdir -p ~/.local/share/fcitx5/themes
cp -a fcitx5-macos-themes/themes/mac-light ~/.local/share/fcitx5/themes/
cp -a fcitx5-macos-themes/themes/mac-dark ~/.local/share/fcitx5/themes/
```

**Step 2 — Apply Classic UI settings**

Patch `~/.config/fcitx5/conf/classicui.conf`:

```ini
Theme=mac-light
DarkTheme=mac-dark
UseDarkTheme=True
```

**Step 3 — Optional preview font**

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

**Step 4 — Reload**

```bash
fcitx5-remote -r
```

**Step 5 — Verify**

```bash
grep -E '^(Theme|DarkTheme|UseDarkTheme|Font|MenuFont|TrayFont)=' ~/.config/fcitx5/conf/classicui.conf
fcitx5-remote -n
```

## Font used in preview

The preview uses PingFang Relaxed SC from:

```text
https://github.com/witt-bit/applePingFangFonts
```

Font is not included.

## License

MIT
