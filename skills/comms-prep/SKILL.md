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

# Comms Prep — prepare before drafting (Phase 1)

A communication's success depends on its being appropriate for its audience, meeting their needs,
and having a clear measure of success. This skill helps you prepare the information you need to
succeed. Once your draft is written, run `/comms-review`; your brief becomes the reviewer's
briefing.

**Be liberal: any time you are writing something for people, think comms-prep.**

## 1. Decide whether to reuse or prepare

**Adequacy.** A brief is adequate when its answers for objective, audience and context, knowledge
model, and form factor are accurate and complete for the communication.

**Reuse.** While the conversation and objective remain the same, generally reuse an adequate
existing brief. You can amend an existing brief if something has changed and it is no longer
adequate. If the form is a back-and-forth communication, it is not necessary to prepare again for
each reply.

If the brief cannot be reused, choose one interactivity mode before creating or refreshing it:

- **Live** — you can get a reply within this turn from someone who holds the answer.
- **Non-interactive** — a delegated, background or scheduled run, or mid-task with no one to ask.

If a question arises during comms prep and you do not know the answer, ask the user in a Live
session. In a Non-interactive session, note the ambiguity in the brief and use an appropriate
escalation path if you cannot guarantee the quality of the resulting communication.

A session can be Live and still hold gaps nobody present can resolve, such as jargon whose meaning
only an absent author knows. Use your best judgement together, and document the ambiguity.

**Scale.** Scale the brief to the artifact. For a small artifact it may be four lines answered in
seconds: who reads this and when · what do you know that they don't · what must they understand ·
what would mislead them.

**Authoring boundary.** Generally run this skill once you have finished working out the actual
information you need to communicate and immediately before drafting the substantive communication.
When the requested work is itself writing, that boundary is the start of drafting. When underlying
work must happen first, stay with that work until those answers exist; the fact that a report will
eventually follow does not move the boundary to task start.

**Retroactive use (the degraded path).** If a draft already exists with no brief, prepare the brief
from the draft's intended purpose rather than its text. Name the degradation in the audit record,
then hand both to `/comms-review`.

## 2. Write the communications brief

Write a short brief. Go step by step and answer every line. Each line is answered or explicitly
marked *unknown — and how it resolves* (assume X / ask the user / flag as a gap).

1. **Objective.** What is this for — for example, explain, convince, surface risk, or get a
   decision? What should change for the reader if the communication succeeds? For technical comms,
   the objective might be: *help the reader understand the key points well enough to surface
   genuine confusion, objections, and risks.*
2. **Audience & context.** Who reads it? More than one reader? Are they friendly or critical? Under
   what attention budget? What are their expectations for this communication?
3. **Knowledge model** — answer all six: what they **need** / **don't need** / **want** / **don't
   want** to know, what they **already know**, and what you **might be falsely assuming** they know.
   The last cell is highest-value — a failure of assumed context results in "wait, what?" and
   repeated effort. Never skip it, even for a short output. As part of potential false assumptions,
   highlight classes of context-specific terms (labels, abbreviations, coined phrases, tools, or
   domain jargon) that you don't have evidence the user is comfortable with. A term having been
   mentioned to the reader, or written in another communication, is not evidence that the reader
   has adopted it.
4. **Form factor.** What's the right form factor for this communication? Short message, checklist,
   multi-section document, multiple documents? Every part of the communication is part of the form
   factor — consider what attached text the reader will see (title, subject line, headings,
   captions, labels, commit messages) and whether any of these have separate objectives or
   audiences. If the communication is complex and requires a multi-section or multi-document form,
   follow the structure-planning guidance below. If communication *about* this communication is
   required — for example, surfacing issues, uncertainties, or decisions — plan where it will
   go: inline, in a chat reply, or in an accompanying note.

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

## 3. Check and hand off

Check the rubrics P1–P5 below, then the additional Eval checklist. The brief is ready to hand off
only when both sets pass. The P1–P5 table is also `/comms-review`'s entry rubric; if the two
tables differ, please help us by reporting a defect with the effective-comms-skills pack.

When any brief field remains unresolved despite your best efforts, produce a **missing-info /
assumptions note**: ask if Live, or put it in an accompanying note otherwise. Do not overstate your
certainty or confidence level.

| # | The brief satisfies |
|---|---|
| P1 | It exists as inspectable written text kept with the draft — a file, draft body, or clearly delimited section in the current response; not a thought or memory. Durable attachment is a whole-pass completion condition. |
| P2 | Clearly describes objective: what this is for, and what reader response means it worked. |
| P3 | Clearly describes audience & context, including the attention budget. |
| P4 | Fills out the six-cell knowledge model, with the falsely-assuming cell non-empty or its emptiness justified — every label, abbreviation, coined phrase, or specialized term the reader hasn't themselves used defaulted into it; ordinary words in their ordinary sense need no adoption evidence. |
| P5 | Form factor chosen deliberately and scaled to the artifact — including any additional communication components (title, headings, captions planned for the reader); any uncertainty, limitations, unresolved issues, or open decisions have a planned reader-visible home; whether a full `/comms-review` is justified has been decided from the objective, audience, and cost of failure, with a reminder in the brief when it is; multi-section documents have a written structure plan (each section's job and kind; siblings the same kind; reader-path order); long documents (substantially more than a page) have that plan reviewed against the objective before drafting, and re-reviewed before any structural revision. |

## Eval Checklist (all must pass)

- [ ] P1–P5 all hold (the completion rubric above). **Fail** on any silently unmet row.
- [ ] One interactivity mode was chosen before preparation, and unresolved gaps were handled by
      that mode's rule.
- [ ] A reused brief still fits the current objective and material briefing conditions; refresh it
      when it does not.
- [ ] Unanswerable items are explicitly parked with how they resolve — and if prep is inadequate
      overall, the output is a missing-info / assumptions note, not a polished guess.
- [ ] Retroactive runs name the degradation in the audit record.
- [ ] The brief introduced no product, project, company, or tool assumption absent from the task.

Fix every failed check before handoff. The brief is an artifact, not a thought: keep it with the
draft and hand both to `/comms-review`.
