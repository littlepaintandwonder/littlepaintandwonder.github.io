# Little Paint & Wonder — Development README

A gentle, colourful web home for **Little Paint & Wonder** — a creative-kit studio for small hands and huge imaginations. The content and safety guidance are based on the supplied flyer.

## What’s included

- A responsive landing page with one complete Safety & Care area for paints, plaster sculptures, first-aid and safety guidance.
- Brand artwork and Instagram QR code supplied for the package flyer, plus Instagram links, Australian-made messaging and an online-ordering-soon notice.
- A light/dark theme toggle that remembers the visitor’s choice.
- Accessible mobile navigation and footer/floating back-to-top controls.
- A hand-crafted visual system using warm paper, coral, sage, lavender and sky blue; no stock visual dependency.
- GitHub Pages deployment workflow.
- Technical SEO support including canonical metadata, structured data, sitemap and robots controls.

## Tech stack

- [ClojureScript](https://clojurescript.org/)
- [Reagent](https://reagent-project.github.io/)
- [shadow-cljs](https://github.com/thheller/shadow-cljs)
- Plain, custom CSS

The application has no backend. The contact form opens the visitor’s email client with a pre-filled enquiry.

## Run locally

Prerequisites: Node.js 22+ and a Java runtime for shadow-cljs.

```bash
npm install
npm run dev
```

Open [http://localhost:8080](http://localhost:8080).

For a production build:

```bash
npm run build
```

Build output is written to `docs/`, which is the GitHub Pages publish directory.

## Publish

The repository is deployed automatically with GitHub Actions after pushes to `main`.

The live website is:

**https://littlepaintandwonder.github.io/**

In GitHub, Pages should use **GitHub Actions** as its deployment source.

## Project structure

```text
src/little_paint_and_wonder/core.cljs  Reagent UI and interactions
src/README.md                          Development notes

docs/index.html                        Static app shell
docs/404.html                          Custom 404 page
docs/css/                              Site styling
docs/assets/                           Images and brand assets
docs/robots.txt                        Crawler directives
docs/sitemap.xml                       Search-engine sitemap
docs/site.webmanifest                  Web app metadata

.github/workflows/deploy.yml           GitHub Pages deployment
shadow-cljs.edn                        ClojureScript build config
package.json                           npm scripts and dependencies
```
