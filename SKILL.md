---
name: codex-autoskin-chiikawa
description: Install, launch, verify, repair, or remove the bundled Chiikawa Summer skin for the Windows or macOS Codex desktop app.
metadata:
  version: "1.0.0"
---

# Chiikawa Summer AutoSkin

Use this repository as a ready-made family distribution. Do not generate a new theme or replace the bundled Summer artwork during a normal install.

## Install

- macOS: run `scripts/autoskin-macos.sh install`. The Finder entry point is `Install AutoSkin on macOS.command`.
- Windows: run `quickstart.ps1` from PowerShell.
- Keep automatic recovery enabled. It is required to restore the skin after an ordinary Codex restart.
- Restart an already-open Codex only when the user authorizes it.

## Verify and repair

- macOS: run `scripts/verify-dream-skin.sh`; repair by rerunning `scripts/autoskin-macos.sh install`.
- Windows: run `scripts/verify-dream-skin.ps1`; repair by rerunning `quickstart.ps1`.
- A successful result must report theme `summer`, layout `fullscreen`, and a passing main renderer.

## Remove

- macOS: run `scripts/autoskin-macos.sh uninstall` or use `Uninstall AutoSkin on macOS.command`.
- Windows: run `scripts/restore-dream-skin.ps1 -Uninstall -RestoreBaseTheme`.

## Safety

- Never modify, replace, patch, re-sign, or take ownership of the official Codex/ChatGPT app bundle, `WindowsApps`, or `app.asar`.
- Preserve user tasks, authentication, plugins, pets, and the official executable.
- Keep the loopback CDP injector and single-instance recovery watcher paired with the remembered port.
- The only bundled public theme is `themes/summer`.
