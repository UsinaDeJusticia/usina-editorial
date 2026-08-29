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
- Deliver title, excerpt, and body as separate pasteable fields when the harness supports it. The copyable body contains only article content.
- Do not output suggested tags unless the user asks for them.
- Do not invent or suggest a featured image when no image was supplied and the user did not ask for image help.
- Use real H2 headings only for sections that belong in the article. Do not use bold-only pseudo-headings.
- If one petition contains a probable copy/paste reference to the wrong recipient or jurisdiction, do not reproduce the mistake. Surface `ALERTA EDITORIAL — NO FORMA PARTE DE LA NOTA` outside every pasteable block because the source document itself may need review.

**Bad behavior**

- Copy the supplied paragraph unchanged and attach the PDFs.
- Put `LISTO PARA WORDPRESS`, field labels, tags, image suggestions, article body, attachments, and the alert into one copyable document.
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
- Categorize as `Prensa` when the appearance is the primary event.
- Link/embed the original appearance.
- Ignore host or outlet framing that romanticizes an offender or marginalizes victims.
- Keep operational link/embed instructions outside the copyable article body.

**Bad behavior**

- Write a legal-policy essay simply because criminal law was mentioned.
- Summarize every exchange in chronological order.

## Example C — Three photos from an accompaniment activity

**Input pattern**

The user receives a brief description and several photos of an activity with a victim's family.

**Good behavior**

- Keep the note concise if little additional context is necessary.
- Explain what Usina did and why the activity mattered.
- Categorize as `Acompañamiento` unless the human story itself is clearly the primary publication.
- Avoid unnecessary personal or location details.
- Recommend the strongest **supplied** image and write factual alt text.

**Bad behavior**

- Research unrelated crime statistics just to lengthen the article.
- Publish private information visible in a document/photo without considering necessity.
- Propose a different hypothetical image when the supplied images are usable.

## Example D — Observatorio spreadsheet/report

**Input pattern**

A spreadsheet or PDF contains figures about crimes or victimization.

**Good behavior**

- Lead with the most meaningful supported finding.
- State period, geography, source, and methodology.
- Distinguish observed data from interpretation.
- Mention material limitations.
- Categorize as `Observatorio`.

**Bad behavior**

- Select the most dramatic number without denominator/context.
- Turn missing data into a confident estimate.
