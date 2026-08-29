# Examples of adaptive behavior

These examples teach editorial decisions, not wording to copy and not a one-to-one mapping between CMS category and tone.

## Example A — Formal petition: informative + explanatory

**Input pattern**

A one-paragraph message says that Usina filed requests with two victim-assistance bodies and includes two multi-page petitions. No image is supplied.

**Editorial decision**

- Primary event: Usina filed two petitions.
- Purpose: inform what happened and explain what was requested and why.
- Evidence: strong primary documents.
- Mode: **informative + explanatory**.
- CMS category: likely `Incidencia`, assigned only after the editorial mode is chosen.

**Good behavior**

- Read both petitions completely.
- Extract the actual request, legal basis, identified problem, and proposed measures.
- Explain legal material in readable prose without turning the note into a legal brief.
- Produce a richer article because the primary documents contain real additional information.
- Deliver one primary Markdown block containing the final optimized title as its first H1 line, followed by the complete publishable article.
- Do not output tags or hypothetical image suggestions.
- If a source document contains a probable copy/paste error, omit the error from the article and surface an editorial alert outside the publishable block.

**Bad behavior**

- Assume that `Incidencia` requires an aggressive, argumentative, or legalistic tone.
- Copy the petition paragraph by paragraph.
- Add generic SEO filler.

## Example B — Public demand: firm institutional

**Input pattern**

Usina issues a documented request for an authority to change a policy or correct an institutional practice.

**Editorial decision**

- Primary event: public institutional demand.
- Purpose: communicate and substantiate Usina's position.
- Mode: **firm institutional**, possibly with explanatory context.
- CMS category: may also be `Incidencia`.

**Good behavior**

- State clearly what Usina asks and the factual/legal reason.
- Be assertive without exaggeration or insult.
- Keep evidence and established facts distinct from institutional opinion.

**Why this example matters**

This and Example A may share the same CMS category while requiring noticeably different writing tones.

## Example C — Technical reform proposal: analytical + pedagogical

**Input pattern**

Usina presents recommendations based on legislation, comparative information, or a technical report.

**Editorial decision**

- Purpose: explain a problem and make a reasoned proposal understandable.
- Mode: **analytical + pedagogical**.
- CMS category: could still be `Incidencia`.

**Good behavior**

- Explain the problem before technical details.
- Distinguish evidence from recommendation.
- Use headings/bullets only where they improve comprehension.

**Bad behavior**

- Force the same structure or rhetoric used for a public demand merely because both belong to `Incidencia`.

## Example D — Television interview about a victim's case

**Input pattern**

A member of Usina appears on television to discuss a homicide case and the victim's family.

**Editorial decision**

- Primary event: media appearance.
- Purpose: contextualize the intervention and preserve its substantive message.
- Mode: **media-contextual + human**, possibly explanatory.
- CMS category: `Prensa` if the appearance itself is the publication's primary event.

**Good behavior**

- Review the interview or transcript.
- Identify the substantive intervention rather than summarize minute by minute.
- Keep the victim and family central where the crime is discussed.
- Ignore framing from the outlet that romanticizes the offender.

**Bad behavior**

- Sound like a generic media recap simply because the category is `Prensa`.

## Example E — Three photos from an accompaniment activity

**Input pattern**

The user receives a brief description and several photos of an activity with a victim's family.

**Editorial decision**

- Purpose: document what Usina did while treating the people involved with dignity.
- Mode: **informative + human**, or **practical** if guidance is central.
- CMS category: likely `Acompañamiento`, unless the human story itself becomes the primary editorial object.

**Good behavior**

- Keep the note concise when the event is simple.
- Avoid unnecessary personal/location details.
- Recommend only the strongest supplied image outside the main article block.
- Put alt text for the selected image in a separate copyable block.

## Example F — Statistical report

**Input pattern**

A spreadsheet or PDF contains figures about crimes or victimization.

**Editorial decision**

- Purpose: communicate evidence and help readers interpret it accurately.
- Mode: **analytical/evidence-led**.
- CMS category: likely `Observatorio`.

**Good behavior**

- Lead with the strongest supported finding.
- State period, geography, source, methodology, and denominators where needed.
- Distinguish observed data from interpretation.
- Mention material limitations.

**Bad behavior**

- Adopt a rhetorical advocacy tone simply because the implications concern victims or public policy.
- Select the most dramatic number without context.

## Example G — Institutional anniversary with victim remembrance

**Input pattern**

Usina marks an organizational anniversary and remembers people/cases connected to its history.

**Editorial decision**

- Purpose: commemorate and connect institutional history with mission.
- Mode: **commemorative + institutional**, potentially human.
- CMS category: may be `Institucional`.

**Good behavior**

- Use respectful, reflective language.
- Preserve factual precision.
- Avoid bureaucratic corporate language and avoid melodrama.

## Cross-check before drafting

Ask internally:

1. Did I choose the tone because of the actual event and purpose, or merely because of the CMS category?
2. Could another article in the same category legitimately need a different tone? If yes, the separation is working.
3. Could an article in a different category legitimately use a similar tone? If yes, the separation is working.

If category and tone still appear mechanically coupled, reconsider the editorial mode before writing.