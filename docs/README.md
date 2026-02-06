# Small Music Converter

This folder is designed to be published with GitHub Pages using the `docs/`
root. The page loads quickly by only fetching audio when you click Play.

## Local converter (recommended)

GitHub Pages does not set the security headers required by ffmpeg.wasm.
For in-browser conversion, run the local server below in Chrome or Firefox.

```bash
node tools/serve-coop.js
```

Then open `http://localhost:8080/` and use the Opus converter.

## Steps

1. Create `docs/audio/` and put your files there.
2. Update `docs/manifest.json` to list your clips.
3. In GitHub, go to Settings → Pages.
4. Source: Deploy from a branch. Branch: `main`. Folder: `/docs`.
5. Save, then open the provided URL.

## Recommended formats

- Opus (`.opus`) for smallest size.
- AAC (`.m4a`) as a fallback for Safari.

## Manifest format

Each entry should have a title and one or more sources:

```json
{
  "title": "My Clip",
  "sources": [
    { "src": "audio/my-clip.opus", "type": "audio/ogg; codecs=opus" },
    { "src": "audio/my-clip.m4a", "type": "audio/mp4" }
  ]
}
```
