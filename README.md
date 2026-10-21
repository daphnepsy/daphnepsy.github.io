# My website!

[daphnepoon.com](https://daphnepoon.com), built with Jekyll on GitHub Pages using the [Forty](https://html5up.net/forty) theme.

## Run it locally

```sh
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

The site is built and deployed by `.github/workflows/pages.yml` on every push to `master`
(GitHub's built-in Pages build can't run the garden plugin in `_plugins/`).
In the repo's Settings → Pages, "Source" must be set to **GitHub Actions**.

## Where things live

| What | Where |
| --- | --- |
| Homepage bio and fun facts | `index.md` |
| Project pages | `_projects/*.md` |
| Projects with only a card (no page) | `_data/project_cards.yml` |
| Footer social links, site title, email | `_config.yml` |
| Garden notes | `_notes/*.md` (written in Obsidian, see below) |
| Garden images | `assets/garden/` |

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

## Tending the garden

The garden lives at `/garden`. Each note is a Markdown file in `_notes/`, and
`_plugins/garden.rb` makes Obsidian's `[[links]]` work on the site.

**Setup (once):** clone this repo, then in Obsidian choose *Open folder as vault*
and pick the repo folder. The shared settings in `.obsidian/` already put new notes
in `_notes/`, pasted images in `assets/garden/`, and hide the site's code folders.
Use the *Obsidian Git* community plugin (or plain `git`) to commit and push.

**Writing a note:** create a note, then run *Templates: Insert template* →
*Garden note* to add the properties. Only notes with properties (front matter)
are published:

```yaml
---
title: Bread Baking
stage: seedling      # seedling 🌱, budding 🌿 or evergreen 🌳
planted: 2026-10-21  # when you started it
tended: 2026-10-21   # bump when you edit; the garden lists newest first
# published: false   # keep a draft off the site
---
```

Link notes the way you normally do in Obsidian: `[[Bread Baking]]`,
`[[Bread Baking|my bread notes]]`, `[[Bread Baking#Shaping]]`, and `![[loaf.png]]`
for images. A link to a note that doesn't exist yet shows up as faded text.
Each note lists the notes that link to it at the bottom.

The note's URL comes from its file name: `_notes/Bread Baking.md` → `/garden/bread-baking`.
