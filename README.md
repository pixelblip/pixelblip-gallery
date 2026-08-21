# Pixelblip Gallery

Public gallery for Mode 2 paintings from the [art4evaminimal](https://github.com/pixelblip/art4evaminimal) paint app.

**Live site (after GitHub Pages is on):**  
https://pixelblip.github.io/pixelblip-gallery/

## What’s stored

Each FIN upload adds:

- `works/<id>/preview.png` — final image
- `works/<id>/piece.paint.json` — stroke history for PLAY
- an entry in `manifest.json`

Soft-delete moves a work into **Trash** (still in the repo). **Empty trash** removes those files for good.

## Publish this repo

```bash
cd pixelblip-gallery
git init -b main
git add .
git commit -m "Initial Pixelblip Gallery"
gh repo create pixelblip/pixelblip-gallery --public --source=. --remote=origin --push
```

Then: **Settings → Pages → Deploy from branch `main` / root**.

## Owner uploads / trash

In the Paint app, long-press **GAL** and paste a GitHub personal access token with **Contents: Read and write** on this repo only (fine-grained PAT recommended).

FIN then uploads the PNG + play sequence here. On the gallery site, tap **Owner** and paste the same token to trash / empty trash.
