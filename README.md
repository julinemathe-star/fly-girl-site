# Deploying Fly Girl Events & Design to Netlify

This is a pre-built static site — no build step, no dependencies to install.
Everything in this folder is served exactly as-is.

## Option A — Drag and drop (fastest)

1. Unzip this file.
2. Go to https://app.netlify.com/drop
3. Drag the unzipped folder (the one containing `index.html`) into the browser window.
4. Netlify assigns a temporary URL immediately (e.g. `random-name-123.netlify.app`).

## Option B — Connect to Git (better for future updates)

1. Push this folder's contents to a GitHub/GitLab/Bitbucket repository.
2. In Netlify: **Add new site → Import an existing project**.
3. Connect the repository.
4. Build settings: leave the build command **blank**, set publish directory to `.` (repository root).
5. Deploy.

## Connecting the flygirl.events domain

1. In the Netlify dashboard: **Domain settings → Add a domain** → enter `flygirl.events`.
2. Netlify will show DNS records to add at your domain registrar (either point nameservers to Netlify, or add the A/CNAME records it provides).
3. Netlify issues a free SSL certificate automatically once DNS propagates (usually within a few hours).

The sitemap, robots.txt, and all canonical/Open Graph/schema URLs already point to `https://flygirl.events` — no changes needed there once the domain is connected.

## What's included

| Path | Purpose |
|---|---|
| `index.html` + 7 other pages | The site |
| `styles.css` / `main.js` | Shared styles and behavior |
| `video/hero-cinemagraph.mp4` | Homepage hero background (4.9MB, autoplays muted/looped) |
| `images/hero-cinemagraph-poster.jpg` | Static fallback shown before video loads, and permanently for visitors with reduced-motion preferences enabled |
| `images/luxury-destination-wedding-ceremony-sunset.jpg` | Retained but currently unused on-page — kept in case you want it back |
| `icons/` | Favicon set |
| `sitemap.xml`, `robots.txt`, `site.webmanifest` | SEO / PWA metadata |
| `netlify.toml` | Cache headers — no action needed, Netlify reads this automatically |

## After going live

- Submit `https://flygirl.events/sitemap.xml` to Google Search Console and Bing Webmaster Tools.
- Add your real Instagram/Pinterest/Facebook URLs to the footer and schema `sameAs` whenever they're ready (flagged as outstanding in earlier review).
