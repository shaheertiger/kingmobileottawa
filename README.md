# King Mobile Ottawa

One-page landing site for King Mobile Ottawa — mobile phone repair and accessories at 308 Rideau St a, Ottawa, ON K1N 5Y4.

- Single call-to-action: phone **(613) 206-6060** (header button, hero, mid-page, final CTA, and a sticky call bar on mobile).
- No build step. Everything lives in `index.html` (inline CSS, one Google Fonts link, one Google Maps embed).

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploying (Vercel)

The repo root is the deployable site — no framework, no build command.

1. In Vercel: **Add New… → Project** → import this repo.
2. Framework Preset: **Other**. Leave Build Command empty and Output Directory as the root.
3. Deploy.

`vercel.json` sets `cleanUrls`, security headers, and no-cache on `index.html`
so edits go live immediately on redeploy.

After attaching the real domain, update the hardcoded `https://kingmobileottawa.ca/`
URLs in `index.html` (canonical + JSON-LD), `robots.txt`, and `sitemap.xml`.

## Editing

- Phone number appears as `tel:+16132066060` links and as display text `(613) 206-6060`.
- Address and phone are also in the JSON-LD `MobilePhoneStore` block in `<head>` — update both if they change.
- Colors are CSS variables in `:root` (`--gold` is the accent).
