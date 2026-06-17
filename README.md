# Lullabel 🌙

**A gentle baby-name generator that suggests real names, with meanings, origins, faith traditions, and zodiac signs. It also lets you shape full first–middle–last combinations to save.**

---

## What it is

Lullabel helps expecting parents discover a name to grow into. You tell it the qualities you're after — who the name is for, the feeling, a faith tradition, a starting letter, even the baby's birth or due date — and it pulls a real name with its pronunciation, meaning, and origin. Add a middle name and a family name, and it shows how the whole thing sounds together. Heart the ones you love and they collect in a shortlist.

The interface re-themes itself by gender (soft rose, blue, or sage), drifts a calm pastel background, and respects reduced-motion preferences.

## Features

- **Real names with substance** — ~88 curated names, each with pronunciation, meaning, and origin.
- **Filter by who it's for** — *For her*, *For him*, or *Either*; the whole page recolors to match.
- **Filter by feeling** — Timeless, Nature, Celestial, Old soul, Fresh, Mythical, Strong, Gentle, Regal, Joyful, Literary.
- **Filter by faith** — Christian, Jewish, Muslim, Hindu, Sikh, Buddhist, with authentic names per tradition.
- **Starting letter** — optional, or leave it open for a surprise.
- **Full name builder** — optional middle name (auto-matched to gender + faith) and a family-name field, composed into one display name.
- **Born under the stars** — enter a birthday or due date to reveal:
  - **Western zodiac** sign, element, and traits
  - **Chinese zodiac** animal (with precise lunar New Year boundaries, 1990–2044)
  - **Birth season** (with a Northern / Southern hemisphere toggle)
  - **Birthstone** and **birth flower**
  - **Life-path number** (numerology from the date)
- **Name numerology** — a "name number" derived from the chosen first + middle + last.
- **Smart bias** — when a birth date is set, suggestions lean toward names whose qualities match the zodiac and season.
- **Shortlist** — save favorites (with their full names) and remove them anytime.

## Usage

No build, no install, no server.

1. Download `baby-name-generator.html`.
2. Open it in any modern browser (double-click, or drag it into a tab).

To publish it, drop the file into any static host — GitHub Pages, Netlify, or similar — and point at the HTML file.

## How it works

Everything runs in the browser with plain HTML, CSS, and vanilla JavaScript — no frameworks, no network calls, no backend, no tracking. State lives in memory for the session.

Names are stored as a tag-indexed dataset. Each entry looks like this:

```js
{
  n: "Aria",                         // name
  g: "girl",                         // gender: "girl" | "boy" | "either"
  p: "AH-ree-ah",                    // pronunciation
  o: "Italian",                      // origin
  m: "air, or a beautiful melody",   // meaning
  v: ["modern", "classic", "joyful"],// feelings (one or more)
  r: ["christian"]                   // faith traditions (optional)
}
```

Filtering intersects the chosen gender, feeling, faith, and starting letter. Birth-date inputs derive zodiac/season/numerology data and *bias* selection toward matching feeling tags rather than hard-filtering, so results keep flowing.

### Add your own names

Append objects to the `NAMES` array in the `<script>` block.

- `v` accepts any of: `classic, nature, celestial, vintage, modern, mythical, strong, gentle, royal, joyful, literary`
- `r` is optional and accepts: `christian, jewish, muslim, hindu, sikh, buddhist`

New starting letters appear in the dropdown automatically.

**Got a name to add? Open a pull request — see [Contributing](#contributing) below.**

## Accuracy & honest notes

- **Numerology** (name number and life path) is a cultural/spiritual tradition included for delight — not science.
- **Chinese zodiac** uses real lunar New Year dates from **1990–2044**; dates outside that range fall back to a Jan-1 boundary.
- **Seasons** are month-based and default to the Northern Hemisphere — use the toggle for Southern.
- **Birthstones / birth flowers** use the common Western (US) lists; these vary by country.
- Names and meanings vary by region and source — treat them as a warm starting point, not the final word.

## Tech

`HTML` · `CSS` · `vanilla JavaScript` — one file, zero dependencies, fully offline-capable.

## Credits

Built by [@wuisabel-gif](https://github.com/wuisabel-gif).

## Contributing

**The name database grows through pull requests — contributions are welcome!** 🍼

If there's a name you'd love to see (especially names from traditions, languages, or regions not yet well represented), please add it:

1. **Fork** this repository.
2. Open `baby-name-generator.html` and find the `NAMES` array in the `<script>` block.
3. **Add your name** as a new object, following the existing format:
   ```js
   { n:"Amara", g:"girl", p:"ah-MAH-rah", o:"Igbo", m:"grace; everlasting", v:["gentle","modern"] }
   ```
   - `n` name · `g` gender (`girl` / `boy` / `either`) · `p` pronunciation · `o` origin · `m` meaning
   - `v` one or more feelings: `classic, nature, celestial, vintage, modern, mythical, strong, gentle, royal, joyful, literary`
   - `r` (optional) faith traditions: `christian, jewish, muslim, hindu, sikh, buddhist`
4. **Open a pull request** with a short note on the name and where the meaning/origin comes from.

A few friendly guidelines:
- Keep meanings accurate and respectful, and cite a source in the PR when you can.
- One name per object; feel free to add several objects in a single PR.
- Names that broaden the cultural range of the database are especially appreciated.

Found a wrong meaning or pronunciation? Open an issue or a PR to fix it, corrections are just as valuable as additions.

## License

MIT — free to use, modify, and share.
