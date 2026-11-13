# Project portfolio (Jekyll + Minima, UChicago styling)

A single page: an introduction at the top, followed by every project.

## Edit
- `_config.yml`: site title, description, url, and baseurl.
- `index.md`: the introduction text at the top of the page.
- `_projects/`: one Markdown file per project. The text below the second `---`
  is the project description.

## Project fields
    title: Project name
    order: 1               # position on the page (1 = first)
    year: 2026             # optional
    status: In progress    # optional
    team: Names            # optional
    images:                # optional; add as many as you like
      - src: /assets/images/photo.jpg
        alt: What the picture shows
        caption: Optional caption
    links:                 # optional
      - label: View the report
        url: https://example.com

One picture displays full width; two or more display side by side.

## Pictures
Upload them to `assets/images/` (Add file → Upload files) and reference them as
`/assets/images/filename.jpg`. Keep filenames lowercase with no spaces.
Delete the example-*.jpg files once you've added your own.
