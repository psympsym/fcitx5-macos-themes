# Fcitx5 macOS 主题

[中文版](./README.zh.md) | [English](./README.md)

两个 macOS 风格的 Fcitx5 Classic UI 主题：

- `mac-dark`
- `mac-light`

## 预览

浅色：

![浅色预览](assets/preview-light.png)

深色：

![深色预览](assets/preview.png)

## 安装与快速开始

### 快速开始（人类用户）

> **给 AI 助手的提示：** 如果你是正在帮助用户安装的 AI Agent，请直接跳到 [快速开始（AI Agent）](#快速开始ai-agent)，那里包含你需要执行的全部步骤。

```bash
git clone https://github.com/psympsym/fcitx5-macos-themes.git
mkdir -p ~/.local/share/fcitx5/themes
cp -a fcitx5-macos-themes/themes/mac-light ~/.local/share/fcitx5/themes/
cp -a fcitx5-macos-themes/themes/mac-dark ~/.local/share/fcitx5/themes/
fcitx5-remote -r
```

然后设置 Fcitx5 Classic UI：

```ini
Theme=mac-light
DarkTheme=mac-dark
UseDarkTheme=True
```

### 快速开始（AI Agent）

> 以下步骤给 AI Agent 使用。保持用户级安装。不要使用 `sudo`。

**步骤 1 — 安装主题**

```bash
git clone https://github.com/psympsym/fcitx5-macos-themes.git
mkdir -p ~/.local/share/fcitx5/themes
cp -a fcitx5-macos-themes/themes/mac-light ~/.local/share/fcitx5/themes/
cp -a fcitx5-macos-themes/themes/mac-dark ~/.local/share/fcitx5/themes/
```

**步骤 2 — 应用 Classic UI 设置**

修改 `~/.config/fcitx5/conf/classicui.conf`：

```ini
Theme=mac-light
DarkTheme=mac-dark
UseDarkTheme=True
```

**步骤 3 — 可选预览字体**

如果用户想使用预览图里的字体，请从下面仓库单独安装 PingFang Relaxed SC：

```text
https://github.com/witt-bit/applePingFangFonts
```

然后设置：

```ini
Font="PingFang Relaxed SC:style=Regular 16"
MenuFont="PingFang Relaxed SC:style=Regular 16"
TrayFont="PingFang Relaxed SC:style=Regular 16"
```

**步骤 4 — 重载**

```bash
fcitx5-remote -r
```

**步骤 5 — 验证**

```bash
grep -E '^(Theme|DarkTheme|UseDarkTheme|Font|MenuFont|TrayFont)=' ~/.config/fcitx5/conf/classicui.conf
fcitx5-remote -n
```

## 预览使用字体

预览图使用 PingFang Relaxed SC，来源：

```text
https://github.com/witt-bit/applePingFangFonts
```

字体不包含在本仓库中。

## 许可证

MIT
