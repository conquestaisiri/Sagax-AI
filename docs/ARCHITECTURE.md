# Sagax AI — Architecture Overview

> Companion to the product README. No source code is published in this
> repository; this document describes the system at a conceptual level.

## Big picture

```
┌─────────────┐   ┌──────────────┐   ┌──────────────┐   ┌────────────┐
│   Capture   │──▶│ Transcribe   │──▶│    Answer    │──▶│  Present   │
│ mic+loopback│   │ cloud+local  │   │ router+pool  │   │ main+pill  │
└─────────────┘   └──────────────┘   └──────────────┘   └────────────┘
        │                  │                  │                 ▲
        └──────────┬───────┴──────────────────┘                 │
                   ▼                                            │
          ┌──────────────┐   ┌──────────────┐                   │
          │    Screen    │──▶│ Visual turns │───────────────────┘
          │  OCR+vision  │   │  ledger-bound│
          └──────────────┘   └──────────────┘
```

## Audio

- **Dual-source capture.** System (loopback) and microphone run on independent
  pipelines with separate utterance assemblers, so overlapping speech from the
  interviewer and the user never fuses into one transcript.
- **Transcription fleet.** Cloud lanes first (parallel providers, fastest
  healthy lane wins with instant failover), local offline model as fallback.
- **Answer inhibition.** Microphone speech is remembered as the user's context
  but never auto-answered; system speech drives interview answers.

## Vision

Three modes, switchable live without restart:

| Mode        | Behavior                                                     |
| ----------- | ------------------------------------------------------------ |
| Automatic   | Screen changes are scored; real questions open visual turns. |
| Manual      | All automatic watching is dormant. A global hotkey captures, reads, and answers the current screen exactly once. |
| Off         | No capture, no OCR, no vision calls. The hotkey politely refuses. |

Manual captures bypass duplicate suppression *by explicit intent* (pressing the
key means "look now"), while automatic turns stay deduplicated. The app's own
windows are masked out of every capture.

## Routing

- **Endpoint pool.** Every provider × model × key is a tracked endpoint with
  latency averages, consecutive-failure counts, and cooldowns. Failures retire
  only the affected scope: a bad key retires its own routes, a rate limit with
  a server backoff hint cools the provider.
- **Quota domains.** Keys sharing one account/organization/project quota are
  treated as one capacity pool — the scheduler never burns time retrying five
  keys against the same exhausted quota. Genuinely independent quotas are used
  as independent capacity. Switching keys happens before switching providers.
- **Headroom, not hope.** Live rate-limit headers feed remaining/reset state,
  and a conservative reserve keeps the scheduler off nearly-empty keys, so a
  429 rarely arrives mid-question.

## Memory & safety

- Session ledger with question/answer tracking, fact registry, and
  per-question evidence tags (heard / screen / context).
- Output guards and a reviewable trace of routing decisions (provider, model,
  key alias, headroom — never key material).

## Packaging & identity

- Windows desktop app (per-machine MSI, MajorUpgrade lineage, single-instance
  guard), on-device speaker model, vendored OCR discovery, DPAPI credential
  vault with a human-labelled in-app key manager.
