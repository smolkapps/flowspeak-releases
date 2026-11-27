# FlowSpeak Releases & Issue Tracker

[![Website](https://img.shields.io/badge/Website-smolkapps.com%2Fflowspeak-3b4ce2)](https://smolkapps.com/flowspeak/)
[![Latest Release](https://img.shields.io/github/v/release/smolkapps/flowspeak-releases)](https://github.com/smolkapps/flowspeak-releases/releases)

Official binary releases, SHA-256 verification manifests, changelogs, and public issue tracker for **FlowSpeak** (`© 2026 Smolk Apps`), local push-to-talk voice dictation (`Hold Ctrl`, speak, release) built in Go with in-process `whisper.cpp` and a native Liquid Glass desktop dashboard.

- **Website & Pricing:** [smolkapps.com/flowspeak](https://smolkapps.com/flowspeak/)
- **Documentation & Support:** [smolkapps.com/flowspeak/support](https://smolkapps.com/flowspeak/support/)
- **Privacy Policy:** [smolkapps.com/flowspeak/privacy](https://smolkapps.com/flowspeak/privacy/)
- **Lost License Key Recovery:** [smolkapps.com/flowspeak/recover](https://smolkapps.com/flowspeak/recover/)

## Highlights

- **Hold `Ctrl` to Dictate:** Zero finger-yoga shortcuts (`Ctrl` either/left/right, `Fn`/Globe, or Right `Option`). Smart chord cancellation (`Ctrl+C`, `Ctrl+Tab`, `Ctrl+Click`) and double-tap hands-free recording with `Esc` abort.
- **Liquid Glass Interface (Default):** Translucent Liquid Glass macOS dashboard and floating recording HUD (`NSGlassEffectView` on macOS 26+ with `NSVisualEffectView` fallback back to macOS 12), plus an automatic Reduce Transparency fallback and a **Classic Solid** toggle under `Settings -> Appearance`.
- **On-Device Privacy First:** Static in-process `whisper.cpp v1.9.5` powered by Apple Silicon Metal + Accelerate, Intel `x86_64` AVX2, or Linux `x86_64`, plus optional Experimental Features in Settings for Groq, OpenAI, or local Ollama via OS Keychain (off by default).
- **Shared Local Whisper Model Reuse:** Automatically detects and reuses compatible Whisper GGML weights already on disk (`~/.cache/whisper.cpp`, MacWhisper, SuperWhisper, VoiceInk, Spokenly) so models are not duplicated (~11 MB macOS app binary + 141 MB default speech model).
- **Clipboard-Preserving Paste & Zero-Fluff Cleanup:** Deterministic filler/stutter stripping, Personal Dictionary & Voice Snippets, 99-language menu bar Language switcher, and original clipboard restoration after auto-paste.
- **Black Friday / Cyber Monday Pricing (Through Nov 30, 2026):** Free download with **25 full dictations**. Lifetime Pro is **$19 one-time through Nov 30, 2026** (rises to **$49 Founding Lifetime** or **$9/mo · $69/yr** starting **Dec 1**) for up to **3 personal computers** (macOS 12+ and Linux) with offline Ed25519 verification and a 30-day money-back guarantee.

## Install & Downloads

### macOS via Homebrew

```bash
brew install --cask smolkapps/tap/flowspeak
```

### Direct Downloads (`v1.2.2`)

Grab binaries from the [Releases](https://github.com/smolkapps/flowspeak-releases/releases) page or [smolkapps.com/flowspeak](https://smolkapps.com/flowspeak/):

| Platform | Artifact | Notes |
| --- | --- | --- |
| **macOS 12+** (Apple Silicon & Intel Universal) | `FlowSpeak-1.2.2-Universal.dmg` | ~11 MB app binary (+ local Whisper model, 141 MB default, or reuse existing GGML weights); Developer ID signed & double-notarized |
| **Linux** (`x86_64`) | `FlowSpeak-1.2.2-linux-amd64.tar.gz` | 4.2 MB binary (+ local Whisper model) + `.desktop` installer |

### Verify Checksums

```bash
# macOS
shasum -a 256 -c SHA256SUMS.txt --ignore-missing

# Linux
sha256sum -c SHA256SUMS.txt --ignore-missing
```

### macOS Gatekeeper Verification

Official `FlowSpeak-1.2.2-Universal.dmg` and `FlowSpeak.app` releases are signed with our Apple Developer ID certificate (`4R42A425CK`) with Hardened Runtime, notarized by Apple, and stapled, so Gatekeeper opens them directly without any quarantine workaround:

```bash
spctl -a -vvv -t open --context context:primary-signature FlowSpeak-1.2.2-Universal.dmg
xcrun stapler validate FlowSpeak-1.2.2-Universal.dmg
```

### Linux Install

```bash
tar -xzf FlowSpeak-1.2.2-linux-amd64.tar.gz
cd flowspeak-1.2.2-linux-amd64
./install.sh
```

## Reporting Bugs & Feature Requests

Please use our [Issue Templates](https://github.com/smolkapps/flowspeak-releases/issues/new/choose) and include your OS version, FlowSpeak version, chosen trigger key / engine, and non-sensitive logs.
