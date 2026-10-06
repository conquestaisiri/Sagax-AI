# Sagax AI 1.5.8 — Current Preview Build

This is the **current primary preview build** of Sagax AI for Windows. It is
not presented as a fully production-validated release.

## Choose one installer

- `SagaxAI-Setup-1.5.8.exe` — normal interactive setup.
- `SagaxAI-Setup-1.5.8.msi` — Windows Installer package for managed or
  organization deployment.

Both install the same build. Install only one. Each download is about 0.8 GB.

## Important download and Windows warning

The installers are **not digitally signed**. Windows may show that the
publisher is unknown. Download only from this official release. The SHA-256
checksums in [`SHA256SUMS.txt`](https://github.com/conquestaisiri/Sagax-AI/releases/download/v1.5.8/SHA256SUMS.txt)
can tell you whether the download matches the published file; checksums do not
prove who created a file or certify that it is safe. On Windows, open
PowerShell in the download folder and run
`Get-FileHash .\SagaxAI-Setup-1.5.8.exe -Algorithm SHA256` (use `.msi` instead
of `.exe` if you downloaded the MSI). Compare the displayed hash with the
matching line in `SHA256SUMS.txt`.

## What is included

- Separate API Mode and GPT Mode in one desktop application.
- Separate settings for each mode; only one mode runs at a time.
- Welcome screen and step-by-step guide for both modes.
- Updated Sagax application and tray branding.
- API Mode screen-reading and visual-answer features are disabled in this
  preview.

## Checks performed

- 25 Python unit tests passed.
- Desktop host TypeScript type-check passed.
- Packaged sidecar smoke test passed and reported version 1.5.8.
- MSI and executable version metadata were checked.

These checks do not confirm behavior on every computer. Performance and
provider availability vary by hardware, audio setup, network, account, and
service limits. No fixed response time is promised. Read [Getting started](https://github.com/conquestaisiri/Sagax-AI/blob/main/docs/GETTING_STARTED.md), [Privacy](https://github.com/conquestaisiri/Sagax-AI/blob/main/docs/PRIVACY.md), and [Troubleshooting](https://github.com/conquestaisiri/Sagax-AI/blob/main/docs/TROUBLESHOOTING.md) before use.
