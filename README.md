# The Church of Barbelo — website

A single-page static site. No build step, no dependencies.

## Publish it on GitHub Pages

1. Create a new repository, e.g. `church-of-barbelo`.
2. Upload everything in this folder to the root of the repo (`index.html`, `news.json`, `.nojekyll`, and the `assets/` folder).
3. Go to **Settings → Pages**.
4. Under *Build and deployment*, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. Wait a minute or two. The site appears at `https://<your-username>.github.io/church-of-barbelo/`.

### Using your own domain

Add a file called `CNAME` at the root containing just your domain, e.g.:

```
churchofbarbelo.org
```

Then point a CNAME DNS record at `<your-username>.github.io`, and tick *Enforce HTTPS* in Settings → Pages.

## Posting a notice

Edit `news.json` directly on github.com (pencil icon → commit). Newest entries can go anywhere in the list — the page sorts by date itself. Each entry looks like:

```json
{
  "date": "2026-09-01",
  "tag": "Doctrine",
  "title": "Title of the notice",
  "body": "One or two sentences.",
  "link": "https://optional-link.example/"
}
```

`date` must be `YYYY-MM-DD`. `tag` and `link` can be left as empty strings.

## Things to change before you go live

- **Email addresses** — three placeholders in the Enquiries section (`enquiries@`, `office@`, `press@`).
- **The Pleroma Archive URL** — appears twice (Library section and footer), currently `https://example.github.io/pleroma-archive/`.
- **The epigraph** on the hero — placeholder wording, with a caption telling you so. Replace both the line and the `<cite>` (or delete the `<cite>` line entirely).
- **The four teaching points** — written from the Ophite/Sethian framing; check them against your own doctrine.
- **The three news entries** in `news.json` — written as examples.

## Files

```
index.html              the whole page (styles and script are inline)
news.json               the news feed — the only file you edit routinely
.nojekyll               stops GitHub trying to build the site with Jekyll
assets/ring.png         the ouroboros alone, centred for rotation
assets/mark-placed.png  the star mark, positioned to sit inside the ring
assets/mark.png         the star mark, trimmed (header and footer)
assets/lockup.png       the full logo with wordmark, transparent background
assets/seal-dark.png    the dark circular badge
assets/favicon.png      64px icon
assets/apple-touch-icon.png
assets/og-image.png     1200×630 preview card for social links
```

All the assets were cut from the two logo files you supplied — the ring and the
star were separated so the serpent can turn slowly around a fixed mark on the
hero. That animation stops automatically for anyone with reduced motion turned
on in their system settings.
