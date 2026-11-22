# Try MOM-AI with friends

MOM-AI 0.5.0 is a testing preview for **Apple silicon Macs** and **Windows x64 PCs**. The source stays private; the installers are public. Users do not need an Apple Developer account or an App Store listing to install it.

## Download and install

Open the [MOM-AI 0.5.0 release](https://github.com/Gaurav1-4/mom-ai-releases/releases/tag/v0.5.0), read its notes, and choose your installer. The release includes `SHA256SUMS.txt` for checking downloads.

- **Mac:** Download `MOM-AI-0.5.0-arm64.dmg`, open it, and drag MOM-AI into Applications. Launch it from Applications. This preview is ad-hoc signed and not Apple-notarized. If macOS reports an unidentified developer, and you trust the publisher and verified download, Apple's per-app **System Settings → Privacy & Security → Open Anyway** option may be available after the first launch attempt. Follow [Apple's instructions](https://support.apple.com/en-us/102445); managed Macs can restrict this option. A malware or damaged-app warning needs investigation—contact support instead of overriding it.
- **Windows:** Download `MOM-AI-0.5.0-win-x64.exe` and run the per-user installer. This preview is unsigned and can show a publisher warning. If Windows blocks installation, send support the exact error. Do not disable Defender or other system protections.

## Prepare the local meeting worker

1. Open MOM-AI and choose **Set up this computer**. The app prepares local Python/audio tools, Docker, the recorder and Whisper Large v3. It reuses compatible components that are already installed.
2. Complete Docker's installer, licence and OS permission prompts. On Windows, use Linux containers with WSL2 and restart if requested. Keep MOM-AI open to continue automatically; after a restart, reopen it and choose **Resume setup**.
3. When setup is ready, choose **Connect Google and Gemini**. Allow several GB of disk space and download time. Transcription speed and memory use depend on your machine.

Keep the app running and the computer awake and online during scheduled meetings and processing.

## Connect your own accounts

This preview still needs coordinated Google setup; downloading the installer alone does not complete onboarding.

- Obtain the Google **Desktop OAuth client configuration** privately from the publisher, with your account approved as a test user while that Google project remains in Testing mode. Alternatively, configure your own Google Cloud project and Desktop OAuth client for the app's required APIs/scopes. Do not post client configuration or tokens in this public repository.
- In Connections, import the required client configuration and connect your own Calendar and Drive accounts.
- Sign the bot browser into your own intended Google account and complete the app's identity check. Invite that account to the meeting. Google can still require host admission.
- Add your own Gemini API key for English meeting minutes. Transcription uses the local model.

The publisher's personal Google accounts, API keys and meeting data are not included in the installer. Google's test-user restrictions are separate from GitHub distribution and Apple's installation checks. General customer sign-up needs the remaining Google production setup.

## Run a short meeting test

Schedule a Google Meet in the connected calendar and invite the bot account. Join with your Meet microphone unmuted, admit the bot if needed, and speak briefly. Leave the meeting, then check that MOM-AI stops automatically and produces a playable recording, natural Hindi-English transcript, English minutes, and Drive copies. Allow time for local transcription.

Real Windows Google Meet/WSL2 end-to-end acceptance and long-session testing remain pending. This is a friend-testing preview, not a fully validated commercial release.

## Export your meeting

- In **Transcript**, choose **Export transcript (.txt)** for the complete selected version with timestamps and original Hindi-English text. JSON is also available.
- In **Minutes**, choose **Export MOM (PDF)** for a formatted report with executive summary, discussion/context, decisions, action items with owners/deadlines, and open questions. New reports target 1-2 A4 pages. Longer reports retain extra pages rather than dropping details.
- For an older recording, use **Regenerate MOM** once to add the new detailed discussion section. Exporting a saved transcript/report does not need another AI request; regenerating uses your Gemini key.
- New text/PDF files are saved locally and included in automatic Drive uploads when Drive is connected.

## Updates and support

Version 0.5.0 uses release notifications with manual installer updates. The signed in-app updater has been prepared in the private source but is not enabled in this public preview. Finish meetings and processing before installing an update.

Contact **support@gahahq.tech** with your OS, app version and error text. Never post passwords, API keys, authorization links or private meeting recordings in public issues.
