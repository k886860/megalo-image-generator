# Megalo Image Generator Pro v1.43 Beginner Tutorial

## Download and Install

Download `Megalo_Pro_v1.43_GitHub_Free_protected_20260724.zip` from **Releases**. Do not use GitHub's automatically generated source-code archive.

Extract the ZIP, open `chrome://extensions`, enable **Developer mode**, click **Load unpacked**, and select `en_US/extension`.

## Upgrade the Cloud Run Backend

v1.43 adds new Gemini engines. Users upgrading from v1.42 must redeploy the backend using the bundled v1.43 redeployment script.

1. Open `SCENE`.
2. Expand `Vertex / Backend Settings`.
3. Enter the Project ID.
4. Generate and copy the redeployment script.
5. Run it in Google Cloud Shell.
6. Paste the resulting Cloud Run URL into the matching Backend URL slot.

## Engines in v1.43

- Default image: `gemini-3.1-flash-image`
- High-quality image: `gemini-3-pro-image`
- Low-cost 1K image: `gemini-3.1-flash-lite-image`
- Primary text: `gemini-3.6-flash`
- Lightweight text fallback: `gemini-3.5-flash-lite`

Discontinued Preview image models were removed. Old Preview selections are migrated automatically. Flash Lite Image supports 1K only.

## Restore Older Presets and Characters

v1.43 preserves the currently configured Backend URL slots 1–10 when importing old presets, character files, folder backups, or encrypted backups. Character, scene, reference, Project ID, and generation settings still restore normally.

## First Test

Use one reference image, one scene, one output, and 1K or 2K. For Flash Lite Image, use 1K only.

## Troubleshooting

- **404 Model not found:** Redeploy the v1.43 backend and verify model availability and location.
- **403 Permission denied:** Check Vertex AI API, IAM, model access, and Project ID.
- **429 Resource exhausted:** Reduce concurrency, retries, and batch size.
- **Failed to fetch:** Check the Backend URL and Cloud Run status.
