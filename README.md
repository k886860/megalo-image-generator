# Megalo Image Generator Pro v1.43

**A production-oriented Chrome workflow for Google Cloud Vertex AI image generation and Veo video generation.**

[![Latest Release](https://img.shields.io/badge/Download-Latest_Release-2ea44f?style=for-the-badge)](https://github.com/k886860/megalo-image-generator/releases/latest)
![Version](https://img.shields.io/badge/version-1.43-2563eb?style=for-the-badge)
![Languages](https://img.shields.io/badge/UI-KO%20%7C%20EN%20%7C%20JA%20%7C%20ZH-7c3aed?style=for-the-badge)

[한국어](docs/TUTORIAL_KO.md) · [English](docs/TUTORIAL_EN.md) · [日本語](docs/TUTORIAL_JA.md) · [简体中文](docs/TUTORIAL_ZH_CN.md)

## What's New in v1.43

- Added `gemini-3.6-flash` as the primary text-processing engine.
- Added `gemini-3.5-flash-lite` as a lightweight text fallback.
- Added `gemini-3.1-flash-lite-image` for low-cost 1K image generation.
- Changed the default image engine to `gemini-3.1-flash-image`.
- Retained `gemini-3-pro-image` as the high-quality image engine.
- Removed discontinued Preview image models.
- Automatically migrates old Preview selections to `gemini-3.1-flash-image`.
- Preserves current Backend URL slots 1–10 when restoring older presets, character files, folder backups, or encrypted backups.
- Updated the bundled Cloud Run deployment source and redeployment scripts.

> Users upgrading from v1.42 must redeploy their Cloud Run backend before using the new engines.

## Download

Download `Megalo_Pro_v1.43_GitHub_Free_protected_20260724.zip` from the [latest Release](https://github.com/k886860/megalo-image-generator/releases/latest).

Do not download GitHub's automatically generated `Source code (zip)` or `Source code (tar.gz)` archives.

## Quick Install

1. Extract the release ZIP completely.
2. Open `chrome://extensions`.
3. Enable **Developer mode**.
4. Click **Load unpacked**.
5. Select one language folder: `ko_KR/extension`, `en_US/extension`, `ja_JP/extension`, or `zh_CN/extension`.
6. Deploy or connect the v1.43 Cloud Run backend.
7. Enter the matching Backend URL and Google Cloud Project ID.

## Model Notes

| Purpose | Model |
|---|---|
| Default image engine | `gemini-3.1-flash-image` |
| High-quality image engine | `gemini-3-pro-image` |
| Low-cost 1K image engine | `gemini-3.1-flash-lite-image` |
| Primary text engine | `gemini-3.6-flash` |
| Lightweight text fallback | `gemini-3.5-flash-lite` |

`gemini-3.1-flash-lite-image` supports 1K only. Use another image model for 2K or 4K generation.

## Upgrading from v1.42

1. Install v1.43 in a new folder.
2. Redeploy the Cloud Run backend using the v1.43 script.
3. Enter the newly deployed Backend URLs.
4. Restore older presets and character files if needed.

Restoring old files does not overwrite the Backend URLs currently configured in v1.43.

## Release Integrity

`23AC035B71BF7E43B43EB62D255CA280FB1E01D9236FA2FD58E0AD192C876C53`
