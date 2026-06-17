# Contributing to Lullabel 🌙

Thanks for helping Lullabel grow! The name database is community-powered, and thoughtful additions — especially names from traditions, languages, and regions not yet well represented — are genuinely welcome.

## Adding a name

1. **Fork** the repository.
2. Open `baby-name-generator.html` and find the `NAMES` array inside the `<script>` block.
3. Add your name as a new object in the existing format:
   ```js
   { n:"Amara", g:"girl", p:"ah-MAH-rah", o:"Igbo", m:"grace; everlasting", v:["gentle","modern"] }
   ```
   | Field | Meaning | Values |
   |-------|---------|--------|
   | `n` | Name | any |
   | `g` | Gender | `girl` · `boy` · `either` |
   | `p` | Pronunciation | e.g. `ah-MAH-rah` |
   | `o` | Origin / language | e.g. `Igbo`, `Hebrew`, `Sanskrit` |
   | `m` | Meaning | short phrase |
   | `v` | Feelings (1+) | `classic, nature, celestial, vintage, modern, mythical, strong, gentle, royal, joyful, literary` |
   | `r` | Faith traditions (optional) | `christian, jewish, muslim, hindu, sikh, buddhist` |
4. **Open a pull request** describing the name(s) you added and where the meaning and origin come from.

You can add several names in one PR — one object each. New starting letters appear in the dropdown automatically.

## Quality guidelines

- **Accuracy matters.** Use a real, verifiable meaning and origin, and cite a source in your PR when you can.
- **Keep pronunciations simple** and phonetic (the format above), not full IPA.
- **One name per object;** match the existing field order so the file stays readable.
- **Corrections are welcome too** — fixing a wrong meaning or pronunciation is just as valuable as adding a new name.

## Respect 💛

Lullabel is about names real people will carry for a lifetime, drawn from living cultures and faith traditions. Please contribute with that in mind.

- **Respect the cultures and traditions** a name comes from. Represent its meaning and origin honestly and without stereotype, mockery, or caricature.
- **Respect the people who'll use these names.** No slurs, no offensive, demeaning, or "joke" entries, and nothing that targets or belittles any group, religion, or nationality.
- **Respect faith traditions** when tagging names — only apply a `r` tag where the association is genuine.
- **Respect each other.** Keep pull requests, issues, and reviews kind and constructive. Assume good faith, welcome newcomers, and disagree gracefully.

Contributions or conduct that disregard the above may be closed or removed. In short: bring names you'd be proud to give, and treat contributors the way you'd want to be treated.

## Reporting a problem

Spotted an inaccurate meaning, an inappropriate entry, or a bug? Open an issue (or a PR with the fix). Thoughtful reports help keep the database trustworthy and welcoming.
