# Repository Guidelines

## Project Structure & Module Organization

This repository contains a Hebrew Jekyll site published by GitHub Pages. Put top-level pages in the repository root, such as `index.md` and `about.md`. Put lesson content under `lessons/`, with `lessons/index.md` acting as the parent navigation page. Keep small local presentation changes in `_sass/custom/custom.scss`.

Do not copy the Just the Docs theme source, layouts, or assets into this repository unless a small local override is explicitly needed. The site uses the pinned remote theme in `_config.yml`.

## Page Front Matter

Every page must start with Jekyll front matter. Use this pattern for lessons:

```md
---
layout: default
title: שם השיעור
parent: שיעורים
nav_order: 3
permalink: /lessons/example/
---
```

Use `nav_order` to control menu order and `permalink` to keep stable links.

## Hebrew, RTL, and Technical Text

The site is primarily Hebrew and right-to-left. Keep prose readable in Hebrew, and verify that tables, callouts, and navigation work well on mobile. Code blocks, terminal commands, file names, configuration keys, and inline code such as `nav_order` must remain left-to-right.

## Build, Deployment, and Workflow

Local WSL, Bundler, Ruby, and Jekyll serving are not part of this workshop repository's required workflow. Do not run or require `wsl`, `bundle`, `jekyll`, `ruby`, `gem`, or `bundle exec jekyll serve` for normal work.

Every meaningful change must leave the GitHub Pages build passing. Deployment is handled by `.github/workflows/pages.yml` after pushes to `main`.

## Security & Privacy

Never commit secrets, access tokens, private student data, parent information, school records, or identifying classroom data. Use examples that are fictional and safe for a public repository.

## Agent-Specific Instructions

After this initial setup, future agents may read and edit the repository as requested, but must not commit, pull, or push unless the user explicitly asks for Git operations.
