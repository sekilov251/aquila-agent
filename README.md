<p align="center">
  <img src="apps/desktop/assets/icon.png" alt="Aquila Agent" width="96" height="96" />
</p>

<h1 align="center">Aquila Agent</h1>

<p align="center"><b>The agent that grows with you — by Savez.</b></p>

<p align="center">
  <a href="https://github.com/sekilov251/aquila-agent/releases/latest/download/Aquila-Setup.exe"><img src="https://img.shields.io/badge/Download_for_Windows-F5C518?style=for-the-badge&logoColor=black" alt="Download for Windows"></a>
  <a href="https://sekilov251.github.io/aquila-agent/"><img src="https://img.shields.io/badge/Website-1a1710?style=for-the-badge" alt="Website"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License: MIT"></a>
</p>

Aquila Agent is a self-improving AI agent with persistent memory, skills it
creates from experience, scheduled jobs, and connections to Telegram, Discord,
Slack, WhatsApp, Signal, and more — with a polished native desktop app for
macOS, Windows, and Linux.

## Install

**Windows:** download [Aquila-Setup.exe](https://github.com/sekilov251/aquila-agent/releases/latest/download/Aquila-Setup.exe)
(7.5 MB) and run it — it sets everything up in the background. Prefer a full
offline installer? Grab
[Aquila-0.17.0-win-x64.exe](https://github.com/sekilov251/aquila-agent/releases/latest/download/Aquila-0.17.0-win-x64.exe) (105 MB).

**macOS / Linux:** build from source — see
[apps/desktop](apps/desktop/README.md) (`npm run dist:mac` / `dist:linux`).

## Highlights

- **Gold-standard desktop app** — chat with streaming tool output,
  side-by-side previews, a file browser, voice, and settings, in the
  signature Aquila Gold look.
- **Learning loop** — creates skills from experience, improves them during
  use, and builds a deepening model of you across sessions.
- **Runs anywhere** — a $5 VPS, a GPU cluster, or your laptop.
- **Any model** — OpenRouter, OpenAI, your own endpoint, and many others.

## Develop

```bash
npm install                # repo root — links workspaces
cd apps/desktop
npm run dev                # Vite renderer + Electron shell
```

See [apps/desktop/README.md](apps/desktop/README.md) for architecture,
packaging, and verification.

## License

[MIT](LICENSE) — © 2026 Savez.
