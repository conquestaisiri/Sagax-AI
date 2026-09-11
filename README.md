# Sagax AI

![Windows](https://img.shields.io/badge/Windows-10%2F11-0078D6?style=flat-square&logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/status-active-brightgreen?style=flat-square)
![Version](https://img.shields.io/badge/version-1.5.2-blue?style=flat-square)
![License](https://img.shields.io/badge/license-proprietary-red?style=flat-square)

**Sagax AI is a real-time interview assistant for Windows.** It listens to your
live interview (system audio, microphone, or both), understands what's on your
screen, and drafts natural first-person answers in your own voice — as it
happens.

<p align="center">
  <img src="assets/logo.png" alt="Sagax AI" width="220" />
</p>

---

## What it does

- 🎧 **Hears the interviewer** through system loopback audio, your microphone,
  or both at once — with per-source pipelines so overlapping speech never fuses.
- 🖥️ **Reads your screen** — OCR plus vision models for questions, code,
  charts, and tables. Automatic, manual (hotkey), or fully off.
- ⌨️ **Global hotkeys** — analyze the screen, force an answer, or toggle the
  Mini Answer window from any app. They belong to Sagax and release when it
  closes; they never steal focus.
- 🔑 **Quota-aware multi-key routing** — every provider key is health-tracked
  with live quota headroom. A rate-limited key fails over in milliseconds;
  keys sharing one account quota are never pointlessly retried one after
  another.
- 🗝️ **In-app key manager** — per-provider key lists with personal labels,
  one-click validation (no quota spent), encrypted storage.
- 🪟 **Mini Answer pill** — the current answer, always on top, never in the way.
- 🔒 **Private by design** — credentials live encrypted on your machine
  (Windows DPAPI). No account, no cloud dashboard, no telemetry.

## How it answers

1. Speech is transcribed per source and merged into timestamped utterances.
2. Questions are detected, attributed (interviewer vs. you), and tracked in a
   turn ledger with speaker continuity.
3. The router picks the healthiest provider/model/key with real quota headroom
   and streams the draft — then the Mini Answer pill shows it instantly.

## Screenshots

> Coming soon — the pill, the dashboard, and Settings in action.

## Tech at a glance

| Layer        | Technology                              |
| ------------ | --------------------------------------- |
| App          | Python, WebView2 dashboard + Mini pill  |
| Audio        | Loopback + mic capture, cloud + local transcription |
| Vision       | Tesseract OCR + multimodal vision models |
| AI routing   | Multi-provider pool with quota domains  |
| Speaker      | On-device embedding model (ONNX)        |
| Packaging    | PyInstaller + WiX (per-machine MSI)     |
| Secret store | Windows DPAPI (`keys_v1`)               |

## About this repository

This is the **public showcase** for Sagax AI. It contains product
documentation and brand assets only:

- `docs/ARCHITECTURE.md` — how the system fits together
- `docs/PRIVACY.md` — where your data lives (spoiler: only your machine)
- `docs/CHANGELOG.md` — release history
- `assets/` — brand artwork

**Application source code, installers, and credentials are not published
here.** Sagax AI is proprietary software — © Sagax. All rights reserved
(see [LICENSE](LICENSE)).

## Try it

Trial builds (time-limited, bring-your-own-keys) are available on request.
Contact the maintainer through the profile linked on this page.
