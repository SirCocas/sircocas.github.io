# sircocas.github.io

Curriculum Vitae built with Jekyll for GitHub Pages.

## Quick Start

1. Copy an example from `templates/EXAMPLE-*.md` to the appropriate `_section/` folder and rename it
2. Edit the frontmatter and content, then push to `main` branch
3. GitHub Pages builds automatically

## Sections

- `_experience/` - Work experience (frontmatter: title, organization, location, dates)
- `_education/` - Education (frontmatter: degree, institution, location, dates)
- `_publications/` - Research publications (frontmatter: title, venue, year)
- `_thesis/` - Master's thesis (frontmatter: title, institution, year)
- `_projects/` - Project contributions (frontmatter: title, role, dates)
- `_miscellaneous/` - Awards, volunteering, events, speaking (set `category` frontmatter)
- `_opinion/` - Opinion essays (frontmatter: title, date) - view at /opinion.html

## Customize Colors

Edit `assets/css/style.scss` to change:
- `--accent-color`: Link and border colors (default: #3498db)
- `--text-color`: Body text (default: #333)
- `--bg-color`: Background (default: #fafafa)
- `--heading-color`: Headings (default: #2c3e50)
- `--link-color`: Links (default: #3498db)

## Local Development

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Visit http://localhost:4000