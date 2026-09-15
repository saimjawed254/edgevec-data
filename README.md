# EdgeVec Data Repository
This repository is used by GitHub Pages to serve the static JSON files
that power the EdgeVec browser-side vector search.

## Contents
- `centroids.json` — The cluster centroid map (downloaded by the browser first)
- `bucket_0.json` through `bucket_99.json` — Static document buckets by semantic cluster

## How to Regenerate
Run `build.py` in the `edgevec/build/` directory. It will overwrite the files in this folder.

## Deployment
1. Push this folder's contents to your `edgevec-data` GitHub repository.
2. Go to Settings → Pages → Select `main` branch → Save.
3. Update `CDN_BASE_URL` in `edgevec-ui/src/search.js` with your GitHub Pages URL.
