# Scalar Yield

Markets, macro and money — analysed, capitalised, maximised.

**Tagline:** ANALYSE · CAPITALISE · MAXIMISE

## Stack

- Static site, deployed as Cloudflare Workers static assets
- `public/` is the entire build output — no build step required
- No framework, no bundler, no runtime dependencies

## Deploy

```bash
npx wrangler deploy
```

- `run_worker_first` must stay **off** — static asset requests are free and
  unmetered; enabling it makes every request billable and caps you at
  100,000 requests/day.
- Custom domain attaches in the Cloudflare dashboard, not in this file.

## Brand assets

| File | Use |
| --- | --- |
| `public/favicon.ico` | Browser tab |
| `public/brand/icon-*.png` | Home screen, PWA, app icons |
| `public/brand/03-og-1200x630.png` | Link previews |
| `public/brand/04-header-1500x500.png` | Site header / social banner |

Palette: cream `#F8F0E3` · off-white `#FFFDF8` · ink `#241610` · terracotta
`#BC5B33` · deep terracotta `#9C4522` · tan `#E8D5B8` · muted brown `#7A6A58`.
Fonts: Playfair Display (display) + Inter (text).

## Contact

`hello@scalaryield.com` — pending setup.

## Rules

- Never commit credentials, tokens or secrets.
- Never store built pages in this repo — build output goes straight to Cloudflare.
- Every page needs a unique title, a unique 120–155 character description,
  one `<h1>`, an absolute self-canonical, and valid JSON-LD.
