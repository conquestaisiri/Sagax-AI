<p align="center">
  <img src="assets/logo.png" alt="Sagax AI logo" width="110" />
</p>

# Sagax AI

**Current primary build: Sagax AI 1.5.8 — Preview**

Sagax AI is a Windows desktop app with two separate ways to work. Choose **API
Mode** to use Sagax with an AI provider you configure, or **GPT Mode** to open
the ChatGPT website inside Sagax. Only one mode runs at a time.

> **Download only from the current release.** Earlier prototype files are not
> current downloads. Version 1.5.8 is a preview build, not a claim that the app
> has been tested on every Windows computer.

## Download Sagax AI 1.5.8

**[Open the Sagax AI 1.5.8 release](https://github.com/conquestaisiri/Sagax-AI/releases/tag/v1.5.8)**

Choose one installer from that page:

- **EXE setup** — the normal interactive installer for most people.
- **MSI package** — use this if you specifically need a Windows Installer
  package, for example for managed deployment.

Both install the same 1.5.8 preview. They are large downloads (about 0.8 GB
each); install only one. The release page includes SHA-256 checksums so you can
check that your download matches the published file. The installers are not
digitally signed, so Windows may say that the publisher is unknown. A checksum
checks that a file was not changed in download; it does **not** prove who made
the file or certify that it is safe. Download only from this repository's
release page.

## Pick a mode

| Mode | What it does | What you need |
| --- | --- | --- |
| **API Mode** | Uses Sagax's own listening and answer interface with a supported AI provider. | A provider API key and working audio setup. Provider limits or charges may apply. |
| **GPT Mode** | Shows the ChatGPT website inside Sagax. ChatGPT's website handles its own sign-in and chat. | Internet access; a ChatGPT account if you want to sign in. |

The modes have separate settings. Switching modes stops the current mode before
starting the other. A provider API key is not your ChatGPT password.

## First steps

1. Install one of the 1.5.8 installers above and open Sagax AI.
2. Choose **API Mode** or **GPT Mode** on the welcome screen. You can change
   this later in **Settings → Application mode**.
3. Follow the matching guide: [API Mode](docs/GETTING_STARTED.md#api-mode) or
   [GPT Mode](docs/GETTING_STARTED.md#gpt-mode).
4. Use the in-app **Step-by-step guide** if you want Sagax to walk you through
   the buttons.

## Important preview limits

- Sagax AI 1.5.8 is a preview. Speed and results depend on your computer,
  audio setup, internet connection, and provider. No fixed response time is
  promised.
- API Mode's screen-reading and visual-answer features are turned off in this
  build. Do not rely on disabled screen controls.
- GPT Mode opens the ChatGPT website; it is not the same as API Mode and does
  not use API Mode's answer settings.
- Review [privacy and data flow](docs/PRIVACY.md) before sending audio,
  transcripts, profile details, or screenshots to an AI service.

## Help and project information

- [Getting started and step-by-step instructions](docs/GETTING_STARTED.md)
- [Troubleshooting](docs/TROUBLESHOOTING.md)
- [Privacy and data flow](docs/PRIVACY.md)
- [How the two modes work](docs/ARCHITECTURE.md)
- [1.5.8 preview notes](docs/CHANGELOG.md)
- [Support](SUPPORT.md)
- [Security reporting](SECURITY.md)

## This repository

This is the product information and download page for Sagax AI. The Windows
application source code is not published here. Sagax AI is proprietary; see
[LICENSE](LICENSE). The current primary download is always the 1.5.8 release
linked above—not an old file or a copy attached to a discussion.
