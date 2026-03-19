# AnitaProxy (Netlify Reverse Proxy)

This project configures Netlify to reverse proxy all routes to:

- `https://fireofmaat.wixsite.com/my-site-1`

## How It Works

The `netlify.toml` rewrite rule proxies every request:

- Incoming: `https://your-netlify-site.netlify.app/*`
- Proxied to: `https://fireofmaat.wixsite.com/my-site-1/*`

This is a `200` rewrite (reverse proxy), not a browser redirect.

## Files

- `netlify.toml`: Netlify config and proxy rewrite rule
- `public/index.html`: Placeholder publish file

## Deploy Using GitHub + Netlify

1. Create a new GitHub repository.
2. Push this folder to that repository.
3. In Netlify, choose **Add new site** -> **Import an existing project**.
4. Connect your GitHub account and select this repo.
5. Build settings:
   - Build command: *(leave empty)*
   - Publish directory: `public`
6. Deploy site.

## Optional: Custom Domain

1. In Netlify: **Site configuration** -> **Domain management**.
2. Add your custom domain.
3. Update DNS records as Netlify instructs.

## Important Notes

- Some Wix assets or scripts may use absolute URLs/cookies tied to Wix domains.
- If Wix changes headers or anti-bot protections, proxy behavior can be affected.
- Ensure your use complies with Wix terms and content ownership rules.

# AnitaFireofMaat

## Free Option: GitHub Pages Iframe Wrapper

If Netlify cost is a concern, you can host a free wrapper page with GitHub Pages.

### Files used

- `index.html`: iframe wrapper page
- `.nojekyll`: disables Jekyll processing

### Enable GitHub Pages

1. Push the latest changes to `main`.
2. In GitHub, open the repo settings.
3. Go to **Pages**.
4. Under **Build and deployment**, choose:
   - **Source**: Deploy from a branch
   - **Branch**: `main` and folder `/ (root)`
5. Save and wait for GitHub Pages URL to appear.

### Important Notes

- The browser URL stays on your GitHub Pages domain.
- Content is still loaded from Wix in an iframe.
- Some Wix features may behave differently inside iframes (cookies, popups, mobile interactions).
