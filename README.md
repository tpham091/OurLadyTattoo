# Our Lady Tattoo Parlor — Website

A Jekyll site for **Our Lady Tattoo Parlor**, 121 W San Antonio St, San Marcos, TX 78666. Structured the same way as the [Eternal Courage Tattoo](https://github.com/tpham091/Eternal-Courage-Tattoo) reference (`_data` / `_includes` / `_layouts`), with its own American traditional flash / hand-painted sign shop visual design.

## Running it locally

```
bundle config set path 'vendor/bundle'
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`. `bundle exec jekyll build` writes the static output to `_site/`, which is what gets deployed (see `vercel.json` for the Vercel build config, if you use Vercel).

## Structure

- `_config.yml` — site config (title, description, url, timezone)
- `_data/site.yml` — all shop info: address, phone, email, hours, map/review URLs, socials
- `_data/artists.yml` — the crew: name, Instagram, optional booking email, booking-method label, headshot path
- `_data/shop_gallery.yml` — the 11 "around the shop" photos on the gallery page
- `_data/gallery.yml` — the 21 recent-work photo filenames for the lightbox grid
- `_includes/head.html`, `header.html`, `footer.html` — shared page chrome
- `_includes/schema-business.html`, `schema-gallery.html` — JSON-LD structured data
- `_layouts/default.html` — wraps every page in head/header/footer
- `index.html` — the landing page (sticky top bar, full-bleed hero, "why us" section, artist crew grid, contact section with embedded map)
- `gallery.html` — shop/crew photos + a lightbox grid of recent tattoo work
- `css/style.css` — all styling, no framework
- `js/main.js` — mobile nav toggle + gallery lightbox
- `images/artists/` — real artist headshots (Austin, Dane, Davis, Justin, Zach)
- `images/shop/` — real shop photos (storefront, stations, flash wall, the shop dog, door/window signage)
- `images/usp/` — real hand-painted sign/storefront photos used in the homepage "Why Us" cards
- `images/gallery/` — 21 real tattoo photos from the crew
- `images/favicon.svg`, `icons/apple-touch-icon.png` — site icons
- `fonts/` — self-hosted webfonts (Rye, Oswald, Arvo, Permanent Marker — vendored from Google Fonts so the page has no external font dependency)

## Editing content

Almost everything editorial lives in `_data/*.yml`, not in the HTML:

- **Shop info, hours, socials** → `_data/site.yml`
- **Add/remove/edit an artist** → `_data/artists.yml`. Each entry needs `name`, `instagram`, `booking` (the label shown, e.g. "DM to Book" or "DM or Email to Book"), and `image`. Add an `email:` line to also show the envelope icon.
- **Gallery photos** → drop a new file in `images/gallery/`, add its filename to `_data/gallery.yml`. Same pattern for `images/shop/` + `_data/shop_gallery.yml`.

The hero copy, "why us" cards, and service list are static markup directly in `index.html` — edit freely.

## What's real vs. placeholder

Verified / provided directly by the shop:

- Address, phone number `(512) 210-8090`, and shop Instagram `@ourladytattoo`.
- Shop email: `ourladytattoo@gmail.com`.
- Each artist's real Instagram and preferred booking method (in `_data/artists.yml`):
  - **Justin** (owner) — [@doctaylortattooist](https://www.instagram.com/doctaylortattooist/) — DM or email, `doctaylortattooist@gmail.com`
  - **Dane** — [@sweetdanetattoo](https://www.instagram.com/sweetdanetattoo/) — DM
  - **Davis** — [@davis.tattooer](https://www.instagram.com/davis.tattooer/) — DM
  - **Zach** — [@zatattooer](https://www.instagram.com/zatattooer/) — DM or email, `zatattoer@gmail.com`
  - **Austin** — [@austinfromaustintattoos](https://www.instagram.com/austinfromaustintattoos/) — DM
- The five artist headshots are the real photos provided (not stock images) — one artist's cap literally reads "Our Lady Tattoo Parlor," confirming these are the shop's actual crew.
- The 11 shop photos (`images/shop/`), 3 sign/storefront photos (`images/usp/`), and 21 tattoo photos (`images/gallery/`) are real, provided directly.
- Hours (Tue–Sat, 12–8, closed Sun/Mon) in `_data/site.yml` — originally pulled from public listings, now also confirmed by the shop's own hand-painted door signage (`images/usp/door-signage.jpg`).
- The 3 hero backdrop photos (`images/merch/merch-1.jpg` through `merch-3.jpg`) — the shop merch/vintage car lifestyle shots that cross-fade behind the headline.

Worth double-checking:

- The door signage (`images/usp/door-signage.jpg`) promotes two Instagram handles: `@doctaylortattooist` (already Justin's card) and `@lurksteadytattoos`, which isn't currently attached to any artist in `_data/artists.yml`. Let us know whose handle that is and it can be wired up.

Still placeholder / sample, ready for you to edit:

- The "why us" card copy and the service list (in `index.html`) — written to fit a traditional street shop, not a confirmed menu.

See the HTML comment near the top of `index.html` for the same notes in-line.
