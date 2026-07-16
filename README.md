# Megalo Image Generator Pro v1.42

**A production-oriented Chrome workflow for Google Cloud Vertex AI image generation and Veo video generation.**

[![Latest Release](https://img.shields.io/badge/Download-Latest_Release-2ea44f?style=for-the-badge)](https://github.com/k886860/megalo-image-generator/releases/latest)
[![Video Tutorial](https://img.shields.io/badge/Watch-Video_Tutorial-red?style=for-the-badge)](https://www.youtube.com/watch?v=ZIppbRt9u2I)
![Version](https://img.shields.io/badge/version-1.42-2563eb?style=for-the-badge)
![Languages](https://img.shields.io/badge/UI-KO%20%7C%20EN%20%7C%20JA%20%7C%20ZH-7c3aed?style=for-the-badge)

[한국어](docs/TUTORIAL_KO.md) · [English](docs/TUTORIAL_EN.md) · [日本語](docs/TUTORIAL_JA.md) · [简体中文](docs/TUTORIAL_ZH_CN.md)

[![Megalo Image Generator video tutorial](https://img.youtube.com/vi/ZIppbRt9u2I/hqdefault.jpg)](https://www.youtube.com/watch?v=ZIppbRt9u2I)

> Megalo Image Generator is free to download. Google Cloud Vertex AI, Veo, Cloud Run, storage, and network usage may create charges on the user's own Google Cloud account.

## What It Does

Megalo manages the workflow around Vertex AI generation: reference images, multiple projects, batch scenes, retries, recovery, cost tracking, result organization, splitting, merging, and saving. It does not include free Google Cloud usage or bypass provider policies.

| Area | Main capabilities |
| --- | --- |
| Multi-project generation | Up to 10 configurable backend and Project ID slots, ordering, rotation, reserve slots, and concurrent work |
| Reference workflow | Flexible 1–14 reference image slots, character/reference sets, multi-person and specialized reference modes |
| Image production | Batch scene generation, per-scene regeneration, retry control, prompt presets, queue and cancellation controls |
| Recovery and history | Crash recovery, generation history, original restoration, backup and restore workflows |
| Result tools | Sorting, sequential naming, JPG storage, automatic/manual split, merge, crop, batch save, and external-folder rename |
| Cost protection | Slot statistics, credit balance tracking, low-balance locking, retry budgets, session and batch limits |
| Video workflow | Multi-slot Vertex AI Veo generation, image guidance, continuation workflow, preview, and per-slot saving |
| Languages | Korean, English, Japanese, and Simplified Chinese UI and tutorials |

## Download

1. Open the [latest Release](https://github.com/k886860/megalo-image-generator/releases/latest).
2. Download **`Megalo_Pro_v1.42_GitHub_Free_protected_20260716.zip`**.
3. Verify the SHA-256 value shown below.
4. Extract the ZIP completely before installation.

> **Do not download GitHub's automatically generated `Source code (zip)` or `Source code (tar.gz)`. Those archives are not the installable application package.**

## Quick Install

1. Open `chrome://extensions` in Google Chrome.
2. Enable **Developer mode**.
3. Click **Load unpacked**.
4. Select one language folder's extension directory:
   - Korean: `ko_KR/extension`
   - English: `en_US/extension`
   - Japanese: `ja_JP/extension`
   - Simplified Chinese: `zh_CN/extension`
5. Follow the tutorial to deploy or connect the Cloud Run backend.
6. Enter the Backend URL and Google Cloud Project ID.
7. Start with one reference image, one scene, and one output to verify the setup.

## Tutorials

- [한국어 초보자 튜토리얼](docs/TUTORIAL_KO.md)
- [English beginner tutorial](docs/TUTORIAL_EN.md)
- [日本語初心者チュートリアル](docs/TUTORIAL_JA.md)
- [简体中文入门教程](docs/TUTORIAL_ZH_CN.md)
- [Video tutorial on YouTube](https://www.youtube.com/watch?v=ZIppbRt9u2I)

## Before a Large Batch

- Confirm the selected Project ID, backend URL, model access, region, quota, and billing.
- Test identity and costume consistency with a small generation first.
- Set slot credit balances and generation/retry budgets.
- Keep history and backups enabled, but monitor browser memory usage.
- Remember that retries and post-generation safety failures may still consume provider resources.
- Follow Google Cloud, Vertex AI, and applicable local policies.

## Troubleshooting

- **403 / Permission denied:** Check the Project ID, Vertex AI API, IAM roles, model access, and backend service account.
- **429 / Resource exhausted:** Reduce concurrency and retries, wait for quota recovery, or use another authorized project.
- **Failed to fetch:** Verify the complete Backend URL, Cloud Run deployment, public access, CORS, and network connection.
- **Reference mismatch:** Test fewer references and a shorter scene prompt before increasing batch size.
- **Browser memory pressure:** Save results regularly and use the built-in JPG/history/recovery controls.

For detailed instructions, open the tutorial for your language or report a reproducible problem through [GitHub Issues](https://github.com/k886860/megalo-image-generator/issues).

## Release Integrity

Protected ZIP SHA-256:

`3BFAEB574A730137A8FDAE230E9B1D8C57A706A41D5E0C3B251702035F557EF3`

## Project Links

- [Latest release](https://github.com/k886860/megalo-image-generator/releases/latest)
- [Video tutorial](https://www.youtube.com/watch?v=ZIppbRt9u2I)
- [Issue tracker](https://github.com/k886860/megalo-image-generator/issues)
