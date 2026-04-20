# personal-website

Source for [chrisdulhanty.com](https://chrisdulhanty.com) — a static site
with no build step. Just HTML and CSS.

## Files

- `index.html` — Home / about page
- `publications.html` — Publications list
- `media.html` — Press coverage
- `styles.css` — Styles (light + dark modes; Vollkorn serif)
- `assets/images/` — Profile photo and press-outlet logos
- `assets/fonts/` — Vollkorn + Fira Code (self-hosted woff2)
- `CNAME` — Custom domain for GitHub Pages
- `.nojekyll` — Disables Jekyll processing on GitHub Pages
- `robots.txt`, `sitemap.xml` — SEO basics
- `*.webarchive` — Safari archives of the original WordPress site, kept as
  reference. Not served as part of the site.

## Local preview

Any static file server works, e.g.:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Hosting (free)

The repo is set up for **GitHub Pages** with a custom domain:

1. Push this branch to `main` on GitHub.
2. In the repo: **Settings → Pages**, set *Source* to `Deploy from a branch`,
   *Branch* to `main` / `/ (root)`.
3. GitHub Pages reads `CNAME` and will serve the site at `chrisdulhanty.com`.
4. At your DNS provider, point the domain at GitHub Pages:
   - `A` records for the apex `chrisdulhanty.com` →
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `<your-github-username>.github.io`
5. Back in **Settings → Pages**, enable **Enforce HTTPS** once the cert is
   provisioned.

Alternatives (also free, similar flow):
[Cloudflare Pages](https://pages.cloudflare.com/),
[Netlify](https://www.netlify.com/),
[Vercel](https://vercel.com/).
