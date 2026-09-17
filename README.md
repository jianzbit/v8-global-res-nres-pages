# V8 Global RES/NRES Floorspace Dashboard

Standalone GitHub Pages bundle for the interactive V8 Marimo WebAssembly dashboard.

## Contents

- `index.html` — read-only interactive WASM dashboard
- `assets/` — generated Marimo browser runtime assets required by `index.html`
- `public/app_data/` — final V8 dashboard tables only
- `.nojekyll` — prevents GitHub Pages Jekyll processing
- `.github/workflows/deploy-pages.yml` — manual GitHub Pages deployment workflow

No GFA source code, raw GHS-BUILT-V rasters, or source datasets are included.

## Local preview

Serve the bundle over HTTP; do not open `index.html` with `file://`:

```bash
python -m http.server --directory . 8765
```

Open <http://127.0.0.1:8765/>.

## GitHub Pages

Create a new repository in your personal GitHub account, copy this bundle into
it, and push it. In repository **Settings → Pages**, select **GitHub Actions**
as the source. Then run **Actions → Deploy V8 dashboard to GitHub Pages → Run
workflow**.

For a repository named `v8-global-res-nres-pages` under account `YOUR-USER`,
the project-site URL will be:

```text
https://YOUR-USER.github.io/v8-global-res-nres-pages/
```

The workflow is manual and is not run by this bundle preparation.
