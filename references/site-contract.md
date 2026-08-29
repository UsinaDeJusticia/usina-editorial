# Current site and WordPress contract

Use this reference to avoid making the editorial skill do work already handled by the website.

## Publishing boundary

The user publishes posts manually through the existing WordPress admin at `wp.usinadejusticia.org.ar/wp-admin`.

The skill's job ends with a publication-ready editorial package. Do not generate deployment instructions, commits, branches, merges, JSON-LD, sitemap changes, canonical tags, Open Graph markup, or frontend code unless the user separately asks for technical work.

## What the site already does

The current frontend reads published WordPress posts and handles the technical page layer, including:

- page-level article rendering;
- the visible article H1 from the WordPress title;
- author, publication date, and reading time outside the WordPress body;
- `NewsArticle` structured data;
- canonical and social metadata;
- sitemap inclusion;
- content sanitization;
- article image handling;
- alternate Markdown delivery for compatible agents.

Therefore:

- do **not** repeat the article title as an H1 inside the body;
- do **not** prepend the publication date to the body;
- do **not** output technical metadata code;
- do provide a strong WordPress title and excerpt because those editorial fields feed visible cards and downstream metadata.

## Valid current categories

Choose exactly the most appropriate current editorial section:

- `Historias`
- `Acompañamiento`
- `Incidencia`
- `Prensa`
- `Institucional`
- `Observatorio`

Use these short current category names, not similarly named legacy categories.

### Category intent

- **Historias** — victim/family stories where the human story is the primary editorial object.
- **Acompañamiento** — Usina's accompaniment, support, guidance, and direct work with victims or families.
- **Incidencia** — petitions, legal or policy advocacy, institutional requests, reform proposals, public-policy actions, and interventions intended to change institutional behavior.
- **Prensa** — interviews, media appearances, press coverage, and public interventions whose primary event is the media participation itself.
- **Institucional** — organizational announcements, recognitions, milestones, governance, events, partnerships, and institutional communications that do not fit another section better.
- **Observatorio** — reports, datasets, statistics, monitoring, publications, and evidence-oriented analysis.

When two categories appear plausible, choose based on the article's primary event, not every topic mentioned in it.

## Excerpt

Always prepare a useful excerpt unless the user explicitly asks not to.

Default target:

- 1-2 sentences;
- concise and self-sufficient;
- usually about 120-180 characters when possible, but clarity outranks a hard character target;
- should add information rather than merely repeat the title.

## Featured image and alt text

If the user supplied an image, identify the best candidate and write factual alt text based on visible content. Do not stuff keywords into alt text.

If no image was supplied, a brief featured-image suggestion may be useful, but do not invent that an image exists.

## Attachments and links

Supporting PDFs or original documents may remain attached or linked after the article body. The body must still explain the substantive information readers need; do not make the attachment the only place where the story exists.
