# Default output contract

The goal is not to present a descriptive package. The goal is to make each WordPress field immediately usable without deleting labels or unrelated material after copying.

## Field-separation rule

Never place the complete deliverable inside one monolithic writing block, editable artifact, Markdown block, or copyable container.

When the harness supports independent writing/editable blocks, use **one separate copyable block per field that the user must paste**. Put the field label outside the block. The block itself must contain only the value to paste.

For a complete article, use this order:

### TÍTULO

Place the label outside the copyable block. The block contains only the final title.

- No `TÍTULO` text inside the block.
- No `LISTO PARA WORDPRESS` heading.
- No `#`, `<h1>`, publication date, commentary, or alternatives unless the user asked for options.

### EXTRACTO

Place the label outside the copyable block. The block contains only the final excerpt.

- 1-2 self-sufficient sentences.
- Complement the title instead of merely repeating it.

### CATEGORÍA

State exactly one current category from `site-contract.md` as a simple selection value. This normally does not need a writing block because the user selects the category in WordPress rather than pasting prose.

### CUERPO

Use a **separate copyable block containing only the article body**.

The body must:

- start directly with the lede;
- omit the page title and publication date;
- omit field labels such as `CUERPO`;
- contain only text that belongs in the WordPress content field.

Use genuine H2 section headings only when the article benefits from sections. In Markdown-capable harnesses, represent them as `## Heading`; in rich-text harnesses, use actual heading level 2 semantics.

**Never use a standalone bold line as a fake section heading.** Bold text is for emphasis inside prose. This keeps real article headings visually and structurally distinguishable from ordinary emphasis.

Short articles may have no internal headings at all.

## Tags

Do **not** output suggested tags by default. Tags are not part of the user's current publishing workflow.

Only discuss or suggest tags if the user explicitly asks for them or explicitly confirms that tags are available and relevant in the CMS workflow being used.

## Featured image and alt text

Only include an image section when one of these conditions is true:

1. the user actually supplied one or more usable images/visual assets; or
2. the user explicitly asks for help choosing or proposing an image.

If the user did not supply an image and did not ask for an image suggestion, **omit the image section entirely**. Do not invent or recommend a hypothetical stock/editorial image merely because featured images are useful on the site.

When an actual image is supplied:

- identify the specific supplied image to use;
- if several were supplied, choose the strongest candidate and say which one;
- provide factual alt text in its own copyable block when an alt field is useful;
- never expose private data visible in the image unnecessarily.

## Documents and links

If supplied documents or links need to remain attached/linked in the final post, list them **outside the article body block** under a short operational note such as `Documentos para adjuntar` or `Enlaces para incluir`.

Do not place attachment-management instructions inside the copyable article body.

## Editorial alert

The editorial control is always silent unless a real problem requires attention.

When an alert is necessary, it must be **completely separate from every publishable/copyable block**. Never place it inside the article body, the same writing block, or the same Markdown artifact as the publication text.

Use a clearly non-publishable heading such as:

`ALERTA EDITORIAL — NO FORMA PARTE DE LA NOTA`

Then state briefly:

- what was detected;
- where it appears;
- whether it was omitted, neutralized, or left unresolved in the draft;
- what the user should verify before publishing, if anything.

If the harness supports callouts or separate UI blocks, use a separate non-writing callout. The user must be able to copy the article body without capturing the alert.

If there is no real alert, do not mention the editorial-control step.

## Harness fallback

If the harness does not support independent writing blocks, preserve the same separation concept with clearly isolated sections. Never wrap title, excerpt, category, body, operational notes, and alerts into a single copyable artifact.

## Output quality checks

Before delivering, verify that:

- copying the title captures only the title;
- copying the excerpt captures only the excerpt;
- copying the body captures only publishable article content;
- no `LISTO PARA WORDPRESS`, `TÍTULO`, `EXTRACTO`, `CATEGORÍA`, `CUERPO`, or alert text is inside a field's copyable content;
- tags are absent unless explicitly requested;
- image guidance is absent unless an actual image was supplied or the user asked for image help;
- real section headings use H2 semantics rather than bold-only pseudo-headings;
- title and excerpt do not simply repeat one another;
- the opening paragraph explains the event without requiring the attachments;
- article depth matches the material rather than a fixed word count;
- facts added from research are supported;
- victim-centered framing is preserved when crime is involved;
- legal status is accurate;
- category is one of the six current categories;
- attachments support the article but do not contain its only substantive explanation;
- an alert, if necessary, is visibly and mechanically separate from everything the user will publish.