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

1. **Testimonials are placeholders.** Replace the three quotes in the
   `#testimonials` section with real, documented client feedback.
2. **The quote form has no backend.** Point `<form id="quoteForm">` at a handler
   (Formspree, Netlify Forms, or your own endpoint) so submissions are delivered.
   For Netlify Forms, add `netlify` and `name="quote"` to the `<form>` tag.

## Contact details in the site

- Phone / WhatsApp: +1 403 689 7740
- Email: Eric.claveria@mygreatway.ca
- Office: 1223 31 Ave NE, Calgary, AB T2E 7W1
