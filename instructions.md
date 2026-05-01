# writeups

GitHub Pages/Jekyll site for CTF writeups with a Catppuccin Mocha theme.

## Add a writeup

Create a Markdown file under `_writeups/<year>/`, for example:

```markdown
---
title: "Example CTF"
year: 2026
ctf: "Example CTF"
date: 2026-05-01
tags: [web, crypto]
---

# Challenge Name

Your solve notes go here.
```

Files under `_writeups/` use the writeup layout automatically, so you only need the metadata above. The sidebar groups writeups by the `year` field.

The sample template lives at `_writeups/2026/_template.md`. Copy it, rename it without the leading underscore, and edit the front matter for each CTF.

## GitHub Pages

This repo is configured as a project site with `baseurl: "/writeups"` in `_config.yml`. If the GitHub repository name is different, change `baseurl` to `"/repo-name"`. If this becomes a user site like `username.github.io`, set `baseurl` to `""`.

In GitHub, enable Pages from the repository settings and publish from the default branch. GitHub Pages will build the Jekyll site automatically.

## Local preview

```powershell
bundle install
bundle exec jekyll serve
```

With the current `baseurl`, the local site opens at `http://localhost:4000/writeups/`.
