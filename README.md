# Elluryen site

Static site for Elluryen (https://www.tiktok.com/@elluryen). No build step: Cloudflare serves the files in `public/` as they are. Same setup as `Buyseech/seopack-site-` and `Buyseech/buyseech-site`.

## Where things are

- `public/index.html`: placeholder page only (marked noindex) until the real site is built
- `public/404.html`, `robots.txt`, `_headers`: standard site files
- `wrangler.jsonc`: tells Cloudflare to publish the `public/` folder

## Cloudflare settings

- Live at: https://elluryen-site.bajsic.workers.dev (until buyelluryen.com is connected)
- Cloudflare account: Bajsic@gmail.com's Account (Worker `elluryen-site`)
- Connected to this repo through Cloudflare Workers Builds: every push to `main` deploys
- Build command: none
- Deploy command: `npx wrangler deploy`

## Before launch

- `robots.txt` currently blocks search engines and the placeholder is noindex; switch both when the real site goes live, and add `sitemap.xml`
- Add buyelluryen.com to Cloudflare, then attach it as a custom domain (Workers → elluryen-site → Settings → Domains & Routes)
