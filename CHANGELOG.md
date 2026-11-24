# Changelog

All notable changes to FlowSpeak releases are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-11-24

### Added
- **Liquid Glass Interface (Default):** Translucent Liquid Glass dashboard and floating recording HUD (`NSGlassEffectView` on macOS 26+ with `NSVisualEffectView` vibrancy back to macOS 12), automatic `Reduce Transparency` / high-contrast solid fallback, and an explicit **Interface Style** toggle (`Liquid Glass (Default)` / `Classic Solid`) in `Settings → Appearance`.
- **Local & Hybrid Speech Engines:** In-process static `whisper.cpp v1.9.5` with Apple Silicon Metal + Accelerate, Intel `x86_64` AVX2, Linux `x86_64`, plus optional Groq / OpenAI / OpenAI-compatible LAN API fallback.
- **Resumable Model Manager:** HTTP `Range` resumable Whisper GGML downloads with SHA-256 verification and automatic first-run `ggml-base.en.bin` onboarding.
- **Push-to-Talk Engine:** Hold `Ctrl` (Either / Left / Right), `Fn`/Globe, or Right `Option` with smart chord cancellation (`Ctrl+C`, `Ctrl+Click`), double-tap hands-free mode, and `Esc` abort.
- **Deterministic Cleanup & Snippets:** Zero-latency filler removal, stutter cleanup, Personal Dictionary, Voice Snippets, optional Ollama / API polish, and clipboard-preserving paste.
- **Trial & Offline Pro Licensing:** 25 full free dictations followed by offline Ed25519 license activation (`FS-XXXX-XXXX-XXXX-XXXX`, up to 3 personal computers).
