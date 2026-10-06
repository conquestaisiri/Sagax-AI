# Troubleshooting

## The app does not open or install

- Confirm the file came from the [1.5.8 release page](https://github.com/conquestaisiri/Sagax-AI/releases/tag/v1.5.8).
- Install only one format. Use the EXE for a normal install; use the MSI when
  you specifically need a Windows Installer package.
- If Windows displays a warning, read it carefully. Do not bypass a warning
  unless you have independently confirmed the file and its checksum.

## API Mode does not answer

1. Confirm **API Mode** is active.
2. Open **Settings → API keys** and check that a supported provider key is
   present and accepted.
3. Check the provider's service status, account limits, and billing rules.
4. Test with a short, non-private typed question.
5. Check **Settings → Advanced → Run diagnostics** and keep the error message.

An API key from one provider usually cannot be used with another provider.

## API Mode does not hear audio

- Open **Settings → Listening** and select the intended microphone or computer
  audio source.
- Use **Test audio** and confirm Windows has not muted or blocked the device.
- Make sure another application is not exclusively using the audio device.

## GPT Mode is not signed in or voice does not start

- Check that the ChatGPT page has finished loading and that the computer is
  online.
- Sign in using the **Log in** button on the ChatGPT page, not Sagax API-key
  settings.
- If Sagax's **Voice chat** shortcut does not work, use ChatGPT's own voice
  control on the page and check Windows microphone permission.
- ChatGPT account access and voice availability are controlled by the ChatGPT
  service.

## A setting seems to have no effect

Check which mode is active. API Mode and GPT Mode have separate settings, and
the settings for one mode do not control the other. Some screen-reading and
visual-answer controls are disabled in this preview.

## Contact support

Use [GitHub Issues](https://github.com/conquestaisiri/Sagax-AI/issues) for a
bug report or question. Include the app version, Windows version, active mode,
and steps to reproduce. Remove API keys, passwords, private transcripts,
personal data, and screenshots containing sensitive information.
