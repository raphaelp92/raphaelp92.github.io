# raphaelp92.github.io — personal site

Astro site. Dark "midnight + electric blue" theme. Single page: hero, what I do, projects, writing & talks, gaming, about, contact.

## Run locally
```bash
npm install
npm run dev      # http://localhost:4321  ← preview here
npm run build    # outputs static site to ./dist
npm run preview  # serve the built ./dist locally
```

## Add the project screenshot
Drop the Nasjonale prøver (Tromsø) screenshot here:
```
public/projects/nasjonale-prover-tromso.png
```
It appears automatically in the Projects section. If the file is missing, a placeholder shows instead.

## Edit content
- Page content: `src/pages/index.astro`
- Styling / colours: `src/styles/global.css` (palette lives in `:root`)
- Publications list: pulled from `src/data/cv.json` (the `publications` array) — edit there and it re-renders.

## Personal details already wired in
- Twitch: twitch.tv/bunnyhoppor · X: @TL_bunnyhoppor · Email: raphaelpeltzer@googlemail.com
- LinkedIn / GitHub links in the hero and footer.

## Deploy to GitHub Pages (raphaelp92.github.io)
This is a **user site**, so it serves at the domain root — no `base` path needed.

1. Put these files in the root of your `raphaelp92.github.io` repo (replacing the old site). Keep `.github/workflows/deploy.yml`.
2. In the repo on GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Push to `main`. The included workflow builds the Astro site and publishes it. Done.

Prefer not to use Actions? Run `npm run build` and push the contents of `dist/` to a `gh-pages` branch, then point Pages at that branch.

> Tip: before replacing the old site, copy your current repo to a backup branch so the old version is recoverable.
