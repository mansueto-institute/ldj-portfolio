# Unit project portfolio (Jekyll + Minima, UChicago styling)

## Edit
- `_config.yml`: unit name, tagline, email, address, url/baseurl.
- `index.md`: home page intro. Projects with `featured: true` appear here.
- `about.md`: mission and contact.
- `_projects/`: one Markdown file per project. Fields: title, summary, year,
  status, team, partners, featured, image, image_alt, links.
- Images go in `assets/images/`; reference as `/assets/images/name.jpg`.
- Colours and fonts: top of `assets/main.scss`.

## Using the official UChicago fonts
If your unit obtains web font files for UChicago Sans Serif / UChicago Serif,
upload them to `assets/fonts/` and add @font-face rules at the top of
`assets/main.scss` (below the two `---` lines), e.g.:

    @font-face {
      font-family: "UChicago Sans";
      src: url("fonts/UChicagoSans-Regular.woff2") format("woff2");
      font-weight: 400;
    }

The font stacks already list these names first, so nothing else changes.
