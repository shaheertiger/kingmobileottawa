# King Mobile Ottawa

One-page landing site for King Mobile Ottawa — mobile phone repair and accessories at 308 Rideau St a, Ottawa, ON K1N 5Y4.

- Single call-to-action: phone **(613) 206-6060** (header button, hero, mid-page, final CTA, and a sticky call bar on mobile).
- No build step. Everything lives in `index.html` (inline CSS, one Google Fonts link, one Google Maps embed).

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploying

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages) — publish the repo root.

## Editing

- Phone number appears as `tel:+16132066060` links and as display text `(613) 206-6060`.
- Address and phone are also in the JSON-LD `MobilePhoneStore` block in `<head>` — update both if they change.
- Colors are CSS variables in `:root` (`--gold` is the accent).
