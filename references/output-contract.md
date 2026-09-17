# Default output contract

The default deliverable is a **finished article rendered normally in the conversation interface** so the user can move it into WordPress with minimal editing.

Do not present the article as source code. Do not wrap it in a fenced Markdown block, do not label it as `.md`, and do not optimize for one-click copying if that requires exposing raw markup.

## Default rendered handoff

For a normal article:

1. Show exactly **one final optimized title** as the first visible element, using a normal rendered heading.
2. Leave normal visual spacing and begin the lede immediately below it.
3. Continue with the complete publishable article body.
4. Use rendered H2 headings only when they improve structure.
5. Use bullets, emphasis, and reader-facing links only when they belong in the article.

The title is conceptually a separate WordPress field even though it appears directly above the article in the handoff. The body begins with the lede and must not contain a duplicate title.

Never add workflow labels such as `LISTO PARA WORDPRESS`, `TÍTULO`, `EXTRACTO`, `CATEGORÍA`, `CUERPO`, `DOCUMENTOS PARA ADJUNTAR`, or `IMAGEN DESTACADA` around or inside the article by default.

## Clean publication surface

The publishable article must be clean and must not expose the research process.

- Do not place tool citations, file citations, source IDs, internal verification markers, harness provenance markers, or research-only URLs inside the article body.
- Sources consulted for verification do not become reader-facing links by default.
- Add links only when they have an editorial purpose for the reader or when the user explicitly asks to preserve them.
- Preserve explicitly requested links and place each one naturally once unless repetition is editorially justified.
- If the runtime requires citations for traceability, keep them outside the publishable article whenever the interface permits it.
- Do not deliberately emit citation markup, source IDs, footnotes, or a `Sources`/`Fuentes` list as part of the WordPress copy unless the user explicitly requests that editorial feature.
- Host-generated source pills/chips or a platform Sources panel are interface metadata, not reader-facing editorial links. Do not duplicate them in the prose. A skill cannot suppress system-level citation UI when the host requires it; ensure the underlying article text remains clean.

## Rendering rule

Prefer normal rich-text/rendered presentation.

- Do **not** enclose the article in triple backticks.
- Do **not** use a `markdown` code fence.
- Do **not** present the answer as a raw Markdown artifact or `.md` file by default.
- If the harness uses Markdown as its rendering language, use ordinary unfenced Markdown so headings and lists appear rendered to the user.
- If rich rendering is unavailable, use clean plain text with the title and section headings on their own lines rather than exposing raw Markdown source syntax.

The user should see the article, not the markup used to render it.

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

If a separate excerpt is requested, place it outside the article and present it as ordinary rendered text rather than a code block unless the user explicitly asks for copy-only formatting.

## Category

Infer the correct current category internally **only for taxonomy/navigation**.

Category must **not** guide tone, voice, structure, length, research depth, or emotional register. Those decisions come first from the event, evidence, editorial purpose, audience need, sensitivity, and the editorial modes in `content-types.md`.

Assign the category only after the editorial mode and structure are settled.

Do **not** show the category in the default output. Only mention it outside the article if the user explicitly asks which category to select or if category ambiguity genuinely requires human input.

## Tags

Do **not** output suggested tags by default. Tags are not part of the user's current publishing workflow.

Only discuss tags if the user explicitly asks for them or confirms that tags are available and relevant in the CMS workflow being used.

## Images and alt text

Only discuss images when:

1. the user supplied one or more usable images/visual assets; or
2. the user explicitly asks for image help.

If no image was supplied and no image help was requested, say nothing about images.

When an actual image is supplied:

- identify the supplied image to use outside the article;
- if several were supplied, choose the strongest candidate and identify it clearly;
- provide factual alt text outside the article as ordinary rendered text;
- use a separate copy-only block for alt text only if the user explicitly requests that format;
- never expose private data visible in the image unnecessarily.

## Documents and attachments

Do not create a default `DOCUMENTOS PARA ADJUNTAR` section outside the article.

The user already knows which materials were supplied. Mention attachment handling outside the article only when there is a concrete reason the user needs an operational instruction, such as:

- one document should not be published because it exposes personal data;
- one source contains an inconsistency that requires review;
- a specific document should be linked visibly from the article and this is not already represented in the body.

If a document or source link is intended to be visible to readers as part of the publication, include it naturally in the article.

## Editorial alert

The editorial control is always silent unless a real problem requires attention.

When an alert is necessary, place it **outside the publishable article and outside image/alt guidance**. It must never look like part of the note.

Use a clearly non-publishable heading such as:

`ALERTA EDITORIAL — NO FORMA PARTE DE LA NOTA`

Then state briefly:

- what was detected;
- where it appears;
- whether it was omitted, neutralized, or left unresolved in the draft;
- what the user should verify before publishing, if anything.

If there is no real alert, do not mention the editorial-control step.

## Heading semantics

- The displayed title is the only H1-equivalent element in the editorial handoff.
- The WordPress title field ultimately renders the public page H1; therefore the body portion must not repeat the title.
- Use rendered H2 semantics only for genuine article section headings.
- Never use a standalone bold sentence as a fake heading.
- Use bold only for genuine emphasis inside prose.
- Short articles may contain no H2 headings.

## Harness behavior

When the harness supports rich or rendered text, use it directly.

When the harness internally uses Markdown, keep it **unfenced** so the UI renders the article normally. Never use a code fence merely to create a copy button.

When the harness cannot render formatting, use clean plain text rather than raw Markdown source.

Additional separately formatted material is justified only when the user explicitly requests it or when an editorial alert must be isolated from the article.

## Output quality checks

Before delivering, verify that:

- the user sees a finished article rather than Markdown source;
- the article is not inside a fenced code block;
- there is exactly one final optimized title;
- the title is specific, source-supported, readable, and useful for SEO and machine/agent comprehension without keyword stuffing;
- the lede begins immediately after the title and is self-sufficient;
- the body does not repeat the title;
- no workflow or CMS labels appear inside the article;
- no separate excerpt or category is shown unless requested or operationally necessary;
- category did not determine tone or structure;
- tags are absent unless explicitly requested;
- image guidance is absent unless an actual image was supplied or the user asked for image help;
- any image/alt guidance is outside the article;
- attachment-management instructions are absent unless concretely necessary;
- any editorial alert is mechanically and visually separate from the article;
- genuine internal article headings use H2 semantics rather than bold-only pseudo-headings;
- article depth matches the material rather than a fixed word count;
- a substantively rich judicial or legal primary document has not been compressed into a thin update merely because the operative result is simple;
- facts added from research are supported;
- victim-centered framing is preserved when crime is involved;
- legal status is accurate;
- the internally inferred category is one of the six current categories.
