# Kevin Park — personal portfolio

A data-driven Jekyll site designed for GitHub Pages. The homepage mixes a
minimal editorial layout with dedicated project and research pages.

## Content map

- `_data/profile.yml` — name, headline, introduction, and external links
- `_data/projects.yml` — the single source for homepage and project cards
- `_data/research.yml` — research interests and publication entries
- `index.html` — homepage composition
- `projects.html`, `research.html`, `about.html` — main pages
- `assets/css/main.css` — design system and responsive layout
- `assets/js/main.js` — mobile navigation and subtle reveal behavior
- `assets/images/og.png` — social preview image for shared links

## Updating a project

Edit `_data/projects.yml`. A project accepts these fields:

```yaml
- slug: short-url-safe-name
  title: Project title
  kicker: Project 04 · Category
  summary: A two-sentence description focused on your role and the result.
  tags: [Topic, Tool, Method]
  featured: true
  tone: cobalt # cobalt, tangerine, or violet
  link: https://example.com
  year: 2026
```

Set `featured: true` to include it on the homepage. Every entry appears on the
Projects page.

## Adding a publication

Add an entry under `publications` in `_data/research.yml`:

```yaml
publications:
  - title: Paper title
    authors: Kevin Park, Collaborator Name
    venue: Conference or Journal
    year: 2026
    paper: https://example.com/paper
    code: https://github.com/example/repository
    project: https://example.com/project
```

Unused links can be left blank or removed.

## Publishing

GitHub Pages can publish this repository directly. In the repository settings,
set Pages to deploy from the `main` branch and the repository root. A push to
`main` will then rebuild the site automatically.
