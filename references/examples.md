# Examples of adaptive behavior

These examples teach decisions, not wording to copy.

## Example A — Incidencia from a short text plus two petitions

**Input pattern**

A one-paragraph message says that Usina filed requests with two victim-assistance bodies and includes two multi-page petitions. No image is supplied.

**Good behavior**

- Read both petitions completely.
- Extract the actual request, legal basis, identified problem, and proposed measures.
- Produce an `Incidencia` article substantially richer than the one-paragraph message because the primary documents contain real additional information.
- Keep the PDFs as supporting documents rather than the only place where the legal substance appears.
- Deliver one primary Markdown block containing the final optimized title as its first H1 line, followed by the complete publishable article.
- Do not place title labels, excerpt labels, category labels, attachment instructions, tags, image suggestions, or alerts inside that block.
- Do not output a second title outside the block.
- Do not output a separate excerpt unless the user asks for one.
- Do not output suggested tags unless the user asks for them.
- Do not invent or suggest a featured image when no image was supplied and the user did not ask for image help.
- Use real H2 headings only for sections that belong in the article. Do not use bold-only pseudo-headings.
- If one petition contains a probable copy/paste reference to the wrong recipient or jurisdiction, do not reproduce the mistake. Surface `ALERTA EDITORIAL — NO FORMA PARTE DE LA NOTA` outside the publishable Markdown block because the source document itself may need review.

**Bad behavior**

- Copy the supplied paragraph unchanged and attach the PDFs.
- Omit the title and make the user invent it manually.
- Put the title in a separate block that forces the user to copy twice.
- Return a form-like package containing `TÍTULO`, `EXTRACTO`, `CATEGORÍA`, `CUERPO`, or `DOCUMENTOS PARA ADJUNTAR` as part of the copyable artifact.
- Split the publishable content across several copyable blocks.
- Suggest stock/editorial imagery when the user supplied none.
- Add generic SEO filler.
- Generate JSON-LD or deployment instructions.
- Treat the legal/incidence section structure as mandatory for every future post.

## Example B — Television interview

**Input pattern**

A short message says a member of Usina appeared on television, with a link to the interview.

**Good behavior**

- Review the interview or available transcript.
- Identify the actual topic and Usina's substantive position.
- Add only enough background to make the discussion understandable.
- Make the first line of the primary Markdown block one final optimized H1 title that makes the participant/topic/event explicit when useful.
- Categorize internally as `Prensa` when the appearance is the primary event.
- Link/embed the original appearance when that link belongs in the published article.
- Ignore host or outlet framing that romanticizes an offender or marginalizes victims.
- Keep non-publishable operational instructions outside the main Markdown block.

**Bad behavior**

- Write a legal-policy essay simply because criminal law was mentioned.
- Summarize every exchange in chronological order.
- Use a vague title such as `Entrevista en televisión` when the substantive topic can be named accurately.

## Example C — Three photos from an accompaniment activity

**Input pattern**

The user receives a brief description and several photos of an activity with a victim's family.

**Good behavior**

- Keep the note concise if little additional context is necessary.
- Explain what Usina did and why the activity mattered.
- Put one final accurate title as the first H1 line of the primary Markdown block without sensationalizing the victim's story.
- Categorize internally as `Acompañamiento` unless the human story itself is clearly the primary publication.
- Avoid unnecessary personal or location details.
- Recommend the strongest **supplied** image outside the main article block.
- Put the alt text for the selected actual image in its own separate copyable block.

**Bad behavior**

- Research unrelated crime statistics just to lengthen the article.
- Publish private information visible in a document/photo without considering necessity.
- Propose a different hypothetical image when the supplied images are usable.
- Put alt text inside the article Markdown block.

## Example D — Observatorio spreadsheet/report

**Input pattern**

A spreadsheet or PDF contains figures about crimes or victimization.

**Good behavior**

- Lead with the most meaningful supported finding.
- Put one final title as the first H1 line of the primary Markdown block, identifying the subject, period/geography, or principal finding when those elements materially improve understanding and discoverability.
- State period, geography, source, and methodology.
- Distinguish observed data from interpretation.
- Mention material limitations.
- Categorize internally as `Observatorio`.

**Bad behavior**

- Select the most dramatic number without denominator/context.
- Turn missing data into a confident estimate.
- Write a sensational title that overstates what the dataset supports.
