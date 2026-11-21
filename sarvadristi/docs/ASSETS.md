# Sarvadristi: asset guide

Every file lives under `assets/`. `assets/manifest.json` lists each one with size and pixel dimensions. Paths below are relative to `assets/`.

**Provenance.** The logo, the hero art, the two banners, the ten illustrations and the planet style sheet were supplied by the owner. The 119 icons and the planet drawings were made for this product (the icons by tracing the owner's icon sheet; the planets as code). Please confirm usage rights for the supplied artwork before commercial distribution.

---

## 1. Logo (`logo/`)

The logo is an eye with a four-point star as the pupil, framed by stepped lines, with the SARVADRISTI wordmark in letter-spaced geometric capitals. The SVGs are traced from the owner's logo file, so they scale without loss.

| File pattern | What it is | Where it is used |
|---|---|---|
| `svg/logo-mark*.svg` | The eye mark alone | Top navigation (large, with an animated glow), personal home header, splash, favicon |
| `svg/logo-wordmark*.svg` | The wordmark alone | Part of the horizontal and stacked lockups |
| `svg/logo-horizontal*.svg` | Mark and wordmark side by side (280 x 76 viewBox) | Hero on phone and desktop |
| `svg/logo-stacked*.svg` | Mark above wordmark | Splash screen, print, social |
| `svg/favicon.svg` | Mark in violet on a pale rounded tile | Browser tab icon |
| `svg/app-icon-dark.svg` | Gold mark on a deep indigo rounded tile | Home-screen or store icon |
| `png/*.png` | Transparent PNG exports of the above | Slides, documents, social posts |

**Colour variants** (suffix on each SVG and PNG): none = `currentColor` (SVG only, takes the surrounding text colour), `-brown` `#3F2311` (the original brand colour), `-cream` `#FDF6EE` (for dark backgrounds), `-violet` `#4B33B8` (the app accent), `-gold` `#F2B84B` (SVG only).

**Suggested usage**
- Keep clear space around the mark equal to about the height of the star pupil.
- Do not stretch, rotate or recolour outside the variants above.
- On photographic or busy backgrounds use the cream or brown version with enough contrast.
- Minimum sizes: mark 24px wide; horizontal lockup 120px wide.

---

## 2. Illustrations (`illustrations/`)

Ten glossy, gold-and-lavender 3D illustrations. `source/` holds the full-size transparent PNGs (1254 x 1254). `web/` holds 420px WebP files with transparency, which are what the app embeds.

| File | Subject | Used for |
|---|---|---|
| `kundali-lotus` | A lotus-framed kundalī chart with planets and a sun | Kundalī card and tile |
| `astrology-wheel` | A circular astrological wheel with a sun and planets | Vedic card (new-user home) |
| `herb-bowl-remedies` | A bowl of herbs with a drop of golden oil | Remedies card and tile |
| `diya-ritual` | A brass diya with a flame, smoke and a lotus | Rituals card and tile |
| `numerology-wheel` | A lotus mandala ringed by the numbers 1 to 9 | Numerology card and tile |
| `phone-number` | A phone with a star, surrounded by an orbit | Phone number card and tile |
| `sun-moon` | A golden sun held in a violet crescent | Sun, Moon and Rising card; Western card (new-user home) |
| `tarot-cards` | Three tarot cards over a crystal lotus | Tarot card and tile |
| `hands-orb-manifest` | Two hands holding a glowing orb above a lotus | Manifest card and tile |
| `vastu-house` | A house with a lit doorway, a compass and a 1 to 9 grid | Vāstu card and tile |

---

## 3. Hero and banners (`hero/`)

| File | What it is | Used for |
|---|---|---|
| `hero-hands-sun-original.png` | Two hands holding a glowing sun with orbiting planets, on black (1000 x 1000) | Master copy |
| `hero-hands-sun-transparent.webp` | The same art lifted off its black background so it blends into any page colour (780 x 780, with alpha) | Phone hero and desktop hero |
| `banner-constellation-hands.png` | Hands tracing a constellation | Banner at the top of the Horoscope tab |
| `banner-galaxy-threads.png` | Hands joined by threads across a galaxy | Banner at the top of the Family page |

The transparent hero was made by turning brightness into transparency and restoring colour. Very dark parts of the art become see-through by design.

---

## 4. Icons (`icons/`)

119 outline icons, traced from the owner's sheet, drawn as filled outlines on a 100 x 100 grid.

- `svg/NNN-name.svg`: one file per icon, `fill="currentColor"`, so it takes the text colour.
- `icons-sprite.svg`: all icons as `<symbol id="i-name">`. Use `<svg><use href="icons-sprite.svg#i-home"/></svg>`.
- `icons.json`: the index (number, name, file).
- `preview.html`: open in a browser to see them all.

Groups in the set: navigation and actions (home, search, bell, gear, user, share, download and so on), Vedic and astrology (om, diya, gem, tarot cards, crystal ball, compass, kundali lattice), the twelve zodiac signs, the planet glyphs (Sun to Saturn, Uranus, Neptune, Pluto, Rahu, Ketu) and status or interface symbols (check, warning, info, toggles, star, calendar).

**Not in the set.** Arrows and the caret are drawn separately in the app as 8-unit rounded strokes to match; they are not exported here. The map-pin role is filled by the "constellation" icon.

---

## 5. Planets (`planets/`)

Nine animated SVG planets drawn after the owner's reference sheet: wavy bands, gloss, craters and tilted rings (Saturn only; the Sun is a flame-ray sun). They are generated by code, so they are exact copies of what the app draws.

| File | Graha | Notes |
|---|---|---|
| `01-sun.svg` | Sun (Sūrya) | Traditional sun with flame rays that turn slowly, golden disc and glow |
| `02-moon.svg` | Moon (Chandra) | Pale lilac with craters |
| `03-mars.svg` | Mars (Maṅgala) | Red-orange with craters |
| `04-mercury.svg` | Mercury (Budha) | Green |
| `05-jupiter.svg` | Jupiter (Guru) | Orange bands and a red spot |
| `06-venus.svg` | Venus (Śukra) | Pink with craters |
| `07-saturn.svg` | Saturn (Śani) | Banded, with a cream and blue ring |
| `08-rahu.svg` | Rahu | Purple sphere with horns, no ring |
| `09-ketu.svg` | Ketu | Blue sphere with horns, no ring |

Each file carries its own animation (bands drift, rings rock) which pauses for reduced motion. `planet-palettes.json` holds each planet's three base colours, band colours, ring colours and crater positions, so they can be recreated in other tools.

---

## 6. Backgrounds (`backgrounds/`)

| File | Use |
|---|---|
| `star-field-small.svg` | Dense field of small stars, the static layer of the graha explorer |
| `star-field-twinkle.svg` | A sparser layer of larger stars that fades in and out |

---

## 7. Design tokens (`tokens/`)

- `design-tokens.json`: colours (light, dark, tradition sleeves, brand), type, radii, layout and motion.
- `tokens.css`: the same colours and fonts as CSS variables, with light, dark and automatic dark mode.

**Fonts** are not bundled. Load Newsreader, Outfit and the Noto Devanagari families from Google Fonts, or self-host them under their open licences.

---

## 8. Reference (`reference/`)

- `brand-logo-original.png`: the logo as supplied (brown on cream).
- `planet-style-reference-sheet.png`: the sheet of glossy flat-vector planets that guided the planet drawings.


## Tarot artwork

`assets/tarot/` holds the 22 major arcana used on card faces (1024 x 1536 JPEG, from the supplied zip), with `tarot-card-map.csv` listing which source image is used for each card. The app embeds 480 x 720 WebP copies. Tapping a revealed card, or a card in the library, opens it full screen. Every face-down card uses the supplied back, `assets/tarot/card-back.png` (sun and moon-phase mandala in violet and peach); the app embeds a 480 x 720 WebP copy. The zip also holds 56 minor arcana cards and alternates; they are not used yet.

`assets/tarot/hands-deck.png` is the Tarot home illustration: two hands holding the deck, on a transparent background.
