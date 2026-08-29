# Default output contract

The primary deliverable is **one single copyable Markdown block containing the complete article body that belongs in the WordPress content editor**.

The user should be able to copy that block once and paste it into WordPress without deleting labels, metadata, operational notes, alerts, image instructions, or other assistant text.

## Primary Markdown block

For a normal article, produce exactly one main writing/Markdown block.

That block must contain only publishable article-body content:

- start directly with the lede;
- include every paragraph that belongs in the article;
- include genuine internal H2 headings when they improve structure;
- include bullet lists only when they belong in the published article;
- include publication-facing source/document links only when the user actually wants them visible in the article;
- omit the WordPress page title because the site renders it separately as the article H1;
- omit the publication date because the site renders it separately;
- omit field labels and workflow labels;
- omit category, excerpt, tags, image instructions, alt text, attachment-management notes, research notes, and editorial alerts.

Never place strings such as `LISTO PARA WORDPRESS`, `TÍTULO`, `EXTRACTO`, `CATEGORÍA`, `CUERPO`, `DOCUMENTOS PARA ADJUNTAR`, `IMAGEN DESTACADA`, or `ALERTA EDITORIAL` inside the main block.

The main block is not a template to be completed by the user. It is the finished publication text.

## Title

The WordPress title is a separate CMS field and must not be duplicated inside the article body.

When providing a suggested title, show **only the final title itself outside the main Markdown block**, without a `TÍTULO` label and without wrapping it into a second copyable artifact unless the user explicitly asks for a separate title block.

Do not provide multiple title alternatives unless requested.

## Excerpt

Do not output a separate excerpt by default.

Instead, write the opening paragraph so it is concise, self-sufficient, and suitable to become or inform WordPress's automatic excerpt/description when applicable.

Only provide a separate excerpt if the user explicitly asks for one or confirms that they need to fill a manual excerpt field.

## Category

Infer the correct current category internally.

If the user benefits from knowing which category to select, mention it outside the main Markdown block as a brief operational note. Never place the category inside the publishable body.

Do not turn category selection into a separate section of the article.

## Tags

Do **not** output suggested tags by default. Tags are not part of the user's current publishing workflow.

Only discuss tags if the user explicitly asks for them or confirms that tags are available and relevant in the CMS workflow being used.

## Images and alt text

Only discuss images when:

1. the user supplied one or more usable images/visual assets; or
2. the user explicitly asks for image help.

If no image was supplied and no image help was requested, say nothing about images.

When an actual image is supplied:

- identify the supplied image to use outside the main Markdown block;
- if several were supplied, choose the strongest candidate and identify it clearly;
- provide the alt text in **a separate copyable block**, never inside the main article Markdown;
- if several images need alt text, provide one separate alt block per actual image;
- never expose private data visible in the image unnecessarily.

## Documents and attachments

Do not create a default `DOCUMENTOS PARA ADJUNTAR` section.

The user already knows which materials they supplied. Mention attachment handling outside the main Markdown block only when there is a concrete reason the user needs an operational instruction, such as:

- one document should not be published because it exposes personal data;
- one source contains an inconsistency that requires review;
- a specific document should be linked visibly from the article and this is not already represented in the body.

If a document link is intended to be visible to readers as part of the published article, it may appear naturally at the end of the main Markdown block. Do not add generic attachment-management prose to the article.

## Editorial alert

The editorial control is always silent unless a real problem requires attention.

When an alert is necessary, place it **outside the main Markdown block and outside every image-alt block**. It must never be captured when the user copies the article.

Use a clearly non-publishable heading such as:

`ALERTA EDITORIAL — NO FORMA PARTE DE LA NOTA`

Then state briefly:

- what was detected;
- where it appears;
- whether it was omitted, neutralized, or left unresolved in the draft;
- what the user should verify before publishing, if anything.

If there is no real alert, do not mention the editorial-control step.

## Article heading semantics

Inside the main Markdown block:

- use `##` only for genuine article section headings;
- never use a standalone bold sentence as a fake heading;
- use bold only for genuine emphasis inside prose;
- short articles may contain no internal headings.

## Harness behavior

When the harness supports a writing/editable Markdown block, use exactly one for the article body.

Do not create multiple blocks for title, excerpt, category, body, or attachments.

A second copyable block is justified only for alt text belonging to an actual supplied image, or when the user explicitly asks for another separately copyable field.

## Output quality checks

Before delivering, verify that:

- there is one primary copyable Markdown block for the full article body;
- copying that block captures only publishable article content;
- no workflow labels or CMS field names are inside it;
- the title is not duplicated as an H1 inside the body;
- no separate excerpt is shown unless requested;
- tags are absent unless explicitly requested;
- image guidance is absent unless an actual image was supplied or the user asked for image help;
- any alt text is outside the main block in a separate block;
- attachment-management instructions are absent unless concretely necessary;
- any editorial alert is mechanically and visually separate from the publishable article;
- genuine article headings use H2 semantics rather than bold-only pseudo-headings;
- the opening paragraph is self-sufficient and useful as an automatic summary;
- article depth matches the material rather than a fixed word count;
- facts added from research are supported;
- victim-centered framing is preserved when crime is involved;
- legal status is accurate;
- the inferred category is one of the six current categories.