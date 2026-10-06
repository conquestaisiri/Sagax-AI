# How Sagax AI is organized

Sagax AI is one Windows desktop app with two separate modes. It does not run
both modes at the same time.

## API Mode

API Mode opens Sagax's interface. It uses the provider and API key selected in
Sagax settings. Its listening, transcription, answer, and profile settings
belong to API Mode. Audio or text sent for a request goes to the provider used
for that request; that provider's service rules, limits, and billing apply.

## GPT Mode

GPT Mode opens the ChatGPT website in the app. Sign in on that website, not in
Sagax's API-key settings. ChatGPT handles its own account, conversation, voice
feature, service limits, and policies. GPT Mode's controls and settings are
separate from API Mode.

## Switching modes

The app stops the mode that is running before it starts the other one. The
welcome screen lets you choose a starting mode; **Settings → Application mode**
lets you switch later. A setting in one mode should not be treated as a setting
for the other mode.

## Current preview boundary

In 1.5.8, API Mode's automatic screen reading, OCR, and visual-answer path is
disabled. This repository does not publish the application source code or
describe private implementation details. The [getting-started guide](GETTING_STARTED.md)
explains the user-visible steps.
