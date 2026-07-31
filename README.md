# Our Lady Tattoo Parlor — Landing Page

A single-page, static site for **Our Lady Tattoo Parlor**, 121 W San Antonio St, San Marcos, TX 78666.

## Structure

- `index.html` — the landing page (sticky top bar, full-bleed hero, "why us" section, artist crew grid, contact section with embedded map)
- `gallery.html` — shop/crew photos + a lightbox grid of recent tattoo work, same format as the Eternal Courage Tattoo reference's gallery page
- `css/style.css` — all styling, no framework
- `js/main.js` — mobile nav toggle + gallery lightbox
- `images/artists/` — real artist headshots (Austin, Dane, Davis, Justin, Zach)
- `images/shop/` — real shop photos (storefront, stations, flash wall, the shop dog)
- `images/gallery/` — 21 real tattoo photos from the crew, shown in the gallery lightbox
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
- The 8 shop photos (`images/shop/`) and 21 tattoo photos (`images/gallery/`) are real, provided directly.

Pulled from public listings (Google/Yelp/search), not the shop's own channels — worth confirming:

- Hours (Tue–Sat, 12–8, closed Sun/Mon).

Still placeholder / sample, ready for you to swap in:

- **Artist specialty tags** (e.g. "American Traditional," "Blackwork & Custom") — reasonable samples, not confirmed bios. Edit the `<span class="artist-role">` text per artist in `index.html`.
- **Service list** in the "why us" flash strip — a standard traditional-shop service set, not a confirmed menu.

### Still needed: hero backdrop photos

The hero section is wired up to cross-fade 3 rotating background photos (originally
described as "MERCH," "MERCH 2," "MERCH 3" — lifestyle shots of someone wearing shop
merch by a car). The CSS/markup is ready but commented out in `index.html` right after
`<section class="hero" id="top">`, because those 3 photos weren't available as files in
this session (only pasted inline in chat, which doesn't transfer to disk). To finish it:

1. Save the 3 photos as `images/merch/merch-1.jpg`, `merch-2.jpg`, `merch-3.jpg`.
2. Uncomment the `<div class="hero-backdrop">...</div>` block in `index.html`.

That's it — the cross-fade animation in `css/style.css` (`.hero-bg-photo` / `@keyframes heroFade`) is already in place.

See the HTML comment near the top of `index.html` for the same notes in-line.
