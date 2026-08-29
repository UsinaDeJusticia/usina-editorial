# Default output contract

The default deliverable is **one single copyable Markdown block** containing the optimized title and the complete article text the user will take into WordPress.

The user prefers copying everything in one action and then moving/adjusting the title manually inside the CMS. Optimize for that workflow rather than splitting CMS fields into separate blocks.

## Primary Markdown block

For a normal article, produce exactly one main writing/Markdown block.

The **first line must always be the final optimized title**, formatted as a Markdown H1:

`# Final optimized title`

Then leave one blank line and start the article lede.

The same block contains the complete publishable article text:

- optimized title as the first line;
- self-sufficient lede immediately after the title;
- every paragraph that belongs in the article;
- genuine internal H2 headings (`##`) when they improve structure;
- bullet lists only when they belong in the published article;
- publication-facing source/document links only when they are intended to be visible to readers.

The user will manually place the first-line title into the WordPress title field and can remove/move that first line from the body before publication. Do not create a second title outside the block.

Never add workflow labels or CMS labels such as `LISTO PARA WORDPRESS`, `TÍTULO`, `EXTRACTO`, `CATEGORÍA`, `CUERPO`, `DOCUMENTOS PARA ADJUNTAR`, or `IMAGEN DESTACADA` around or inside the primary block.

The block is not a template. It is the finished editorial handoff.

## Title quality — always required

Always generate exactly **one final optimized title** for a complete publication unless the user explicitly supplies a final title that must remain unchanged.

Optimize the title simultaneously for:

- human clarity and immediate comprehension;
- search discoverability (SEO);
- machine/agent comprehension and entity clarity (GEO/AI retrieval);
- fidelity to verified facts and Usina's editorial stance.

Prefer titles that naturally identify the principal entity, action/event, and relevant subject when those elements improve comprehension. Preserve important proper names, institutions, places, legal instruments, or case identifiers when materially relevant.

Do not:

- keyword-stuff;
- write clickbait;
- invent consequences or urgency;
- overstate what the sources establish;
- sacrifice readability to an arbitrary character count;
- produce vague headlines that omit the actual event;
- provide several alternatives unless the user asks for options.

## Excerpt

Do not output a separate excerpt by default.

Write the opening paragraph so it is concise, self-sufficient, and suitable to become or inform WordPress's automatic excerpt/description when applicable.

Only provide a separate excerpt if the user explicitly asks for one or confirms that a manual excerpt field must be completed.

If a separate excerpt is requested, keep it outside the primary Markdown block so it cannot be confused with article content.

## Category

Infer the correct current category internally **only for taxonomy/navigation**.

Category must **not** guide tone, voice, structure, length, research depth, or emotional register. Those decisions come first from the event, evidence, editorial purpose, audience need, sensitivity, and the editorial modes in `content-types.md`.

Assign the category only after the editorial mode and structure are settled.

Do **not** show the category in the default output. Only mention it outside the primary block if the user explicitly asks which category to select or if category ambiguity genuinely requires human input.

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
- provide the alt text in **a separate copyable block**, never inside the primary article Markdown;
- if several images need alt text, provide one separate alt block per actual image;
- never expose private data visible in the image unnecessarily.

## Documents and attachments

Do not create a default `DOCUMENTOS PARA ADJUNTAR` section outside the article.

The user already knows which materials were supplied. Mention attachment handling outside the main Markdown block only when there is a concrete reason the user needs an operational instruction, such as:

- one document should not be published because it exposes personal data;
- one source contains an inconsistency that requires review;
- a specific document should be linked visibly from the article and this is not already represented in the body.

If a document or source link is intended to be visible to readers as part of the publication, include it naturally in the primary Markdown block.

## Editorial alert

The editorial control is always silent unless a real problem requires attention.

When an alert is necessary, place it **outside the primary Markdown block and outside every image-alt block**. It must never be captured when the user copies the publication content.

Use a clearly non-publishable heading such as:

`ALERTA EDITORIAL — NO FORMA PARTE DE LA NOTA`

Then state briefly:

- what was detected;
- where it appears;
- whether it was omitted, neutralized, or left unresolved in the draft;
- what the user should verify before publishing, if anything.

If there is no real alert, do not mention the editorial-control step.

## Heading semantics inside the block

- The first line is the only H1 and represents the final title handed off to the CMS.
- Use `##` only for genuine article section headings.
- Never use a standalone bold sentence as a fake heading.
- Use bold only for genuine emphasis inside prose.
- Short articles may contain no H2 headings.

## Harness behavior

When the harness supports a writing/editable Markdown block, use exactly **one primary block** containing title + article.

Do not create a second title block, body block, category block, attachment block, or routine excerpt block.

Additional copyable blocks are justified only for alt text belonging to actual supplied images, or when the user explicitly requests another separately copyable field.

## Output quality checks

Before delivering, verify that:

- there is exactly one primary copyable Markdown block;
- its first line is exactly one final optimized H1 title;
- the title is specific, source-supported, readable, and useful for SEO and machine/agent comprehension without keyword stuffing;
- the lede begins after the title and is self-sufficient;
- copying the block captures the complete editorial handoff and no workflow labels;
- no `TÍTULO`, `CUERPO`, `CATEGORÍA`, `LISTO PARA WORDPRESS`, or similar labels appear in the block;
- no separate title is duplicated outside the block;
- no separate excerpt or category is shown unless requested;
- category did not determine tone or structure;
- tags are absent unless explicitly requested;
- image guidance is absent unless an actual image was supplied or the user asked for image help;
- any alt text is outside the main block in a separate block;
- attachment-management instructions are absent unless concretely necessary;
- any editorial alert is mechanically and visually separate from the primary block;
- genuine internal article headings use H2 semantics rather than bold-only pseudo-headings;
- article depth matches the material rather than a fixed word count;
- facts added from research are supported;
- victim-centered framing is preserved when crime is involved;
- legal status is accurate;
- the internally inferred category is one of the six current categories.