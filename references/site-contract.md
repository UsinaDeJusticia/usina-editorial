# Current site and WordPress contract

Use this reference to avoid making the editorial skill do work already handled by the website while preserving the user's preferred one-copy handoff.

## Publishing boundary

The user publishes posts manually through the organization's existing WordPress administration interface.

The skill's job ends with publication-ready editorial content. Do not generate deployment instructions, commits, branches, merges, JSON-LD, sitemap changes, canonical tags, Open Graph markup, or frontend code unless the user separately asks for technical work.

## What the site already does

The current frontend reads published WordPress posts and handles the technical page layer, including:

- page-level article rendering;
- the visible article H1 from the WordPress title field;
- author, publication date, and reading time outside the WordPress body;
- `NewsArticle` structured data;
- canonical and social metadata;
- sitemap inclusion;
- content sanitization;
- article image handling;
- alternate Markdown delivery for compatible agents.

## Important distinction: handoff block vs published body

The website ultimately renders the title from the WordPress title field, so the final published body must not contain a duplicate H1.

However, the user's preferred editorial handoff deliberately places the **final optimized title as the first Markdown H1 inside the single copyable block** so the user can copy the entire result in one action. The user then moves/sets that first-line title in the WordPress title field while arranging the post in the CMS.

Therefore:

- **do include** exactly one optimized H1 title as the first line of the skill's primary Markdown handoff;
- treat that H1 as part of the handoff workflow, not as an instruction to publish a duplicate H1 inside the final WordPress body;
- do not create a second title outside the primary block;
- do not prepend the publication date to the article text;
- do not output technical metadata code;
- make the opening paragraph concise and self-sufficient so it works well as the basis for summaries/descriptions;
- only provide a separate manual excerpt when the user explicitly asks for it or confirms that field must be completed manually.

This distinction must remain consistent with `SKILL.md` and `output-contract.md`.

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

When two categories appear plausible, choose based on the article's primary editorial object, not every topic mentioned in it.

**Category is taxonomy, not tone.** Choose editorial mode, voice, structure, depth, and research needs from the event, evidence, purpose, audience, and sensitivity first. Assign the CMS category separately afterward. Never make `Incidencia`, `Prensa`, `Historias`, or any other category impose a writing style.

The category is a CMS selection, not article-body content. Keep it outside the primary Markdown block if it must be shown to the user.

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