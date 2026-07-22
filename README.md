# Codex AutoSkin Chiikawa — Summer Edition

一套可直接安装的 Chiikawa 夏日泳池 Codex 桌面主题。仓库已包含最终背景、配色、卡片头像和全部细节配置；安装后默认启用 `summer` 全屏主题，无需再手动制作素材。

> Unofficial fan-made theme. See [ASSET-NOTICE.md](ASSET-NOTICE.md) before redistributing the artwork.

## 主题效果

- 主标题：`Chiikawa 夏日泳池皮肤`
- 副标题：`Private Edition for HT`
- 右侧签名：`Lucky lucky ❤`
- 泳池全屏背景和右侧泳池壁构图
- 半透明玻璃卡片与四个 Chiikawa 头像徽章
- 夏日蓝色侧栏、标题栏、项目选择器和输入框
- 首页与对话页均有独立调校

运行时真正需要的主题文件只有：

```text
themes/summer/
├── art.png       # 最终泳池背景
├── theme.json    # 文案、配色、裁剪和透明度配置
└── extra.css     # 卡片头像、Logo 和精细界面样式
```

## macOS 安装

要求：已安装并至少打开过一次 Codex 桌面版。脚本会优先复用 Codex 自带的 Node.js。

```bash
git clone https://github.com/Jiaranbb/codex-autoskin-chiikawa.git
cd codex-autoskin-chiikawa
./scripts/autoskin-macos.sh install
```

也可以下载仓库 ZIP，解压后双击 `Install AutoSkin on macOS.command`。

如果 Codex 当时已经打开，按脚本提示允许重启，或安装后执行：

```bash
./scripts/autoskin-macos.sh start --restart-existing
```

## Windows 安装

要求：Windows 10/11、已打开并登录过 Microsoft Store 版 Codex，以及 Node.js 20 或更高版本。

```powershell
git clone https://github.com/Jiaranbb/codex-autoskin-chiikawa.git
cd codex-autoskin-chiikawa
.\quickstart.ps1
```

## 使用与验证

Summer 已设为仓库默认主题。需要重新切回 Summer 全屏版时：

```bash
node scripts/set-theme.mjs summer fullscreen
```

macOS 可执行完整验证并保存截图：

```bash
./scripts/verify-dream-skin.sh --screenshot "$PWD/summer-verify.png"
```

列出实际扫描到的主题：

```bash
node scripts/injector.mjs --themes
```

## 卸载与恢复

macOS：

```bash
./scripts/autoskin-macos.sh uninstall --restore-base-theme
```

或双击 `Uninstall AutoSkin on macOS.command`。

Windows：

```powershell
.\scripts\restore-dream-skin.ps1 -Uninstall -RestoreBaseTheme
```

AutoSkin 通过本机 Chromium DevTools Protocol 注入样式，不修改 Codex 官方应用包、签名或 `app.asar`。用户任务、登录状态和插件不会被替换。

## Credits

Theme packaging and Summer configuration: [Jiaranbb/codex-autoskin-chiikawa](https://github.com/Jiaranbb/codex-autoskin-chiikawa)

Based on the reversible AutoSkin engine from [Finderchangchang/codex-autoskin](https://github.com/Finderchangchang/codex-autoskin). Engine code is licensed under [MIT](LICENSE); theme artwork is governed separately by [ASSET-NOTICE.md](ASSET-NOTICE.md).

---

## English quick start

This repository packages a ready-to-install Chiikawa Summer pool theme for the Codex desktop app. The bundled `summer` theme is the default; no image preparation is required.

macOS:

```bash
git clone https://github.com/Jiaranbb/codex-autoskin-chiikawa.git
cd codex-autoskin-chiikawa
./scripts/autoskin-macos.sh install
```

Windows PowerShell:

```powershell
git clone https://github.com/Jiaranbb/codex-autoskin-chiikawa.git
cd codex-autoskin-chiikawa
.\quickstart.ps1
```

Please read [ASSET-NOTICE.md](ASSET-NOTICE.md) before public redistribution.
