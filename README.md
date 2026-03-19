# AnitaFireofMaat

This project uses a GitHub Pages iframe wrapper for:

- `https://fireofmaat.wixsite.com/my-site-1`

## How It Works

The root page embeds Wix inside an iframe so your GitHub Pages URL stays visible.

## Files

- `index.html`: root iframe wrapper (GitHub Pages)
- `public/index.html`: Netlify wrapper copy (optional)
- `.nojekyll`: disables Jekyll processing on GitHub Pages

## Deploy on GitHub Pages

1. Push the latest changes to `main`.
2. In GitHub, open repo **Settings** -> **Pages**.
3. Under **Build and deployment** choose:
   - **Source**: Deploy from a branch
   - **Branch**: `main` and folder `/ (root)`
4. Save and wait for the Pages URL.

## Important Notes

- Browser URL stays on your GitHub Pages domain.
- Content is still served by Wix inside an iframe.
- Some Wix features can behave differently in iframe contexts (cookies, popups, mobile interactions).

## Private + Public Mirror Workflow

This repo is configured with two remotes:

- `origin` = private repo (`git@github.com:Edelva01/AnitaFireofMaat.git`)
- `public` = public mirror (`git@github.com:Edelva01/AnitaFireofMaat_public.git`)

Use these commands:

1. Push private only:
   - `git push origin main`
2. Push public only:
   - `git push public main`
3. Push both:
   - `git push origin main; git push public main`
