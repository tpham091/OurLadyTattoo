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

Verified / provided directly by the shop:

- Address, phone number `(512) 210-8090`, and shop Instagram `@ourladytattoo`.
- Shop email: `ourladytattoo@gmail.com`.
- Each artist's real Instagram and preferred booking method:
  - **Justin** (owner) — [@doctaylortattooist](https://www.instagram.com/doctaylortattooist/) — DM or email, `doctaylortattooist@gmail.com`
  - **Dane** — [@sweetdanetattoo](https://www.instagram.com/sweetdanetattoo/) — DM
  - **Davis** — [@davis.tattooer](https://www.instagram.com/davis.tattooer/) — DM
  - **Zach** — [@zatattooer](https://www.instagram.com/zatattooer/) — DM or email, `zatattoer@gmail.com`
  - **Austin** — [@austinfromaustintattoos](https://www.instagram.com/austinfromaustintattoos/) — DM
- The five artist headshots are the real photos provided (not stock images) — one artist's cap literally reads "Our Lady Tattoo Parlor," confirming these are the shop's actual crew.

Pulled from public listings (Google/Yelp/search), not the shop's own channels — worth confirming:

- Hours (Tue–Sat, 12–8, closed Sun/Mon).

Still placeholder / sample, ready for you to swap in:

- **Artist specialty tags** (e.g. "American Traditional," "Blackwork & Custom") — reasonable samples, not confirmed bios. Edit the `<span class="artist-role">` text per artist.
- **Service list** in the "why us" flash strip — a standard traditional-shop service set, not a confirmed menu.

See the HTML comment near the top of `index.html` for the same notes in-line.
