# Our Lady Tattoo Parlor — Landing Page

A single-page, static site for **Our Lady Tattoo Parlor**, 121 W San Antonio St, San Marcos, TX 78666.

## Structure

- `index.html` — the page (sticky top bar, full-bleed hero, "why us" section, artist crew grid, contact section with embedded map)
- `css/style.css` — all styling, no framework
- `js/main.js` — mobile nav toggle
- `images/artists/` — real artist headshots (Austin, Dane, Davis, Justin, Zach)
- `images/favicon.svg` — site icon
- `fonts/` — self-hosted webfonts (Rye, Oswald, Arvo, Permanent Marker — vendored from Google Fonts so the page has no external font dependency)

No build step. Open `index.html` directly, or serve the folder with any static server, e.g.:

```
python3 -m http.server 8000
```

## What's real vs. placeholder

Pulled from public listings (Google/Yelp/search) and verified where possible:

- Address, phone number `(512) 210-8090`, and Instagram `@ourladytattoo` are real.
- Hours (Tue–Sat, 12–8, closed Sun/Mon) came from public directory listings, not the shop's own channels — **please confirm before relying on them.**
- The five artist headshots are the real photos provided (not stock images) — one artist's cap literally reads "Our Lady Tattoo Parlor," confirming these are the shop's actual crew.

Still placeholder / sample, ready for you to swap in:

- **Contact email** (`hello@ourladytattoo.com`) — a placeholder; no public email was confidently verified.
- **Per-artist Instagram links** — all five artist cards currently link to the shop's main Instagram (`@ourladytattoo`) because individual artist handles aren't public. Swap each `<a class="artist-card" href="...">` in `index.html` for the artist's personal handle when you have it.
- **Artist specialty tags** (e.g. "American Traditional," "Blackwork & Custom") — reasonable samples, not confirmed bios. Edit the `<span class="artist-role">` text per artist.
- **Service list** in the "why us" flash strip — a standard traditional-shop service set, not a confirmed menu.

See the HTML comment near the top of `index.html` for the same notes in-line.
