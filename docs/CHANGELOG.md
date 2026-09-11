# Sagax AI — Changelog

## 1.5.2 — Provider key manager + trial build

- Settings → API keys: per-provider key lists with personal labels, one-click
  validation that spends no quota, encrypted storage, live reload without
  restart, safe removal.
- Separate time-limited trial build (bring your own keys, honest countdown).
- Trial length: 4 calendar months + 9 days from first launch.

## 1.5.1 — Global hotkeys + manual vision

- System-wide shortcuts (Analyze screen, Answer now, Show/hide Mini) that work
  from any app while Sagax is open and release when it closes. Fully
  configurable with conflict detection.
- Manual vision mode: automatic screen-watching goes dormant; one hotkey
  press captures, reads, and answers the current screen into the app and the
  Mini pill. Vision Off captures nothing at all.
- Credential health/quotas mirrored live for routing telemetry.

## 1.5.0 — Quota-aware credential scheduling

- Quota domains: keys sharing one account quota are scheduled as one pool;
  independent quotas as independent capacity. Pre-emptive headroom reserves,
  distinct failure states (auth/billing/access/rate-limit/transient), and
  millisecond same-domain failover without request storms.

## 1.4.0 — Multimodal cognitive release

- Dual-source audio pipelines, visual-turn engine with actionability scoring,
  hedged low-latency chat routing, on-device speaker continuity, WebView2
  dashboard with Mini Answer pill.

## 1.3.x — Dual-capture repair and human-like field acceptance

- Loopback + microphone independence, answer inhibition for user speech,
  self-output suppression, interviewer-turn continuity.
