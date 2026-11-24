# FlowSpeak Releases & Issue Tracker

[![Website](https://img.shields.io/badge/Website-smolkapps.com%2Fflowspeak-3b4ce2)](https://smolkapps.com/flowspeak/)
[![Latest Release](https://img.shields.io/github/v/release/smolkapps/flowspeak-releases)](https://github.com/smolkapps/flowspeak-releases/releases)

Official binary releases, SHA-256 verification manifests, changelogs, and public issue tracker for **FlowSpeak** (`© 2026 Smolk Apps`) — local push-to-talk voice dictation (`Hold Ctrl`, speak, release) built in Go with in-process `whisper.cpp` and a native Liquid Glass desktop dashboard.

- **Website & Pricing:** [smolkapps.com/flowspeak](https://smolkapps.com/flowspeak/)
- **Documentation & Support:** [smolkapps.com/flowspeak/support](https://smolkapps.com/flowspeak/support/)
- **Privacy Policy:** [smolkapps.com/flowspeak/privacy](https://smolkapps.com/flowspeak/privacy/)
- **Lost License Key Recovery:** [smolkapps.com/flowspeak/recover](https://smolkapps.com/flowspeak/recover/)

## Highlights

- **Hold `Ctrl` to Dictate:** Zero finger-yoga shortcuts (`Ctrl` either/left/right, `Fn`/Globe, or Right `Option`). Smart chord cancellation (`Ctrl+C`, `Ctrl+Tab`, `Ctrl+Click`) and double-tap hands-free recording with `Esc` abort.
- **Liquid Glass Interface (Default):** Translucent Liquid Glass macOS dashboard and floating recording HUD (`NSGlassEffectView` on macOS 26+ with `NSVisualEffectView` fallback back to macOS 12), plus an automatic Reduce Transparency fallback and a **Classic Solid** toggle under `Settings → Appearance`.
- **On-Device Privacy First:** Static in-process `whisper.cpp v1.9.5` powered by Apple Silicon Metal + Accelerate, Intel `x86_64` AVX2, or Linux `x86_64`, plus optional Groq / OpenAI / custom OpenAI-compatible LAN fallback and optional Ollama cleanup.
- **Clipboard-Preserving Paste & Zero-Fluff Cleanup:** Deterministic filler/stutter stripping, Personal Dictionary & Voice Snippets, and original clipboard restoration after auto-paste.
- **Fair Ownership Pricing:** Free download with **25 full dictations**. Lifetime Pro is **$19** during the Black Friday launch (**Nov 24–Dec 1, 2026**, 34% off **$29** regular price — no code needed) for up to **3 personal computers** with offline Ed25519 license verification (Windows included free once released).

## Downloads

Grab binaries from the [Releases](https://github.com/smolkapps/flowspeak-releases/releases) page or [smolkapps.com/flowspeak](https://smolkapps.com/flowspeak/):

| Platform | Artifact | Notes |
| --- | --- | --- |
| **macOS 12+** (Apple Silicon & Intel Universal) | `FlowSpeak-1.0.0-Universal.dmg` | Dev-signed (`arm64` Metal + `x86_64` AVX2) |
| **Linux** (`x86_64`) | `FlowSpeak-1.0.0-linux-amd64.tar.gz` | Standalone binary + `.desktop` installer |

### Verify Checksums

```bash
# macOS
shasum -a 256 -c SHA256SUMS.txt --ignore-missing

# Linux
sha256sum -c SHA256SUMS.txt --ignore-missing
```

### macOS First-Launch Gatekeeper Note

Current macOS builds are Developer-signed and awaiting Apple Developer ID notarization completion. Until notarized, macOS Gatekeeper may warn on first launch from an internet download. After dragging `FlowSpeak.app` into `/Applications`, either **Right-click → Open** in Finder or clear the download quarantine attribute:

```bash
xattr -dr com.apple.quarantine /Applications/FlowSpeak.app
```

### Linux Install

```bash
tar -xzf FlowSpeak-1.0.0-linux-amd64.tar.gz
cd flowspeak-1.0.0-linux-amd64
./install.sh
```

## Reporting Bugs & Feature Requests

Please use our [Issue Templates](https://github.com/smolkapps/flowspeak-releases/issues/new/choose) and include your OS version, FlowSpeak version, chosen trigger key / engine, and non-sensitive logs.
