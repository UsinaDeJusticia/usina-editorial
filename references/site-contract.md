# Current site and WordPress contract

Use this reference to avoid making the editorial skill do work already handled by the website.

## Publishing boundary

The user publishes posts manually through the organization's existing WordPress administration interface.

The skill's job ends with publication-ready editorial content. Do not generate deployment instructions, commits, branches, merges, JSON-LD, sitemap changes, canonical tags, Open Graph markup, or frontend code unless the user separately asks for technical work.

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
- make the opening paragraph concise and self-sufficient so it also works well as the basis for summaries/descriptions;
- only provide a separate manual excerpt when the user explicitly asks for it or confirms that field must be completed manually.

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

The category is a CMS selection, not article-body content. Keep it outside the primary Markdown block if it is shown to the user.

## Tags

The frontend can read and display WordPress tags when historical posts already contain them, but tags are **not part of the user's current manual publishing workflow**.

Therefore:

- do not suggest tags by default;
- do not include a tags field in the standard output;
- only discuss tags if the user explicitly asks for them or the publishing workflow changes in the future.

## Featured image and alt text

A featured image is useful on the site, but the editorial skill must not invent an image task that the user did not request.

Therefore:

- if the user supplied one or more images, identify the strongest usable image outside the primary article block;
- put alt text for an actual selected image in its own separate copyable block;
- if no image was supplied, omit image and alt fields entirely;
- only propose an unsupplied image when the user explicitly asks for help finding, choosing, generating, or briefing an image;
- never imply that a hypothetical image is part of the material received.

## Attachments and links

Supporting PDFs or original documents may remain attached or linked after the article body. The body must still explain the substantive information readers need; do not make the attachment the only place where the story exists.

Do not output a routine `DOCUMENTOS PARA ADJUNTAR` section. The user already knows what material was supplied.

Mention attachment handling separately only when there is a concrete operational reason, such as a privacy issue, an inconsistency in a source document, or a specific reader-facing link that must be inserted.

If a document or source link is meant to be visible to readers as part of the publication, it may be included naturally in the article body itself.