# De Mayo AI Movie Studio

## Build 1.5 — True AI Scene and Audio Generator

Build 1.5 adds real AI-generated landscape scene images and downloadable Tagalog MP3 dialogue. Generated media is inserted into the timeline automatically and captured in the exported movie. API credentials remain in the included Cloudflare Worker secret, never in GitHub Pages.

### Secure Worker setup

1. Deploy the `worker` directory with Cloudflare Workers.
2. Add the secret `OPENAI_API_KEY` to the Worker.
3. Confirm `ALLOWED_ORIGIN` in `worker/wrangler.toml` matches `https://romerdemayo.github.io`.
4. Paste the deployed `workers.dev` address into **Secure AI connection** in the app and test it.

The default economical models are `gpt-image-1-mini` (low-quality 1536×1024 JPEG) and `gpt-4o-mini-tts` (MP3). API usage is paid by the connected OpenAI account and is not unlimited or free.

## Build 1.4 — Hybrid Voice Studio

Build 1.4 adds automatic browser-based Tagalog dialogue previews, voice selection, speed and pitch controls, Character Card speed matching, per-scene voice tests, and automatic dialogue timing. The app continues to accept uploaded audio for the final rendered MP4/WebM because browser speech synthesis cannot be captured reliably into a downloaded video.

## Build 1.3 — Character Continuity

Build 1.3 adds reusable Character Cards for consistent AI filmmaking. Elias, Anna and The Guardian are included as starter actors. Each card locks facial features, body appearance, signature clothing, personality and voice direction. Cards can be reused across movies, assigned per scene, imported, exported, edited, duplicated or deleted.

Scene prompts are rebuilt from the selected character cards so every generated image receives the same identity description. Character cards and movie projects are stored locally in the browser.

A mobile-friendly GitHub Pages app for planning and rendering original Tagalog AI-assisted movies. Build 1.2 adds a local media timeline, scene images and audio, animated cinematic previews, burned-in subtitles, and browser-based YouTube video rendering.

## Run locally

Open `index.html` directly, or serve the folder with any static web server.

## Deploy with GitHub Pages

Upload these files to a repository, then enable **Settings → Pages → Deploy from branch → main / root**.

## Privacy and costs

Build 1.2 works entirely in the browser and does not use paid APIs. Projects are stored in the browser's local storage. Selected media stays on the current device and is not uploaded. Download a JSON backup before clearing browser data or changing devices.

## Roadmap

- Build 1.5: secure optional AI image and voice provider connections
- Build 1.6: vertical YouTube Shorts exporter and thumbnail creator

## Copyright

Copyright © 2026 Romer De Mayo. All rights reserved. See [LICENSE](LICENSE). Users retain ownership of their original movie projects and remain responsible for rights to media they upload.
