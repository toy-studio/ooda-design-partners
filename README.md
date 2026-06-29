# ooda — Design partners

A tiny, single-page pre-launch landing site for recruiting design partners,
**hosted on ooda itself**. Built with [Astro](https://astro.build).

## Develop

```bash
npm install        # first time only
npm run dev        # dev server with live reload → http://localhost:4321
```

## Edit the blurb

Open `src/pages/index.astro` and edit the block marked `EDIT ME` (inside
`.blurb`). It's plain HTML — keep the `<p>` paragraphs and use `<strong>` for
emphasis. The CTA button points at `mailto:hello@ooda.run`; change it if you
want a different contact.

## Publish to ooda

`astro build` outputs the static site to `dist/`, which is what `ooda publish`
uploads.

```bash
npm run build      # builds the site → dist/
ooda publish       # publishes dist/ → https://design-partners.ooda.run
```

The slug comes from `ooda.json` (`design-partners`), so re-publishing always
lands on the same URL. The dashboard title shows as **Design Partners** (the
prettified slug); pass `--title "…"` on publish to override.

## Project structure

- `src/pages/index.astro` — the page (edit here)
- `public/logo.svg`, `public/favicon.svg` — ooda brand assets (served from `/`)
- `astro.config.mjs` — Astro config
- `ooda.json` — publish metadata (slug, description, tags)
- `package.json` — `dev` / `build` / `preview` scripts
- `dist/` — build output uploaded by `ooda publish` (git-ignored)
