# Write the communications brief

Write a short brief. Go step by step and answer every line. Each line is answered or explicitly
marked *unknown — and how it resolves* (assume X / ask the user / flag as a gap).

1. **Objective.** What is this for — for example, explain, convince, surface risk, or get a
   decision? What should change for the reader if the communication succeeds? For technical comms,
   the objective might be: *help the reader understand the key points well enough to surface
   genuine confusion, objections, and risks.* Describe the deliverable: for example a chat reply,
   a single document, a document plus a short handoff. When the request is to improve an existing
   communication, the deliverable is the improved communication itself, not just findings about
   it.
2. **Audience & context.** Who reads it? More than one reader? Are they friendly or critical? Under
   what attention budget? What are their expectations for this communication?
3. **Knowledge model** — six key questions about the audience: what they **need** / **don't need**
   / **want** / **don't want** to know, what they **already know**, and what you **might be falsely
   assuming** they know. The last cell is highest-value — a failure of assumed context results in
   "wait, what?" and repeated effort. Never skip it, even for a short output.

   **Language and jargon.** The communication must avoid context-specific terms (labels,
   abbreviations, coined phrases, tools, or domain jargon) that you don't have evidence the user is
   comfortable with. This part of the prep must determine what that looks like. You need to use
   your judgement on what terminology the audience is confident with and what needs to be
   rephrased. If they've used the term themselves, that is strong evidence. Having read the term
   recently, or it being ordinary knowledge for their role, could also be evidence, but is not a
   guarantee of knowledge. Highlight specific classes of terms (e.g. section headings and
   abbreviations) to avoid. A term that is unfamiliar to the user should be defined in the
   communication at its first use if it's helpful for communicating the objective; otherwise try
   to avoid unfamiliar terms.
4. **Source meaning that must be preserved.** When the communication describes, rewrites, or
   summarises source material, list the key points that must be preserved in the rewrite: for
   example ordered procedures, instructions, and checklists; numerical or factual information;
   distinctions the source draws, such as who owns what or which system does which job; conflicts,
   contradictions, and uncertainties in the source; explicit exclusions; and the requested scope,
   so a writing task stays a writing task. This list is what the review rechecks after every
   revision.
5. **Form factor.** What's the right form factor for this communication? Short message, checklist,
   multi-section document, multiple documents? Every part of the communication is part of the form
   factor — consider what attached text the reader will see (title, subject line, headings,
   captions, labels, commit messages) and whether any of these have separate objectives or
   audiences. If the communication is complex and requires a multi-section or multi-document form,
   read [Structure plan](structure.md) before drafting prose. If communication *about* this communication is
   required — for example, surfacing issues, uncertainties, or decisions — plan where it will
   go. Working notes stay outside the communication and need not persist after the review unless
   the user explicitly asks for a record.
6. **Style and conventions.** Which house style conventions, writing skills, and instructions in
   your prompts or project files apply to this communication? Find them before writing and name
   them here, so the draft follows them and the review checks against them.

## Check before drafting

Verify the following stopping conditions before continuing. Go back and review or redo if
necessary to ensure a good-quality communication brief.

- [ ] every line of the brief is answered or explicitly parked with how it resolves;
- [ ] the "falsely assuming" question has been answered or its absence justified, and it names
      the terms you will introduce or avoid;
- [ ] the source-meaning list exists whenever there is source material;
- [ ] the decision on whether a full `/comms-review` is justified is written down;
- [ ] the applicable style conventions and skills are named;
- [ ] the brief introduced no new information that is not justified from the sources; and
- [ ] the brief stays separate from anything you will return to the reader.
