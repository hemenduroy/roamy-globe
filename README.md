# Roamy Stupid

Puzzle tools and 3D globe for the Beast hunt. Built from beast_puzzle/locations.

**Live site:** https://hemenduroy.github.io/roamy-stupid/

---

## Pages

- **Home** — links to Globe and Car grid variants
- **Globe** — 41×3 route triplets (location → roamy → location) on a 3D globe
- **Car grid variants** — Trips by Car grid transformations for puzzle solving

---

## Updating the site

**Option A — Automatic:** Push to `beast_puzzle` (main). If the repo has a GitHub Action set up and the secret `ROAMY_STUPID_TOKEN` is configured, the action will sync and push to roamy-stupid so the page updates without running anything locally.

**Option B — Manual:** From beast_puzzle repo root run:

```bash
./locations/sync_globe_site.sh
cd roamy-stupid
git add .
git commit -m "Update site"
git push
```

Repo: [hemenduroy/roamy-stupid](https://github.com/hemenduroy/roamy-stupid)
