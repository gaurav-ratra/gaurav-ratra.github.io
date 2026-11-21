# Sarvadristi (सर्वदृष्टि)

*Formerly "Nāma Kundalī Vāstu".* A private, on-device astrology, numerology, Vāstu and tarot companion. Everything runs in the browser; nothing about the user is sent anywhere.

| | |
|---|---|
| **Owner** | Gaurav Ratra |
| **Version** | v26 (November 2026) |
| **Form** | One self-contained HTML file (`app/sarvadristi.html`, about 1.3 MB with embedded images) |
| **Live build** | https://claude.ai/artifact/LebihdkEd1byMGTpeGXc3Z |
| **Languages** | English, Hindi (हिन्दी), Hinglish |
| **Platforms** | Any modern browser. Phones and narrow screens (up to 700px) get one design; desktop and tablets get another |

---

## 1. What it is

Sarvadristi takes a person's name, birth details and (optionally) phone number and turns them into a set of readings: a computed Vedic kundalī, a Western chart, daily horoscopes, name and phone-number numerology, remedies, rituals and a japa counter. Alongside that sit two tools that need no personal data at all: a Vāstu guide for the home and an interactive tarot reading.

The name means "the all-seeing view". The logo is an eye with a four-point star as its pupil, framed by stepped lines, and it is the visual idea behind the whole product.

### Who it is for
- People who follow Vedic astrology, numerology and Vāstu and want a quick, private reference in Hindi, Hinglish or English.
- Families who want to read several people's charts and see how they fit together.
- Anyone who wants a guided tarot pull without signing up.

### Principles
1. **Private by design.** No account, no server, no tracking. All data lives in the browser's local storage.
2. **Computed, not canned.** Readings come from the user's own chart and today's sky, using stated rules, not random text.
3. **Both traditions, kept distinct.** Vedic (sidereal) and Western (tropical) are separate, switchable, and never mixed in one reading.
4. **Reflective, not predictive.** The app says plainly that it is a traditional and reflective guide.
5. **Calm and tactile.** Soft gradients, glossy planets, a deep-space explorer, and small animations that stop for people who prefer reduced motion.

---

## 2. Feature inventory

### 2.1 Home
Home is different for new and returning users, and different on phone and desktop.

- **New user (phone).** A hero where the artwork of two hands holding a glowing sun floats on the page background. The horizontal logo sits where a headline would, with a one-line promise and a "Begin your reading" button. Four small numbered pointers show the setup steps (Name, Birth, Place, Number). Below are swipeable cards for Vedic, Western, Vāstu and Tarot, each opening straight into that area. Vāstu and Tarot work with no details entered.
- **Returning user (phone).** A personal dashboard:
  - Greeting and today's headline.
  - Three tiles: name score, phone score, day streak.
  - A Vedic | Western sleeve containing a "Today" card with a progress bar and an Explore row of illustrated tiles.
  - Four daily practices to tick off (they drive the streak): read today's horoscope, chant the day mantra 11 times, pull a daily tarot card, write one line of gratitude.
  - A Profiles row showing the user and up to ten relatives.
- **Desktop.** The earlier design: the horizontal logo, a button ("Begin your reading", or "Open my chart" once a profile exists), the four setup pointers, a blended hero image, and a "Two traditions, one birth chart" section. Every card in that section is fully clickable (mouse, touch or keyboard).

### 2.2 Setup wizard (four steps)
1. **Name.** Plus an optional second name to compare.
2. **Birth.** Date and time of birth, with "I do not know the exact time" (noon is used and the lagna is flagged as approximate).
3. **Place.** A city list (about 27 Indian cities) or manual latitude, longitude and UTC offset.
4. **Number.** An optional mobile number.
A review summary is shown before the reading is computed. Form values are saved on the device so the dashboard returns on the next visit.

