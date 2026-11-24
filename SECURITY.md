# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in FlowSpeak (including the desktop app, local loopback dashboard authentication, license verification, or `smolkapps.com/flowspeak/`), please report it privately rather than opening a public GitHub issue.

- **Email:** [support@smolkapps.com](mailto:support@smolkapps.com) (Subject: `[Security] FlowSpeak Vulnerability Report`)
- **GitHub Private Reporting:** Use the **Security → Advisories → Report a vulnerability** workflow on this repository if enabled.

Please include:
1. Affected version (`FlowSpeak --version` or DMG filename) and OS version.
2. Clear reproduction steps or proof-of-concept.
3. Expected vs. actual security boundary behavior.

You will receive an acknowledgment within 72 hours. Once verified and remediated, fixes will be documented in [CHANGELOG.md](./CHANGELOG.md).

## Scope Notes

- Audio recording occurs strictly while the push-to-talk trigger is actively held or locked in hands-free mode, and stays on-device when using Local Whisper.
- Local API requests bind to `127.0.0.1` and require a per-session bearer token generated at launch.
- Optional cloud API keys and AI keys are stored in the OS Keychain / Credential Store rather than plaintext JSON config.
