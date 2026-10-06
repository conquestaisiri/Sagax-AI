# Getting started with Sagax AI 1.5.8

This guide uses short steps. The app also has a **Step-by-step guide** on its
welcome screen.

## Install

1. Open the [1.5.8 release page](https://github.com/conquestaisiri/Sagax-AI/releases/tag/v1.5.8).
2. Download **one** installer: the EXE setup for a normal interactive install,
   or the MSI if you need a Windows Installer package.
3. Run the file you downloaded and follow the Windows prompts.
4. Open Sagax AI. The welcome screen asks which mode you want to use.

The two installers are different formats for the same preview version. Do not
install both. The download is about 0.8 GB.

## API Mode

API Mode uses Sagax's own listening and answer interface together with an AI
provider that you configure.

1. On the welcome screen, choose **API Mode**.
2. Open **Settings → API keys**. Add a key from a provider shown in Sagax. A
   ChatGPT password is not an API key.
3. Open **Settings → Profile & context** and add only correct information you
   want the selected provider to receive.
4. Open **Settings → Listening**. Choose the audio source you want and use
   **Test audio** with a harmless voice clip.
5. Open the Live page and start listening. Try a short typed question first if
   you want to test answering without a live call.
6. Stop listening when you are done.

Provider access, free limits, billing, and response speed depend on that
provider and your account. API Mode's screen-reading and visual-answer features
are disabled in this preview.

## GPT Mode

GPT Mode displays the ChatGPT website inside the Sagax window. The website—not
Sagax API Mode—handles ChatGPT conversations and voice chat.

1. On the welcome screen, choose **GPT Mode**.
2. Wait for the ChatGPT page to load.
3. If needed, click **Log in** on the ChatGPT page and sign in there. Do not
   enter your ChatGPT password in Sagax settings.
4. Type a harmless test message in ChatGPT's message box and send it.
5. To try voice, use the Sagax **Voice chat** shortcut or ChatGPT's own voice
   control. If the shortcut does not find the website control, use the control
   on the ChatGPT page.

ChatGPT account access, voice availability, and usage limits are controlled by
the ChatGPT service. GPT Mode does not use API Mode's provider keys or listening
settings.

## Change modes

Open **Settings → Application mode**, then choose API Mode or GPT Mode. Sagax
stops the active mode before starting the other. Do not switch modes during a
live call unless you intend to stop the current mode.

## Privacy reminder

Before using real conversations, read [Privacy and data flow](PRIVACY.md). Use
only audio, transcripts, screenshots, and profile details that you have the
right to send to the service you selected.
