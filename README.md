# EDGI902 A3 — GitHub Pages hosting package

Three files in this folder are everything you need. Each HTML file is fully
self-contained (no folders of assets to keep alongside it).

```
index.html      ← landing page; links to both artefacts. THIS is the link you submit.
prototype.html  ← the working prototype (fully offline-bundled)
companion.html  ← the evidence-architecture companion (loads Google Fonts online)
.nojekyll       ← empty file; tells GitHub to serve files as-is (leave it in)
```

## Publish it (≈5 minutes)

1. On github.com, create a **new repository** — e.g. `edgi902-a3`.
   Make it **Public** (free GitHub Pages requires public, or GitHub Pro for private).
2. Upload the **contents of this folder** (not the folder itself) to the repo root:
   `index.html`, `prototype.html`, `companion.html`, `.nojekyll`.
   (Drag-drop works: repo → "Add file" → "Upload files".)
3. Repo → **Settings** → **Pages**.
   - **Source:** "Deploy from a branch"
   - **Branch:** `main`  ·  **Folder:** `/ (root)`  → **Save**
4. Wait ~1–2 minutes. The page URL appears at the top of the Pages settings:
   `https://<your-username>.github.io/edgi902-a3/`
   **That is the single link you put in your A3 submission.**

## Good to know

- **Submit the `index.html` URL** (the repo root URL above). It reaches both
  artefacts, so one link covers everything.
- **Filenames matter.** These are deliberately lowercase, no spaces, no `·`.
  Don't rename them to versions with spaces/special characters — GitHub Pages
  serves them but the URLs become brittle (`%20`, `%C2%B7`).
- **First load can lag ~60s** after you enable Pages or push a change — GitHub
  is building the site. A hard refresh (Cmd/Ctrl+Shift+R) clears stale caches.
- **`companion.html` fetches fonts from Google Fonts**, so it needs network on
  first open (true on GitHub Pages). If a font is slow it falls back gracefully
  to Helvetica/Georgia — content is never blocked. `prototype.html` is fully
  offline-bundled and needs nothing external.
- **Updating later:** re-upload the changed file to the repo (overwrite) and
  Pages redeploys automatically in a minute or two.
- **No build step, no Jekyll.** The `.nojekyll` file keeps GitHub from trying to
  process the site — plain static HTML, served exactly as written.
