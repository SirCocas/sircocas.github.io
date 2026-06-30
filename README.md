# sircocas.github.io

Curriculum Vitae built with Jekyll for GitHub Pages.

## Quick Start

1. Clone or edit directly on GitHub
2. Add entries in markdown to `_section/` folders
3. Push to `main` branch - GitHub Pages builds automatically

## Sections

- `_experience/` - Work experience (frontmatter: title, organization, location, dates)
- `_education/` - Education (frontmatter: degree, institution, location, dates)
- `_publications/` - Research publications (frontmatter: title, venue, year)
- `_thesis/` - Master's thesis (frontmatter: title, institution, year)
- `_projects/` - Project contributions (frontmatter: title, role, dates)
- `_miscellaneous/` - Awards, volunteering, events, speaking (set `category` frontmatter)
- `_opinion/` - Opinion essays (frontmatter: title, date)

## Local Development

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Visit http://localhost:4000