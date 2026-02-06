# Small Music Converter

This folder is designed to be published with GitHub Pages using the `docs/`
root. The page includes an in-browser Opus converter and a fast-loading
audio library that only fetches files when you click Play.

## Steps

1. Create `docs/audio/` and put your files there.
2. Update `docs/manifest.json` to list your clips.
3. In GitHub, go to Settings → Pages.
4. Source: Deploy from a branch. Branch: `main`. Folder: `/docs`.
5. Save, then open the provided URL.

## Converter notes

- The Opus converter runs fully in the browser using ffmpeg.wasm.
- Large files can be slow or memory-heavy depending on your device.

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
