# Megalo Image Generator Pro v1.42 Beginner Tutorial

This guide is for users who are new to Chrome extensions, Google Cloud, and Vertex AI.

## 1. Before You Start

The application is free. Image and video generation runs through your own Google Cloud project, so Vertex AI and Cloud Run charges may apply.

For the first test, use only:

- One reference image
- One scene
- One output image
- 1K or 2K resolution

## 2. Download And Install

Download `Megalo_Pro_v1.42_GitHub_Free_protected_20260716.zip` from this repository's **Releases** page. Do not download GitHub's automatically generated `Source code (zip)` file.

Extract the ZIP completely, then:

1. Open `chrome://extensions` in Chrome.
2. Enable **Developer mode**.
3. Click **Load unpacked**.
4. Select `en_US/extension`.

Other language folders are `ko_KR/extension`, `ja_JP/extension`, and `zh_CN/extension`.

## 3. Prepare Google Cloud

You need a Google Cloud project with billing and Vertex AI access. Enter the **Project ID**, not the display name.

![Find the Project ID](assets/gcp_01_project_id.png)

The deployment may require Vertex AI, Cloud Run Admin, Cloud Build, Artifact Registry, and Service Usage APIs.

## 4. Deploy The Cloud Run Backend

1. Open the `SCENE` workspace.
2. Expand `Vertex / Backend Settings` and configure slot 1.
3. Enter an alias and your Project ID.
4. Open the automatic backend redeployment script section.
5. Create and copy the script.
6. Open Google Cloud Shell and run the copied script.

![Run the deployment](assets/gcp_04_deploy_commands.png)

When deployment finishes, copy the `https://` Cloud Run service URL.

![Cloud Run service URL](assets/gcp_05_service_url.png)

Paste it into the same slot's Backend URL field. The Project ID and Backend URL must belong to the same project.

## 5. Add Reference Images

The default reference roles are:

| Slot | Role |
|---|---|
| 1 | Face and hair identity |
| 2 | Front full-body and outfit |
| 3 | Side profile and silhouette |
| 4 | Back view and rear details |
| 5 | Face and costume reinforcement |

All five are optional. One face reference is enough for a connection test. Confirm that the actual preview image appears before generation.

## 6. Generate The First Image

Example system prompt:

```text
One adult character. Preserve the same face and hairstyle as the uploaded reference.
Modern high-resolution live-action photography. No text, logo, or watermark.
```

Example scene prompt:

```text
[Scene] The adult character stands comfortably in a bright indoor studio and looks toward the camera. Natural full-body framing and soft lighting.
```

Select the aspect ratio, use 1K or 2K, set the image count to one, verify the final prompt preview, then click the automatic generation request button.

Do not repeatedly click the generation button while a request is running.

## 7. Review And Save

Use the `SAVE` workspace to inspect, reorder, regenerate, delete, and save results. Split-screen images can be processed with automatic or manual split tools. Saved output uses JPEG storage to reduce memory usage.

## 8. Cost And Recovery

Before a large batch, configure slot credit values and the Generation Safety Center.

- Batch budget: estimated limit for one generation batch
- Session budget: accumulated limit for the current session
- Emergency backup: preserves recovery information when memory use becomes unsafe

After a Chrome crash, reopen the extension and check crash recovery and generation history before clearing browser data.

## 9. Troubleshooting

- **403 Permission Denied:** Check Vertex AI API, model access, Project ID, and the Cloud Run service account role.
- **429 Resource Exhausted:** Reduce concurrent slots, retries, and batch size, then wait before retrying.
- **Failed to fetch:** Check the Backend URL and confirm that the Cloud Run service is deployed and reachable.
- **Weak reference fidelity:** Shorten conflicting prompts and test with fewer references and a simpler scene.
- **Out of memory:** Close unused tabs, use smaller batches, save results, and restart Chrome.

## 10. Updating

Download the next Release into a new folder. Back up presets, characters, reference sets, and results before switching the unpacked extension folder.
