# Roamy Globe

Interactive 3D globe showing route triplets (location → roamy → location). Built from [beast_puzzle/locations](https://github.com).

**Live site:** https://hemenduroy.github.io/roamy-globe/

---

## Host on GitHub Pages (first-time setup)

### 1. Push this folder to the repo

Repo: [hemenduroy/roamy-globe](https://github.com/hemenduroy/roamy-globe)

```bash
cd roamy-globe   # or full path to this folder
git init
git add .
git commit -m "Initial commit: route globe for GitHub Pages"
git branch -M main
git remote add origin git@github.com:hemenduroy/roamy-globe.git
git push -u origin main
```

(Using SSH so you won’t be prompted for a password.)

### 2. Turn on GitHub Pages

- In the repo: **Settings** → **Pages**
- **Source:** Deploy from a branch
- **Branch:** `main` → **/ (root)** → Save
- After a minute or two: **https://hemenduroy.github.io/roamy-globe/**

---

## Updating the site

After changing the globe or config in `beast_puzzle/locations`:

```bash
# From beast_puzzle repo root
./locations/sync_globe_site.sh
cd roamy-globe
git add .
git commit -m "Update globe"
git push
```
