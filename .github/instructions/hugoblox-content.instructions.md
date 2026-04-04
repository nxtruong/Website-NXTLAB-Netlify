---
description: "Use when creating or editing Hugo/HugoBlox content in this repository, including news posts, publications, and landing pages. Enforces exact repo schemas, file paths, and naming conventions."
applyTo: "content/**/*.md"
---
# HugoBlox Content Rules For This Repository

## Scope
- Apply these rules only to this repository.
- Do not infer fields or structures from external Hugo/HugoBlox docs.

## Repository Structure (Exact Paths)
- News posts (actual items): `content/post/<slug>/index.md`
- News landing page (year-based collections): `content/news/index.md`
- Publications listing page: `content/publication/_index.md`
- Publication items: `content/publication/<paper short name and year>/index.md`
- Research page used as project-style page: `content/research/index.md`
- Misc landing pages: `content/misc/_index.md`, `content/misc/<subpage short name>/_index.md`
- People landing page: `content/people/index.md`
- People info pages: `content/authors/<username>/_index.md`

## Front Matter Schemas (Use Existing Fields Only)

### 1) News Post Schema (`content/post/<slug>/index.md`)
Use these fields:
- `title`
- `subtitle`
- `summary`
- `authors`
- `tags`
- `categories`
- `date`
- `lastmod`
- `featured`
- `draft`
- `image` with nested keys: `caption`, `focal_point`, `preview_only`
- `projects`

Do not add extra front matter keys.

### 2) Publication Schema (`content/publication/*/index.md`)
Observed fields across publication files:
- `title`
- `authors`
- `author_notes`
- `date`
- `doi`
- `publishDate`
- `publication_types`
- `publication`
- `publication_short`
- `abstract`
- `summary`
- `tags`
- `featured`
- `links` (optional list with `name`, `url`)
- URL fields: `url_pdf`, `url_code`, `url_dataset`, `url_poster`, `url_project`, `url_slides`, `url_source`, `url_video`
- `image` with nested keys: `caption`, `focal_point`, `preview_only`
- `projects`
- `slides`

Only use fields already present in the target publication file type.

### 3) Landing/Section Page Schema (`type: landing` pages)
Observed top-level fields:
- `title`
- `date` (present in some pages, e.g. people)
- `type: landing`
- `sections` (list of blocks)

Observed section block patterns:
- `block: collection` with nested `content` and `design`
- `block: markdown` with nested `content.title`, `content.subtitle`, `content.text`
- `block: people` with nested `content.user_groups`, `content.sort_by`, `content.sort_ascending`, and `design` flags

For list index pages (non-landing), schema in repo includes:
- `title`
- `view`
- `banner` with `caption`, `image`

## File Naming Conventions
- News item directories are date-prefixed and kebab-case, then `index.md`:
  - Pattern: `YYYY-MM-<slug>`
  - Examples: `2026-01-papers-accepted`, `2018-04-BPACS-paper`
- Publication items are directories under `content/publication/` and use `index.md`.
- Landing pages are either `index.md` (section root) or `_index.md` for list sections.

## Content Patterns

### News Posts
- Structure:
  - Full front matter block.
  - Short body, usually one concise paragraph or one short intro plus bullet list.
- Tone:
  - Factual, academic/lab update style.
  - Mentions paper title, venue, collaborators, and congratulations.
- Formatting:
  - Plain markdown paragraphs.
  - Bullets used for multiple announcements.

### Publication Pages
- Structure:
  - Metadata-heavy front matter.
  - Body usually short and may contain HugoBlox callouts.
- Tone:
  - Formal/academic metadata language.
- Formatting:
  - Keep URL fields and optional associations (`projects`, `slides`) in front matter.

### Landing/Other Pages
- Structure:
  - `type: landing` and `sections` blocks.
  - `markdown` blocks often use multi-line `text: |`.
  - Some pages include markdown tables or numbered lists.
- Tone:
  - Informational and direct.

## Style Rules (Inferred)
- Prefer concise, information-dense writing.
- Keep announcements concrete (what happened, where, who).
- Preserve existing markdown conventions already used on the page (tables, ordered lists, bullets).
- Keep capitalization and punctuation consistent with nearby content.

## Minimal Real-Pattern Examples

### News Post Example (minimal complete file)
```md
---
title: "Papers accepted at ACC 2026 and ICCPS 2026"
subtitle: ""
summary: "Two papers were accepted, one at ACC 2026 and the other at ICCPS 2026."
authors: [lab]
tags: [paper,2026]
categories: [news]
date: 2026-01-29
lastmod: 2026-01-29
featured: false
draft: false
image:
  caption: ""
  focal_point: ""
  preview_only: false
projects: []
---
Our lab had two papers accepted at two different conferences.
- The paper titled "Full paper title" was accepted to conference name or published in journal name. A one-sentence introduction of the paper extracted from the abstract. Authors include <list of authors if there are 4 or fewer, otherwise list the first author>.
```

### Publication Example (minimal complete file)
```md
---
title: "An example conference paper"
authors:
  - admin
  - Robert Ford
author_notes:
  - "Equal contribution"
  - "Equal contribution"
date: "2013-07-01T00:00:00Z"
doi: ""
publishDate: "2017-01-01T00:00:00Z"
publication_types: ["paper-conference"]
publication: "In *Wowchemy Conference*"
publication_short: "In *ICW*"
abstract: "Lorem ipsum..."
summary: "Lorem ipsum..."
tags: []
featured: true
url_pdf: ""
url_code: "https://github.com/HugoBlox/hugo-blox-builder"
url_dataset: "https://github.com/HugoBlox/hugo-blox-builder"
url_poster: ""
url_project: ""
url_slides: ""
url_source: "https://github.com/HugoBlox/hugo-blox-builder"
url_video: "https://youtube.com"
image:
  caption: "Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)"
  focal_point: ""
  preview_only: false
projects:
  - example
slides: example
---
Add the publication's full text or supplementary notes here.
```

### Landing Page Example (minimal complete file)
```md
---
title: Upcoming Events
type: landing
sections:
  - block: markdown
    content:
      title: Upcoming Conferences 2026
      text: |
        | Control | Robotics |
        |---------|----------|
        | ACC: May 26-29 | ICRA: June 1-5 |
---
```

## Output Requirements For AI Assistants
- Always generate complete files (front matter + body), not partial snippets, unless explicitly asked for a snippet.
- Match existing path, naming, and schema exactly for the target content type.
- Do not introduce new front matter fields.
- Reuse existing field order and formatting style from nearby files of the same type.
