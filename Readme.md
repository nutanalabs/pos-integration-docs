This repo contains the documentation related to pos-integration. It is a static HTML site (exported pages plus `index.html`) published with GitHub Pages at [https://docs.ownly.food](https://docs.ownly.food).

## How do we launch?

From the repo root, serve the files with any static file server. Relative links between pages need HTTP, so open the site through the server instead of double-clicking `index.html`.

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000). `index.html` is the home page; it links to Guides and API Documentation.

## How do we deploy?

GitHub Pages publishes the root of `master` automatically. There is no separate build step.

1. Commit the updated HTML (and any new assets) on a branch and open a pull request.
2. Merge the pull request into `master`.
3. GitHub Pages builds and publishes the site. The live URL is [https://docs.ownly.food](https://docs.ownly.food).

`CNAME` must stay `docs.ownly.food`. That file is what maps the custom domain. HTTPS is enforced on the Pages site.
