# ooda — Design partners

A tiny, single-page pre-launch landing site for recruiting design partners,
**hosted on ooda itself**.

## Edit the blurb

Open `index.html` and edit the block marked `EDIT ME` (inside `.blurb`). It's
plain HTML — keep the `<p>` paragraphs and use `<strong>` for emphasis. The
CTA button points at `mailto:hello@ooda.run`; change it if you want a different
contact.

## Publish to ooda

There's no framework — the "build" just copies the static files into `dist/`,
which is what `ooda publish` uploads.

```bash
npm run build      # copies index.html + assets → dist/
ooda publish       # publishes dist/ → https://design-partners.ooda.run
```

The slug comes from `ooda.json` (`design-partners`), so re-publishing always
lands on the same URL. The dashboard title shows as **Design Partners** (the
prettified slug); pass `--title "…"` on publish to override.

## Files

- `index.html` — the page (edit here)
- `logo.svg`, `favicon.svg` — ooda brand assets
- `ooda.json` — publish metadata (slug, description, tags)
- `package.json` — the `build` script (copy to `dist/`)
