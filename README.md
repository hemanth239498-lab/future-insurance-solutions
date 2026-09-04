# Future Insurance Solutions Inc.

Marketing site for **Eric Claveria**, independent life & health insurance agent, Calgary AB.

Single-file build: all HTML, CSS and JS live in `index.html`. No build step, no dependencies.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire site |
| `eric-claveria.jpg` | Portrait used in the About Me card |
| `Life insurance pic.jpg` | Permanent Insurance card |
| `Whole life insurance pic.png` | Whole Life card |
| `Term life insurance pic.png` | Term card |
| `Accident & Sickness insurance pic.png` | Accident & Sickness card |
| `Critical illness insurance pic.png` | Critical Illness card |
| `netlify.toml` | Netlify publish + cache headers |

Funeral Insurance uses inline SVG artwork, not a photo.

## Local preview

```
python -m http.server 8777
```

Then open http://127.0.0.1:8777

## Before going live

1. **Testimonial wording.** The three names (Dr. Swapna, Miguel, Hemant) were
   supplied by the client, but the quote text is still drafted copy. Confirm each
   person actually said something to that effect, or swap in their real words.
2. **The quote form has no backend.** Point `<form id="quoteForm">` at a handler
   (Formspree, Netlify Forms, or your own endpoint) so submissions are delivered.
   For Netlify Forms, add `netlify` and `name="quote"` to the `<form>` tag.

## Going live on www.futureinsurancesolutions.com

The site is deliberately invisible to search until the real domain serves it.
Publishing the GitHub Pages hostname first would get the wrong URL indexed.

**Launch checklist — all four, in one commit:**

1. `index.html` — delete the `<meta name="robots" content="noindex, nofollow">`
   tag and the PREVIEW BUILD comment above it.
2. `index.html` — in the SHARING + SEARCH block, change `og:url`, `og:image`
   and `twitter:image` from the GitHub Pages host to
   `https://www.futureinsurancesolutions.com`, and add:
   `<link rel="canonical" href="https://www.futureinsurancesolutions.com/">`
3. `robots.txt` — replace the preview block with the Allow + Sitemap lines
   already written in its comment.
4. Submit `https://www.futureinsurancesolutions.com/sitemap.xml` in Google
   Search Console.

`share-card.jpg` (1200x630) is the WhatsApp / Facebook / LinkedIn preview image.
Regenerate it if the headline or contact details change.

## Languages

The site ships in English, French and Tagalog. Translations live in the `DICT`
object inside the "TRILINGUAL RUNTIME" `<script>` block in `index.html`, keyed by
the page's own English source text — so adding or editing copy means adding the
matching key to `DICT`, not adding markup attributes.

The switcher is the EN / FR / TL control in the header. A visitor's choice is
remembered in `localStorage`; first-time visitors get French or Tagalog
automatically if that's their browser language.

**Any new English copy that isn't added to `DICT` will stay in English** when the
page is switched. To audit, diff the page's visible strings against `DICT` keys.

## Contact details in the site

- Phone / WhatsApp: +1 403 689 7740
- Email: Eric.claveria@mygreatway.ca
- Office: 1223 31 Ave NE, Calgary, AB T2E 7W1