### 2.3 Kundalī (Vedic)
- **Janma Kundalī.** A North Indian style chart. Each planet is drawn as a small glossy planet. Hover, focus or tap a planet to see its name, Sanskrit name, sign, degree, house and whether it is retrograde. Rings and surface bands are animated.
- **Graha explorer.** A deep-space panel with stars. A large planet, its sign and degree, a strength ring (1 to 5), and facts: house and its meaning, nakshatra and pada, houses ruled, weekday, bilingual mantra. Arrows and a scrolling row of planet cards move between the nine grahas.
- **Full planetary table.** Sign, degree, house, nakshatra, strength and state, with planet illustrations. Collapsed by default.
- **Chart snapshot, yogas and doshas.** Yogas checked: Gaja-Kesari, Budhāditya, Chandra-Maṅgala and the five Mahāpuruṣa yogas. Doshas checked: Maṅglik, Kāl Sarp, Sāḍe Sātī, Dhaiyā, Pitṛ, Guru-Chāṇḍāla and Grahaṇa.
- **Vimśottarī Daśā.** A timeline bar of the whole life in planet periods, a "Now" marker, the antardaśās inside the current period, and the next three periods with dates.
- **Remedies.** Chosen from the running daśā lord, the lagna lord and weak planets, shown as numbered step cards: Start here, Next, Then, Later. Each card has the planet, why it was chosen, a Chant box (Sanskrit and English, with an "Open japa counter" button), Give, Colour (with swatches) and Live by tiles, and a footer with the deity and a gemstone caution. Dosha remedies are cards with a checklist.

### 2.3.1 Daily horoscope (Vedic and Western)
Generated for the chosen tradition from today's planet positions against the user's own chart.
- **Vedic.** Moon transit from the natal Moon (Chandra gochar), Tārā bala from the birth nakshatra, and the classical good-house tables for Sun, Mars, Mercury, Jupiter, Venus and Saturn. Gives an overall rating, four category ratings (Love, Career, Health, Money), do and go-easy-on lists, lucky colour and number, the mantra of the day and an approximate Rahu Kāla.
- **Western.** The transit Moon through the user's solar houses, its aspect to the Sun sign, and Mercury retrograde. Same categories, plus an affirmation.

**Downloadable reports.** Five reports can be saved as a PDF or an HTML file: name numerology, phone number numerology, Lo Shu grid, kundalī analysis and the daily horoscope (for the tradition currently selected, with a seven-day outlook). The PDF is built on the device from page images; it needs a connection the first time to load the PDF tools.

### 2.4 Western
- Sun, Moon and Rising in the tropical zodiac with element and modality.
- **Chart wheel.** Rising sign at the left, sign glyphs, planets placed by longitude, and lines for major aspects (solid for trines and oppositions, dashed for sextiles and squares) within 6 degrees.
- Planets table and a **Balance** view: an element donut (Fire, Earth, Air, Water) and a modality bar.

### 2.5 Numerology
- **Name.** A 0 to 100 score on an animated gauge, letter-by-letter breakdown (Chaldean values, vowels shaded), compound and reduced numbers, near-miss notes, favourable numbers from the chart, and suggested respellings (bounded edits and middle-initial changes). An alternative name can be compared.
- **Phone number.** Strips +91 or a leading 0, adds the digits, reads the compound and reduced number as a planet, and scores it against the user's birth number, destiny number, name number, compound quality and digit balance (clusters of 4s and 8s, zeros, domination). Includes a digit chart, target totals and last-digit suggestions. A second number can be compared.

- **Lo Shu grid.** The classic 3 by 3 magic square (4 9 2 / 3 5 7 / 8 1 6) filled with your birth-date digits plus birth and destiny numbers. Each square shows its planet; complete rows, columns and diagonals are joined by a line. It lists the eight planes and lines (Mental, Emotional, Practical, Thought, Will, Action, Determination, Insight) as Complete, Partial or Missing; the numbers you have; missing numbers with a mantra, charity and colour for the matching planet; repeating numbers; and whether your name number fills a gap.

