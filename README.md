# Viktoriia Balykina — Résumé Site

A single-page personal résumé website, part of my SDET portfolio. It's plain HTML and CSS with no frameworks and no build step.

## Structure

```
index.html                      # the page
styles.css                      # styles (light/dark theme, print styles)
.github/workflows/deploy.yml    # GitHub Pages deployment
```

Key elements have `data-testid` attributes, so the planned E2E test suite has stable selectors to target.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then go to http://localhost:8000.

## Deployment

Every push to `main` (including merged pull requests) deploys the site to GitHub Pages using the [`deploy.yml`](.github/workflows/deploy.yml) workflow. You can also start it manually from the **Actions** tab.

One-time setup: in the repository, go to **Settings → Pages → Build and deployment → Source** and select **GitHub Actions**.

The site will be available at `https://<username>.github.io/<repo-name>/`.

## Roadmap

- [ ] Fill in About, responsibilities and skills
- [ ] E2E test suite for this site
- [ ] Run the tests in CI before deploying
