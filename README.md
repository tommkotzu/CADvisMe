# Thomas Mayer — Portfolio

**Live site: https://tommkotzu.github.io/CADvisMe/**

One-page portfolio for job applications in 3D and CAD visualisation, adapted from the CAD-Vis business site.

Static HTML/CSS/JS, with no build step and no external dependencies. The Inter font is self-hosted in `fonts/`, so nothing loads from Google.

```
index.html        page markup
impressum.html    Impressum (§ 5 DDG)
datenschutz.html  Datenschutzerklärung (DSGVO)
styles.css        design tokens and all styles
main.js           nav hide/show on scroll, sticky CTA, video autoplay, contact form, scroll reveal
img/              case-study images, hero video and its poster frame
cases/            raw source material (git-ignored, not published)
```

## Run locally

```sh
python3 -m http.server 8000   # then open http://localhost:8000
```

## Publish on GitHub Pages

1. Create an empty repository on github.com (e.g. `portfolio-3d`).
2. Push this folder: `git remote add origin https://github.com/tommkotzu/<repo>.git && git push -u origin main`
3. On GitHub: Settings → Pages → Source "Deploy from a branch" → Branch `main`, folder `/ (root)` → Save.
4. After a minute the site is live at `https://tommkotzu.github.io/<repo>/`.

All paths are relative, so the site works under the `/<repo>/` sub-path without changes. `.nojekyll` tells Pages to serve the files as-is.

## Before going live

- **Image and video rights:** the case-study images and `hero.mp4` come from third-party portfolio work. Replace them or get permission before publishing.
- **Contact form:** there is no backend yet. Submitting opens a prefilled e-mail to `CAD-vis.design@pm.me`. To use a form service such as Formspree, add `action` and `method="post"` to `#contact-form`; the JS then steps aside.
- **Impressum / Datenschutz:** fill in every `[placeholder]` in `impressum.html` and `datenschutz.html`: currently phone and image credits.