### 2.5.1 Vāstu (independent of the user)
Deliberately uses no name, birth date or birth day.
- **How to use.** Three plain steps: find the door direction, mark where each room is, fix the red ones first.
- **Vāstu compass.** A sixteen-zone dial (steel bezel, degree ring, deity ring, compass rose). Tap a zone, type degrees, or **aim with the phone**: the Aim button opens a full-screen live compass, you point the top of the phone at the door or room and tap anywhere to lock that heading. The result is a colour-coded verdict (a green, amber or red panel) in plain language: what the side is good for, what to do, and suitable colours, with the traditional deity, graha and element tucked under "Traditional details".
- **Room planner.** Fourteen rooms. Each room card has a small 3 by 3 compass; tap the direction the room is in, or tap the room (Main entrance, Kitchen and so on) to open the aim-and-tap compass and lock its direction by pointing. Dots show the best (green), okay (amber) and avoided (red) spots, and the card says in words whether to keep or move it. An overall fit meter summarises the plan.
- **To-do list.** Rooms to fix first, rooms that could be better, and a count of rooms already in a best spot, each with where it should go and what to do if it cannot move.
- **Dosha finder.** Fourteen yes/no switches in five groups (corners and centre, entrance, water and clutter, floors and ceilings, bedroom and mirrors) are combined with the door direction and the room placements. Each dosha found is shown as Major, Moderate or Minor with why it matters, what triggered it, the best fix and easy fixes that need no construction, and a dosha-free score on a meter. Covered: Ishanya, Nairutya, Agneya, Vayavya and the four other direction doshas, Brahmasthan, Dwar vedha, weak entrance, door direction, wrong slope, beam, mirror, water leakage, clutter, toilet facing a sacred space, sleeping direction, cooking direction and stalled energy. Answers are saved on the device.
- **Wealth and abundance.** A 3 by 3 wealth map (north at the top, with the north, north-east and south-west marked as the main money zones) and a twelve-item checklist (entrance, north and north-east, locker and cash, daily habits) with a progress bar. A note says these are traditional customs and not financial advice.
- **Quick jump.** Chips at the top of the page jump to Door, Rooms, To-do, Doshas and Wealth.
- **Direction cheat-sheet** (eight direction cards with an optional list of the eight in-between zones) and **easy fixes for any home**.

### 2.6 Tarot (works without a profile)

**Tarot home and reading.** The Tarot home shows hands holding the deck. In a reading the cards are large: one or two cards fill the width, three or more sit in a swipeable row (with position dots) so each card is about 260 px wide. Each card has its position label (Past, Present, and so on) and shows its name after it is turned. Turning a card is a short animation: the card lifts and glows, turns edge-on with rays and sparks, shows the face with a light sweep, then settles. "Reveal all" turns the cards one at a time. With reduced-motion turned on, cards simply turn over. The deck strip and the picked slots are also larger.

