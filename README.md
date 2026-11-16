# MOM-AI downloads

Public installer catalog and release notes for MOM-AI. Application source is maintained privately; customer recordings, Google credentials and API keys are never part of this repository.

## Current availability

**There is no Windows-and-Mac production release yet.** The present candidate targets Apple silicon Macs. Windows and Intel Mac installers are not available. A draft release is preparation for review; its assets are not public downloads until that release is published.

Each published release will state its supported platform, preview/production status, signing/notarization status, prerequisites and known limitations. Do not assume a personal preview is a signed/notarized commercial installer. Do not disable operating-system security protections to install a preview.

## Meeting workflow

MOM-AI is being built to join authorized Google Meet meetings, capture audio/video, transcribe locally with Whisper Large v3, generate English minutes from a natural Hindi-English transcript through the user's Gemini API key, and archive to the user's Google Drive. Google admission, account approval, recording permission and third-party API/storage limits apply. Review generated minutes against the recording.

Publisher Google production approval/onboarding and a fresh full live acceptance run remain outstanding. Current controlled builds require importing Google Desktop OAuth client configuration. These builds are not ready for general customer onboarding.

## Updates

New desktop previews can check this repository's published releases and notify users when a newer compatible installer is available. Current installation is **manual**. Release notifications do not provide automatic signed installation or remote control of customer computers. Signed automatic upgrades require separate signing, packaging and upgrade testing.

When an appropriate release is published, download only its installer for your platform and compare its SHA-256 checksum with `SHA256SUMS.txt`. Check the release notes before installation and finish recording/processing first. Draft releases are visible only to repository collaborators and do not trigger update notifications.

## Support

Publisher: Gaurav Goyal. Contact: support@gahahq.tech.

This is a download catalog, not a support inbox for secrets. Never post API keys, passwords, authorization links or private meeting recordings in issues.
