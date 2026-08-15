# Little Paint & Wonder

A gentle, colourful web home for **Little Paint & Wonder** — a creative-kit studio for small hands and huge imaginations. The content and safety guidance are based on the supplied flyer.

## What’s included

- A responsive landing page with one complete Safety & Care area for paints, plaster sculptures, first-aid and safety guidance.
- Brand artwork and Instagram QR code supplied for the package flyer, plus Instagram links, Australian-made messaging and an online-ordering-soon notice.
- A light/dark theme toggle that remembers the visitor’s choice.
- Email updates UI, accessible mobile navigation, and both footer and floating back-to-top controls.
- A hand-crafted visual system: warm paper, coral, sage, lavender and sky blue; illustrative CSS palette and brush artwork; no stock visual dependency.
- GitHub Pages deployment workflow.

## Tech stack

- [ClojureScript](https://clojurescript.org/) `1.12.145` (provided by the current build tooling)
- [Reagent](https://clojars.org/reagent) `2.0.1`
- [shadow-cljs](https://clojars.org/thheller/shadow-cljs) `3.4.11`
- Plain, custom CSS (no component-library dependency)

The application has no backend. The updates form provides friendly client-side confirmation; connect it to a newsletter service when an email provider is selected.

## Run locally

Prerequisites: Node.js 22+ and a Java runtime (needed by shadow-cljs).

```bash
npm install
npm run dev
```

Open [http://localhost:8080](http://localhost:8080). For the production build:

```bash
npm run build
```

Build output is written to `docs/`, deliberately chosen as the publishable GitHub Pages directory.

## Publish to GitHub Pages

1. Create a GitHub repository named `littlepaintandwonder` under the `littlepaintandwonder` account and push this project’s `main` branch.
2. In repository **Settings → Pages**, set **Source** to **GitHub Actions**.
3. The included workflow builds and deploys the app after every push to `main`.

If the desired final address is the account root, `https://littlepaintandwonder.github.io/`, name the repository exactly `littlepaintandwonder.github.io` instead. The app uses root-relative asset paths so it is ready for this user-site setup.

## Project structure

```text
src/little_paint_and_wonder/core.cljs  Reagent UI and interactions
docs/index.html                        Static app shell
docs/css/site.css                      Theme, layout and responsive styling
.github/workflows/deploy.yml           GitHub Pages deployment
shadow-cljs.edn                        ClojureScript build config
```
# littlepaintandwonder