**Card art.** The 22 major arcana use the supplied artwork on the card faces (reversed cards are shown upside down). Tapping a revealed card or a library card opens it full screen. Face-down cards use the supplied sun and moon-phase back. Minor arcana are not part of the deck yet.
- Spreads: Daily (1 card), Yes or No (1), Past and Path (3), Chart spread (3, through the user's chart, needs a profile), Six-card snapshot.
- **Interaction.** Pick your own cards from a fanned deck of 22 major arcana. Picked cards fly into labelled slots. Tap each card to turn it over with a spark burst and vibration. Revealed cards tilt as the finger or mouse moves. After the reveal there is a "story so far", a clarifier-card draw for short spreads, and "Reveal all".
- All 22 cards have upright and reversed meanings and a card library. Readings can be saved to a journal (up to 30).

### 2.7 Rituals
- Today's sky: moon phase, tithi, nakshatra, day ruler.
- Eight ritual intentions, each with a five-step practice.
- **Japa counter with suggested mantra.** Suggestions come from the running daśā lord (the main one), today's day ruler and the lagna lord. The chosen mantra shows large in Devanagari with the English transliteration beneath, with the reason it was suggested. A 108-bead ring counts repetitions and mālās.
- Upcoming sacred dates.

### 2.8 Manifest
Intention to sankalpa builder, next favourable window, a 21 or 40 day tracker with persistence, plus affirmation, timing and placement advice.

### 2.9 Family and profiles
- Up to **10 relatives**, with relations Mother, Father, Spouse, Son, Daughter, Daughter-in-law, Son-in-law, Mother-in-law, Father-in-law, Sibling, Grandparent, Aunt or uncle, Cousin and Other (CSV also accepts plain spellings such as "son in law" and common Hindi words like bahu, saas, sasur, damad), added by form (name, relation, date, time and place of birth, phone), by CSV upload, or by the browser's contact picker where supported.
- **Compatibility** with the user: Moon-sign relation 40 points, birth numbers 25, destiny numbers 20, name vibration 15 (name-only when no birth date).
- **Switch profile.** A relative with a birth date can become the active profile; the whole app (home, charts, horoscope, numerology, tarot echoes) then reads for them. A "Viewing {name}, Back to me" bar shows on Home.

### 2.9.1 Profile and settings
Language (English, Hindi, Hinglish), appearance (light, dark), profiles list, my details, family, saved tarot readings, new reading, reopen last reading, and clear saved data (asks twice).

---

## 3. Information architecture

Bottom navigation (4 items): **Home, Kundalī, Vāstu, Profile.**

| Route (`#hash`) | Contents | Needs a profile |
|---|---|---|
| `home` | New-user hero or personal dashboard (desktop: the earlier home) | No |
| `begin` | Four-step wizard | No |
| `kundali` | Vedic and Western sleeve. Vedic: Kundalī, Remedies, Horoscope. Western: Western, Horoscope | Yes |
| `vastu` | Entrance, room planner, directions, remedies | No |
| `name` | Name, Phone and Lo Shu tabs | Yes |
| `practice` | Rituals and Manifest tabs | Yes |
| `tarot` | Tarot hub, spreads, library, journal | No (chart spread needs one) |
| `family` | Add, import, list and compare relatives | No (matches need a profile) |
| `profile` | Settings and profile switcher | No |

**Sleeves.** Vedic and Western are two obsidian cards stacked on top of each other. The selected tradition is the front card, joined to its own tab; the other one sits behind it, with its tab and a soft sliver of its edge showing underneath. Switching swaps which card is in front. Vedic joins on the left, Western on the right. Outside Kundalī the tabs are plain pills.

---

## 4. Method and content notes

These are the rules the engine follows. They are stated so a reader can check or challenge them.

- **Positions.** Low-precision analytic orbital elements for the planets and a perturbed Moon series, evaluated in the browser. The Rahu and Ketu nodes are the mean nodes. This is not a Swiss Ephemeris and was not independently validated against one in this project; treat degree values as approximate, particularly near sign and nakshatra boundaries.
- **Zodiac.** Sidereal (Lahiri ayanamsha: 23.85306° at J2000 plus 1.39697° per century) for Vedic; tropical for Western.
- **Houses.** Whole-sign houses from the lagna.
- **Daśā.** Vimśottarī from the Moon's nakshatra; antardaśās are proportional.
- **Daily Vedic horoscope.** Moon house from the natal Moon scored 1 to 5 (best in houses 10 and 11), adjusted by Tārā bala; category ratings use the classical gochar good-house lists.
- **Numerology.** Chaldean letter values for names; Mūlānk (birth number) and Bhāgyānk (destiny number) from the date of birth; planet friendships decide how well two numbers fit.
- **Vāstu.** Traditional direction, deity and room-placement tables (ideal, acceptable, avoid). The room planner scores ideal as full, acceptable as 0.6, neutral as 0.4 and avoid as 0.
- **Tarot.** 22 major arcana; reversed with 35 percent probability; the Yes or No result combines a per-card tendency with orientation.
- **Mantras.** Seventeen mantras (nine planetary beeja mantras plus eight deity mantras) stored in both Devanagari and a Roman transliteration.
- **Disclaimer text.** The app presents astrology as a traditional, reflective guide, not a prediction, and not medical, legal or financial advice. Gemstone guidance carries a "with expert advice" caution.

---

## 5. Data and privacy

No network calls are made for user data. The only external requests are Google Fonts. Stored in the browser's `localStorage`:

| Key | Holds |
|---|---|
| `nkv.form` | Wizard inputs (name, birth details, place, phone) |
| `nkv.active` | Which profile is active (`me` or a relative's id) |
| `nkv.family` | Up to 10 relatives |
| `nkv.journal` | Saved tarot readings (max 30) |
| `nkv.track` | Manifest tracker |
| `nkv.tasks`, `nkv.streak` | Today's practices and the streak |
| `nkv.vastu` | Door direction and room placements |
| `nkv.trad` | Vedic or Western |
| `nkv.lang` | `en`, `hi` or `hn` |
| `nkv.splash` (session) | Logo splash already shown this session |

"Clear saved data" removes these keys except the language. Phone numbers and family details never leave the device. Clearing browser data or switching browsers loses them; there is no sync or backup.

---

## 6. Design system

Tokens are in `assets/tokens/`.

- **Brand.** Eye-and-star logomark with a letter-spaced SARVADRISTI wordmark. Original colours are warm brown on cream; in the app the logo takes the interface ink colour so it works in light and dark.
- **Colour.** Light: lavender ground `#F4F0FA`, ink `#1D1634`, accent `#4B33B8`. Dark: deep indigo `#120E26`, ink `#F5F2FF`, accent gold `#F2B84B`. Each tradition is a flat obsidian card: Vedic a warm obsidian (`#16110D`) with a gold accent, Western a cool obsidian (`#0A111D`) with an ice-blue accent. Inside a card the palette switches to light-on-dark, so every card, tile and chart reads the same way in both light and dark themes.
- **Type.** Newsreader (serif) for headings and large numbers; Outfit (geometric sans) for everything else; Noto Serif and Sans Devanagari fill in Hindi and Sanskrit.
- **Shape.** Large rounded cards (28 to 32px), pill buttons, and squircle sleeves with concave fillets where the tab meets the body.
- **Imagery.** Hero art blended into the page (no frame). Ten illustrations for the feature areas, shown on the cards. Glossy planets drawn after the reference sheet: wavy bands, gloss, craters and tilted rings (Saturn only). The Sun is drawn as a traditional sun with flame rays that turn slowly. Rahu and Ketu are ringless spheres with horns.
- **Icons.** A 119-icon traced outline set used for navigation, actions, zodiac signs and planet glyphs. Arrow and caret icons are drawn to match.
- **Motion.** Needle sweep on meters, drifting planet bands, rocking rings, a pulsing logomark glow, twinkling stars, card flights and flips in tarot. All decorative motion is disabled under `prefers-reduced-motion`.
- **Responsive.** One breakpoint at 700px. Phone and desktop are deliberately different designs.
- **Accessibility.** Focus styles on the clickable cards and chart planets, keyboard access for both, labelled buttons, and touch targets of about 44px for the main controls. A full accessibility audit (contrast, screen-reader pass) has not been done.

---

## 7. Languages

- **English** (default), **Hindi** and **Hinglish** (Latin script with Hindi planet names: Surya, Chandra, Mangal, Budh, Guru, Shukra, Shani).
- A dictionary maps interface strings and a glossing pass translates planet, sign, nakshatra, day and city names inside longer sentences. A mutation observer translates content added later.
- **Chart labels** follow the language: English Su Mo Ma Me Ju Ve Sa Ra Ke; Hinglish Su Ch Ma Bu Gu Sk Sn Ra Ke; Hindi सू चं मं बु गु शु श रा के.
- **Mantras** are always shown in Devanagari with a transliteration.
- **Known gap.** Hindi coverage is complete for navigation, headings, labels, planets, signs, tarot and the horoscope headlines, but long remedy and Vāstu paragraphs are still partly in English.

---

## 8. Technical notes

- **Delivery.** A single HTML file with inline CSS and JavaScript, no framework, no build step at runtime. Images are embedded as WebP data URIs; icons and planets are inline SVG.
- **Structure of the script.** (1) Calculation core: dates, ephemeris, ayanamsha, houses, daśā, yogas, doshas, numerology, scoring. (2) Content tables: planet info, remedies, rituals, tarot, Vāstu, mantras, cities. (3) View builders that return HTML strings. (4) UI layer: routing by hash, wizard, tarot app, family, profile switching, language layer, tooltips. (5) Boot: restores saved data, recomputes the reading and renders.
- **Fonts.** Loaded from Google Fonts on first visit (Newsreader, Outfit, Noto Devanagari). Without a network the app falls back to Georgia and the system sans.
- **Device features.** Compass uses `DeviceOrientationEvent` (magnetic north, no declination correction). Vibration on tarot actions where supported. The contact picker appears only where the browser offers it.
- **Size.** About 1.3 MB, most of it embedded images. A future pass could lazy-load the illustrations.

---

## 9. Quality notes

- Logic paths (wizard, profile switching, family import, tradition switching, tarot, meters, language switching) were exercised in an automated browser simulation, and screens were checked in screenshots on phone and desktop in light and dark.
- It has **not** been tested on real phones or tablets, nor in Safari or Firefox specifically. Real-device checks are the most valuable next step, especially touch on the chart tooltip, the compass, the contact picker and animation smoothness.
- Astrological output follows the stated rules; it was not reviewed by a practising astrologer. A review of the Sanskrit mantra spellings, the remedy text and the Vāstu tables by a subject expert is recommended before wider release.

### Known limitations
- Ephemeris is approximate (see section 4).
- City list is short; other places need manual coordinates and UTC offset.
- Compass shows magnetic, not true, north.
- No minor arcana in tarot.
- Hindi is partial for long paragraphs.
- Data is per device and per browser.
- The illustrations and hero art were supplied by the owner; confirm licensing before commercial distribution.

### Ideas for later
Desktop dashboard with profile switching and the daily checklist; export and import of saved data; true-north compass correction; more cities with a place search; a printable kundalī; push or calendar reminders for the daily horoscope; lazy-loaded imagery.

---

## 10. Version history (summary)

| Stage | Highlights |
|---|---|
| v1 to v15 | Computation engine, name and phone numerology, Kundalī, remedies, Vāstu, Western chart, tarot, rituals, manifest, language layer (Hindi, Hinglish). |
| v16 to v18 | Profile in the bottom nav, birth date and time layout fix, the supplied icon set. |
| v19 | Vāstu made independent of personal data, family of up to 10, daily horoscope, two homes, Vedic and Western split, interactive tarot. |
| v20 | Profile switching, relatives with birth time and place, planet illustrations in the planet table, unified profile button, icon set applied. |
| v21 | New type pairing, graha explorer, daśā timeline, Western wheel and balance donut, japa counter with suggested mantra, separate desktop and mobile designs. |
| v22 | Sanskrit and English mantras, Hinglish chart labels, logo and splash, app renamed Sarvadristi. |
| v23 | Hero imagery, four-step pointers, folder-tab sleeves, glossy planets, animated chart planets with name tooltips, meter needle fix. |
| v24 to v26 | Hero blended into the page, horizontal logo, glowing logomark, deep-space explorer, whole-section sleeves, horns on Rahu and Ketu, clickable illustrated cards (ten illustrations). |

---

## 11. Files in this package

```
sarvadristi/
  PRODUCT.md          this document
  app/sarvadristi.html  the complete app
  docs/ASSETS.md      asset guide (what each file is and where it is used)
  assets/
    logo/             svg and png: mark, wordmark, horizontal, stacked, favicon, app icon
    illustrations/    source (full size png) and web (420px webp) for ten feature illustrations
    hero/             hero artwork (original and transparent), two banners
    icons/            119 individual svg files, a sprite, a json index and an html preview
    planets/          nine animated planet svgs and the palette json
    backgrounds/      star fields used by the graha explorer
    tokens/           design-tokens.json and tokens.css
    reference/        original logo and the planet style reference sheet
    manifest.json     every file with size and dimensions
```

## Responsive tarot (v37)
Phone (<=700px): readings stack vertically. Tablet (701-1099px): cards in a grid, 3 across. Desktop (>=1100px): a real desktop shell with a left side navigation, a wide workspace, two-column Kundali, a sticky compass beside rooms in Vastu, a card grid on Home and a split Tarot hub.

## v39
Relatives can be edited after adding, and any relative can be checked under another name (score preview, then "Use this name"). New Guru tab: questions are answered by Claude from the computed kundali, using the artifact `sample` capability (works only when the published page is opened in Claude). Chat history is kept per profile in localStorage key nkv.guru.

## v41 desktop dashboard
At >=1100px: framed workspace, dark icon rail, top bar (Vedic/Western toggle, Ask the Guru field), bento Home (#dash, renderDash). Tablet and phone unchanged.

## v42
Kundali Predictions card (today + next 12 months), Vedic sign names, desktop compass drag, indigo palette replacing obsidian, hero-led bento Home, profile dropdown.

## v43
Theme switch + wordmark in top bar, animated edge glow and hover info on cards, planet-image daśā timeline, tarot-for-today stack on Home, Predictions (today, daśā months, calendar year, life, dates) and calendar reminders (.ics).

## v44
Dasha timeline uses your planet images (Sun, Mercury, Venus, Mars, Jupiter, Saturn) plus Rahu and Ketu characters, on desktop dashboard and Kundali Dasha tab (tablet and phone).
