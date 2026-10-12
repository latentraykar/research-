# Kaustubh x Lauki

All the research, scripts, frameworks, prompts and files from the Kaustubh x Lauki hub, in one static site.

Live: https://latentraykar.github.io/research-/

## What's inside

```
index.html        the hub page (start here)
t/                text pages: scripts, frameworks, references
pages/            the bigger research pages (higgsfield 200 reels, creative director pathway, jev brief, ...)
f/                downloadable files (.md, .skill, .zip)
m/                media (demo video + poster)
.nojekyll         tells GitHub Pages to serve files as they are
```

It's plain HTML. No build step, nothing to install.

## 1. Get the code on your machine

You need git installed. Check with `git --version`.

First time (clone):

```bash
git clone https://github.com/latentraykar/research-.git
cd research-
```

Already cloned? Get the latest changes (pull):

```bash
cd research-
git pull
```

Want to look at it locally? Just open `index.html` in your browser.

## 2. Push it to another repo

1. On GitHub, click **+ > New repository**. Give it a name, leave it **empty** (no README, no .gitignore, no license), and click **Create repository**.
2. Copy the new repo's URL, e.g. `https://github.com/<your-username>/<new-repo>.git`.
3. In your `research-` folder, add it as a second remote and push:

```bash
git remote add other https://github.com/<your-username>/<new-repo>.git
git push other main
```

That's it, the new repo now has everything. Later, to send fresh changes there too:

```bash
git pull            # get latest from this repo
git push other main # send it to the other repo
```

Want the other repo to be the main one instead? Swap the remote:

```bash
git remote set-url origin https://github.com/<your-username>/<new-repo>.git
git push -u origin main
```

If git asks for a password, use a GitHub personal access token (GitHub > Settings > Developer settings > Personal access tokens), not your account password. Or sign in once with the GitHub Desktop app / `gh auth login`.

## 3. Put the other repo live on GitHub Pages

1. Open the new repo on GitHub and go to **Settings > Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Pick branch **main** and folder **/ (root)**, then click **Save**.
4. Wait a minute or two, then refresh the page. The link shows up at the top: `https://<your-username>.github.io/<new-repo>/`
5. Open it. You should see the hub.

Notes:
- The repo must be **public** for free GitHub Pages.
- Every `git push` to `main` updates the live site automatically within a minute or two. Check progress in the repo's **Actions** tab.
- Page not updating? Hard refresh (Cmd+Shift+R).

## Editing

- Change text on the hub: edit `index.html`.
- Add a file: drop it in `f/`, link it from `index.html` as `f/your-file.pdf`.
- Then:

```bash
git add .
git commit -m "what you changed"
git push
```
