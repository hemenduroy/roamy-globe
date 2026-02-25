# Route Globe

Interactive 3D globe showing route triplets (location → roamy → location). Built from [beast_puzzle/locations](https://github.com).

**Live site:** https://YOUR_USERNAME.github.io/route-globe/ (after you create the repo and enable Pages)

---

## Host on GitHub Pages (first-time setup)

### 1. Create a new repo on GitHub

- Go to [github.com/new](https://github.com/new)
- **Repository name:** `route-globe` (or any name; the site will be `username.github.io/route-globe`)
- **Public**, no need to add README, .gitignore, or license (this folder already has files)
- Click **Create repository**

### 2. Push this folder as the repo

From your machine, in the folder that contains this README (e.g. `globe-site` or the repo root):

```bash
cd /path/to/globe-site   # or wherever this folder is
git init
git add .
git commit -m "Initial commit: route globe for GitHub Pages"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/route-globe.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username and `route-globe` with your repo name if different.

### 3. Turn on GitHub Pages

- In the repo: **Settings** → **Pages**
- **Source:** Deploy from a branch
- **Branch:** `main` (or `master`) → **/ (root)** → Save
- After a minute or two, the site will be at:

  **https://YOUR_USERNAME.github.io/route-globe/**

---

## Updating the site

After you change the globe or config in `beast_puzzle/locations`, refresh the live site by copying the built files and pushing:

```bash
# From beast_puzzle repo root (or use the sync script)
cp locations/route_globe.html globe-site/index.html
cp locations/route_config.json globe-site/
cp locations/earth_texture.jpg globe-site/
cd globe-site
git add .
git commit -m "Update globe"
git push
```

Or run the sync script from `beast_puzzle`: `./locations/sync_globe_site.sh`
