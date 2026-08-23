# Ai Vibecode Public Docs

Static public documentation site for Ai Vibecode apps and games.

The site is designed to scale from one product to many without changing the basic structure.

## Site structure

```text
/
├── index.html                         # Ai Vibecode landing page
├── styles.css                         # shared visual system
├── privacy-policy.html                # compatibility redirect
└── apps/
    └── visual-perception-game/
        ├── index.html                 # product documentation hub
        └── privacy-policy.html        # current privacy policy
```

Future products should follow the same pattern:

```text
apps/<product-slug>/index.html
apps/<product-slug>/<document>.html
```

Add one card to the root `index.html` for each new public product, then add document cards to that product's own `index.html`.

## GitHub Pages

Deployment is handled by `.github/workflows/pages.yml` using GitHub Pages Actions.

Expected project-site URL:

`https://andrewmuir.github.io/PublicDocs/`

The workflow attempts to enable/configure Pages automatically. If GitHub requires a one-time repository setting, open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**, then re-run the `Deploy public docs to GitHub Pages` workflow.

## Privacy policy URL

Canonical game privacy policy:

`https://andrewmuir.github.io/PublicDocs/apps/visual-perception-game/privacy-policy.html`

The old root-level `privacy-policy.html` remains as a redirect so any earlier link continues to work.

## Branding / naming

`Visual Perception Game` is a working title. The Android package `com.visualperceptiongame.app` remains the stable identifier for the privacy policy even if the public app name changes later.

The site itself is intentionally framework-free: plain HTML and CSS, no analytics, cookies, remote fonts or third-party scripts.
