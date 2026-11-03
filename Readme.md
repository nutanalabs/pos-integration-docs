This repo contains the documentation related to pos-integration. It is a static HTML site published with GitHub Pages at [https://docs.ownly.food](https://docs.ownly.food).

## Versions

`index.html` is the single entry point and is the latest version (**v2**): one self-contained page with guides, every endpoint and the change log. The previous documentation (**v1**, the exported Notion pages) is kept as it was: `v1/index.html` is its landing page and the exported pages stay in their original folder. It is reachable from the version switcher in the header, from the footer, or directly at `/v1`. `/v2` simply redirects to the base URL, so it always serves the latest version.

```
index.html   v2 (latest), entry point
v2/index.html   redirects to the base URL (always the latest)
v1/index.html   v1 landing page (links to the exported pages below)
Restaurant Menu & Order Management Integration …/   v1 exported pages
CNAME        custom domain
```

## How do we launch?

From the repo root, serve the files with any static file server. Relative links between pages need HTTP, so open the site through the server instead of double-clicking `index.html`.

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000). `index.html` is the home page (v2); the version switcher links to `v1/`.

## How do we deploy?

GitHub Pages publishes the root of `master` automatically. There is no separate build step.

1. Commit the updated HTML (and any new assets) on a branch and open a pull request.
2. Merge the pull request into `master`.
3. GitHub Pages builds and publishes the site. The live URL is [https://docs.ownly.food](https://docs.ownly.food).

`CNAME` must stay `docs.ownly.food`. That file is what maps the custom domain. HTTPS is enforced on the Pages site.
