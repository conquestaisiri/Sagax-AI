# Sagax AI — Privacy

## The short version

Your data lives on your computer. There is no Sagax account, no cloud
dashboard, and no telemetry.

## Credentials

- API keys are encrypted with **Windows DPAPI** (current-user scope) the
  moment you add them in Settings → API keys.
- They are decrypted only in memory, only to call the AI provider you chose.
- They are never written to logs, reports, settings exports, or installers.
- Key labels are stored separately from key values, referenced by an
  irreversible fingerprint — a label alone can never reveal a key.

## What leaves your machine

Only what the features you enable require:

| You enable…      | Sent to…                          | Content                    |
| ---------------- | --------------------------------- | -------------------------- |
| Answers          | Your chosen AI provider(s)        | Question + profile context |
| Transcription    | Your chosen transcription lane    | Audio chunks               |
| Screen reading   | Your chosen vision lane           | Screenshots / OCR text     |

Disable a feature and its traffic stops entirely. Vision Off performs zero
captures — verified by idle counters, not by promise.

## What stays local

Profile/CV text, sessions, settings, trial anchors, routing statistics, and
the credential vault — all under your own user profile. Uninstalling removes
the application; your data folder is left for you to keep or delete.

## Screen privacy

The app's own windows are masked out of every capture, and an optional
stealth mode hides Sagax from recordings and shared screens.
