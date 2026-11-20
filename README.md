# AgentHub: installers

AgentHub is a desktop app that runs many [Claude Code](https://docs.anthropic.com/en/docs/claude-code) sessions side by side, each in a real terminal tab, coordinated by a single **master** agent. You talk to the master; it opens tabs, splits work across your projects, forwards requests and tells you when something needs you. You can also type into any tab directly. Every session runs the official `claude` CLI on your own Claude subscription.

Highlights: spaces, projects, groups and tabs; pending questions in one place; notifications; per-project memory and wiki (optionally shared through the project's git repo); history of finished tabs you can resume; remote projects over SSH; an optional phone page to answer the master; per-tab diffs and token usage; agents answer in your OS language or the one you pick.

This repository only holds the installers and the auto-update feed (`latest.json`). The source code is private.

## Requirements

- The Claude Code CLI (`claude`) installed and logged in.
- Windows: [Git for Windows](https://git-scm.com/download/win) (tabs run in Git Bash).

## Install

1. Open the [latest release](https://github.com/andrewmautone/agenthub-releases/releases/latest).
2. Download the file for your system:
   - **Windows**: `AgentHub_<version>_x64-setup.exe`, then run it. It does not ask for admin rights: it installs for your user only.
   - **macOS** (Apple Silicon and Intel): `AgentHub_<version>_universal.dmg`, open it and drag AgentHub to Applications.

Windows SmartScreen may warn that the installer is not recognized, because it has no Microsoft code signature. Click **More info > Run anyway**.

The macOS build is not notarized by Apple. The first time, macOS may refuse to open it: go to **System Settings > Privacy & Security** and click **Open Anyway** (or right-click the app and choose **Open**).

## Updates

AgentHub checks for new versions when it opens and every 6 hours. You can also check in **Settings > Updates**. Nothing is installed without your confirmation, because updating restarts the app and closes all tabs.

Packages are signed (minisign/Tauri). The app only installs an update if its signature matches the public key built into it.

Some releases ship for one platform only. Auto-update on macOS is not available yet: to update, download the new `.dmg` from the releases page.

## Uninstall

- **Windows**: **Windows Settings > Apps > AgentHub > Uninstall**.
- **macOS**: move AgentHub from Applications to the Trash.

Your data in `~/.agenthub` (`%USERPROFILE%\.agenthub` on Windows: projects, memory, wiki, history) is **not deleted**.
