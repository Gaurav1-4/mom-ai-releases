# MOM-AI downloads

Public installer catalog and release notes for MOM-AI. Application source is maintained privately; customer recordings, Google credentials and API keys are never part of this repository.

## Current availability

**MOM-AI 0.5.1 is a testing preview for Apple silicon Mac and Windows x64.**

[Download both installers and SHA-256 checksums](https://github.com/Gaurav1-4/mom-ai-releases/releases/tag/v0.5.1).

Sharing with friends? Start with the [friend testing and installation guide](FRIENDS-SETUP.md). No App Store listing or Apple Developer account is required for users.

- Mac: `MOM-AI-0.5.1-arm64.dmg` — ad-hoc signed, not notarized.
- Windows: `MOM-AI-0.5.1-win-x64.exe` — unsigned per-user installer.
- New: the compact update popup offers **Update now**, **Release notes** and **Later**. Update now downloads/verifies and opens the system installer without a browser download.
- One resumable setup flow prepares Docker, local Python/audio tools, the recorder and Whisper. Docker may require OS permissions or WSL setup/restart.
- New: full timestamped transcript text export and a detailed MOM PDF with discussion, decisions, action items and open questions. New text/PDF files are included in automatic Drive uploads.
- Current Mac and Windows CI passed private tool installation, actual audio conversion, setup/retry UI, transcript/PDF downloads and installer builds. Previous Windows installation/reinstall/uninstall and full local Large v3 inference checks passed; the shared recorder passed synthetic audio/video and automatic stopping checks.
- Real Windows Google Meet/WSL2 end-to-end acceptance, long-session testing and commercial signing remain pending. Intel Mac and Windows ARM64 are not validated targets.

Each published release will state its supported platform, preview/production status, signing/notarization status, prerequisites and known limitations. Do not assume a personal preview is a signed/notarized commercial installer. Do not disable operating-system security protections to install a preview.

## Meeting workflow

MOM-AI is being built to join authorized Google Meet meetings, capture audio/video, transcribe locally with Whisper Large v3, generate English minutes from a natural Hindi-English transcript through the user's Gemini API key, and archive to the user's Google Drive. Google admission, account approval, recording permission and third-party API/storage limits apply. Review generated minutes against the recording.

Publisher Google production approval/onboarding and a fresh full live acceptance run remain outstanding. Current controlled builds require importing Google Desktop OAuth client configuration. These builds are not ready for general customer onboarding.

## Updates

Version 0.5.1 checks this repository and offers **Update now** in the popup. It downloads the correct installer, verifies its SHA-256 and size, and opens it after current work has finished. On Mac, replace MOM-AI in Applications and reopen it; on Windows, complete the installer. Normal OS permission/security prompts remain. Versions older than 0.5.1 need one initial installer upgrade to get this new popup.

Fully automatic replacement with **Restart and install** remains available only in signed updater builds. Preview updates use the interactive system installer and never disable OS security checks.

When an appropriate release is published, download only its installer for your platform and compare its SHA-256 checksum with `SHA256SUMS.txt`. Check the release notes before installation and finish recording/processing first. Draft releases are visible only to repository collaborators and do not trigger update notifications.

## Support

Publisher: Gaurav Goyal. Contact: support@gahahq.tech.

This is a download catalog, not a support inbox for secrets. Never post API keys, passwords, authorization links or private meeting recordings in issues.
