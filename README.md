# Breu Software

The public website for Breu Software, published at [www.breusoftware.com](https://www.breusoftware.com).

The site is deliberately build-free: its HTML, design-system files, and image assets live in `docs/` and can be served by any static web server.

## Preview locally

From the repository root, run:

```sh
python3 -m http.server 8000 --directory docs
```

Then open [http://localhost:8000](http://localhost:8000).

## Publish

The GitHub Pages workflow in `.github/workflows/pages.yml` deploys `docs/` whenever relevant files are pushed to `main`. It can also be started manually from the repository's Actions page.

The custom domain is declared in `docs/CNAME`. DNS should point:

- `breusoftware.com` to GitHub Pages' four apex `A` records.
- `www.breusoftware.com` to `breusoftware.github.io` with a `CNAME` record.

Do not add secrets, private builds, or source-only project material beneath `docs/`; everything there is published publicly.
