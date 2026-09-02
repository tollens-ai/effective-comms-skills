---
name: comms-prep
description: >-
  Write yourself a brief about the communication's objective and audience in order to communicate
  more successfully. Use immediately before drafting human-facing findings, explanations,
  recommendations, decision requests, or text intended for publication or reuse. For example, use
  before writing human-facing READMEs, PR messages in public repos, tutorials, documentation,
  recommendations, error messages, reports, or website copy. If the communication will come at the
  end of a piece of work, do the work first and invoke the skill later — for example, finish the
  bug fix and then call comms-prep when you are about to explain what you did to the user. While the
  conversation and objective remain the same, you can reuse the existing brief rather than invoke
  the skill again to write a new one. Use retroactively when a draft exists without an adequate
  brief.
---

# Comms Prep — prepare before drafting

A communication's success depends on its being appropriate for its audience, meeting their needs,
and having a clear measure of success. This skill helps you prepare the information you need to
succeed. Once your draft is written, run `/comms-review`; your brief supplies the objective,
audience, context, evidence sources, and structure plan if appropriate. This is useful both when
you are drafting and for independent review agents.

**Be liberal: any time you are writing something for people, think comms-prep.**

## 1. Decide whether to reuse or prepare

**Adequacy.** A brief is adequate when its answers for objective, audience and context, knowledge
model, source content, form factor, and style conventions are accurate and complete for the
communication.

**Reuse.** While the conversation and objective remain the same, generally reuse an adequate
existing brief. You can amend an existing brief if something has changed and it is no longer
adequate. If the form is a back-and-forth communication, it is not necessary to prepare again for
each reply.

**Scale.** Scale the brief to the artifact. For a small artifact it may be four lines answered in
seconds: who reads this and when · what do you know that they don't · what must they understand ·
what would mislead them.

**Authoring boundary.** Generally run this skill once you have finished working out the actual
information you need to communicate and immediately before drafting the substantive communication.
When the requested work is itself writing, that boundary is the start of drafting. When underlying
work must happen first, stay with that work until those answers exist; the fact that a report will
eventually follow does not move the boundary to task start.

**Retroactive use.** If a draft already exists with no brief, prepare the brief from the draft's
intended purpose rather than copying assumptions out of its text. Then make the brief and draft
available to `/comms-review`.

**Where it lives.** The brief is an artifact, not a thought: keep it available with the draft for
`/comms-review` reviewers, while keeping it outside the primary reader-facing communication. Keep
it in your own scratch space, in context, or as a brief summary directly in chat if appropriate.
Do not include the brief with the workspace or files for the audience; this would generally not
be appropriate.

## 2. Write the communications brief

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
   follow the structure-planning guidance below. If communication *about* this communication is
   required — for example, surfacing issues, uncertainties, or decisions — plan where it will
   go. Working notes stay outside the communication and need not persist after the review unless
   the user explicitly asks for a record.
6. **Style and conventions.** Which house style conventions, writing skills, and instructions in
   your prompts or project files apply to this communication? Find them before writing and name
   them here, so the draft follows them and the review checks against them.

### Add a reminder to call `/comms-review`

Decide whether the communication is substantive enough to justify running `/comms-review` once it
is complete. `/comms-review` uses an audience-review loop to check that the communication meets its
objective and avoids common failure modes. Judge whether that work is proportionate by considering
the objective, audience, and cost of failure. In most circumstances, a few rounds of review cost
less than repeated back-and-forth with a confused human. They almost certainly cost less than
misleading a wide audience.

If a full review is justified, add a note to the end of the brief instructing the drafting agent to
invoke `/comms-review` when the draft is complete.

### Structure plan for multi-section and long documents

For a multi-section or multi-document communication, write and review the plan first: ordered and
nested headings or titles, bullet points, and one line or a few bullet points naming each section's
objective. Self-review the plan against the high-level objective and audience before continuing.
The following rubrics are guidance, not an exhaustive list — use your judgement to achieve the
best plan before drafting prose.

**Rubrics for categorising section headings**

- Each level's children partition their parent along some clear axis — for example, domain, phase,
  view, work-item type, or audience. If the axis cannot be named in a phrase, this nesting level may
  mix unlike things and cause confusion.
- Generate each axis's "missing siblings" — things the audience might reasonably expect at that
  level. If that produces sections you do not intend to write, the axis may be miscategorised or
  mislabelled.
- Sibling headings are the same "kind of thing." For the drafting agent's convenience, annotate
  this in the plan.
- Each piece of content you want to write has one clear home. Pressure to duplicate a fact is a
  structure signal.
- Each likely reader question routes to one obvious heading.
- Uncertainty, limitations, unresolved issues, and open decisions have an explicit home appropriate
  to their importance rather than being scattered or buried.
- The order follows the reader's path through the subject, not the author's path through the
  sources.

Combining sources can be where structural issues appear: a document assembled in encounter order
can read as a pile of good content in a random structure.

For a long document — substantially more than a page — the structure plan is itself a reviewable
artifact. Review its headings and topic bullets against the communications brief before drafting,
the way a software design is reviewed before code. The outline is the cheapest version of the
document, so a structural bug found there costs a bullet edit instead of a rewrite. A structural
revision retriggers this gate: edit and re-review the plan before changing the prose.

## 3. Unresolved questions

If a question arises during comms prep and you don't know the answer, ask the user when you can
get a reply this turn. Otherwise, note the issue in the brief, and use an appropriate escalation
path if this significantly affects the quality of the communication. Even when you can ask,
sometimes neither of you knows the answer (for example, some information the absent author hasn't
provided). Use your best judgement together, and document ambiguity. Do not overstate your
certainty or confidence level. Never make stuff up. If some particular part of the communication
is not possible, say so, but deliver any unaffected or unrelated remaining parts.

## 4. Check and hand off

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

## 5. Writing the communication

Once you have a good communication brief, use it to go and write a good communication. Say what
you mean, as simply as benefits your objective. Avoid mannered prose and metaphor unless it carries
key meaning that serves the objective and audience.

Follow the style conventions and skills the brief names.
