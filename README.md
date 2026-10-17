# My website!

[daphnepoon.com](https://daphnepoon.com), built with Jekyll on GitHub Pages using the [Forty](https://html5up.net/forty) theme.

## Run it locally

```sh
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Where things live

| What | Where |
| --- | --- |
| Homepage bio and fun facts | `index.md` |
| Project pages | `_projects/*.md` |
| Projects with only a card (no page) | `_data/project_cards.yml` |
| Footer social links, site title, email | `_config.yml` |
| Resume | `assets/files/resume.pdf` |

## Adding a project

Create `_projects/<slug>.md`. It's served at `/projects/<slug>` and gets a card on the projects page automatically:

```yaml
---
title: My Project
period: Fall 2026            # shown before the title on the card
order: 0                     # cards are sorted by this, lowest first
image: assets/images/my-project.png
summary: One or two sentences for the card.
# image_position: 25% 25%    # optional, crop focus for the card image
---
Write about the project here (Markdown).

{% include pdf.html file="assets/files/report.pdf" width="600" height="600" %}
```
