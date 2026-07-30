---
name: comms-prep
description: Run the moment you are about to write ANYTHING for people — reports, documents, explainers, commit messages, PR titles and descriptions, help text, error messages, READMEs, page copy, announcements. Produces the communications brief (objective, audience, knowledge model, evidence, form factor) the draft is written from; /comms-review requires it as input. The brief scales to the artifact — three lines for a commit message. Running it after a draft exists is the degraded path.
when_to_use: Any time you are about to write something a person will read — a report, document, explainer, handoff, review finding, recommendation, decision note, commit message, PR title or description, help text, error message, README, page copy — or a report trigger fired (a stakeholder ask, a scheduled digest, a run-out-of-work report). Also retroactively when a draft exists with no brief. Trigger phrases — "write me a report/doc/explainer", "prep this comms", "who is this for?". ("effective comms" routes via /effective-comms.)
---

# Comms Prep — prepare before drafting (Phase 1)

A communication is shaped by decisions made before its first sentence: who it is for, what they
need, what counts as it working. This skill is that preparation, run as its own gate at authoring
time — the draft is then WRITTEN FROM the brief, and the brief travels with the draft to
`/comms-review`, where it becomes the reviewer's briefing. Skipping prep and "fixing it in review"
compresses these decisions into the worst moment: the reader saying "I don't understand" is prep
arriving late. Product-neutral: assume no specific project, company, or tool.

**Be liberal: any time you are writing something for people, think comms-prep.** Reports, updates,
strategy docs, review findings, audits, handoffs, worker reports, recommendations, decision notes —
and equally the small furniture-sized artifacts: commit messages, PR titles and descriptions, help
text, error messages, READMEs, page copy. **The brief scales to the artifact**: for a commit message
it is three lines answered in seconds (who reads this and when · what must they understand · what
would mislead them). Cost is never the reason to skip — prep is far cheaper than review, and cheaper
still than a reader's confusion. Skip only for genuinely trivial messages (a one-line ack, a yes/no)
with no audience to model. When in doubt, run it.

**Interactivity.** Choose one mode before starting:

- **Live** — you can get a reply within this turn from someone who holds the answer. Ask them to
  resolve any brief gap you cannot answer.
- **Addressed, no reply channel** — the audience is a real, nameable person, but no reply can reach
  you this turn (the ordinary shape of dispatched writing work). Brief against the REAL audience;
  treat every judgment call as Non-interactive does — park, never guess-and-proceed silently.
- **Non-interactive** — a background or scheduled run, or mid-task with no one to ask. Park every
  unresolved gap in a missing-info / assumptions note, place it where **Evidence & uncertainty**
  (item 4) says uncertainty belongs for this form, and finalize the rest.

A session can be Live and still hold gaps nobody present can resolve (jargon whose meaning only an
absent author knows): those gaps are handled as Addressed-no-reply-channel — parked and disclosed,
never fabricated.

**Narrate.** Say that you are running comms-prep. Do not run silently.

## The communications brief (Phase 1 of the pass)

Write a short brief. Every line is answered or explicitly marked *unknown — and how it resolves*
(assume X / ask the user / flag as a gap). An unanswered line is a prep failure.

1. **Objective.** What is this for — explain, convince, surface risk, get a decision? What reader
   response means it worked? Default for technical/project comms: *help the reader understand the
   key points well enough to surface genuine confusion, objections, and risks.*
2. **Audience & context.** Who reads it? More than one reader? Under what attention budget?
3. **Knowledge model** — answer all six: what they **need** / **don't need** / **want** / **don't
   want** to know, what they **already know**, and what you **might be falsely assuming** they know.
   The last cell is highest-value — assumed-context failures hide there. Never skip it, even for a
   short output. Here **term** means a label, abbreviation, coined phrase, tool or domain jargon, or
   an ordinary word used in a non-ordinary local sense; ordinary words in their ordinary sense need
   no adoption evidence. A term the reader has not themselves used belongs in the falsely-assuming
   cell by default: mentioning it to the reader, or receiving it from another agent, is not the
   reader adopting it; it is usable without friction only once the reader has used it back.
4. **Evidence & uncertainty.** What is solid, an assumption, a guess, blocked, or a decision still
   needed? Where does uncertainty belong for this form (working note → up front; polished artifact →
   end/appendix)?
5. **Form factor.** Short message, full report, checklist, handoff, decision note? A single long
   async dump is not the default shape. The furniture is part of the form — plan here what attached
   text the reader will see (title, subject line, headings, captions, labels) and what each must do
   for them; a title describes the artifact's effect for its reader, not the author's task. It is
   all written from this brief and reviewed under the same rubric as the body (C13).
   **For a multi-section document, the form answer includes a structure plan** — the ordered
   headings with one line each stating that section's job and its KIND — checked two ways before
   any prose is written: sibling headings are the same kind of thing (a domain next to a domain,
   not a domain next to a technique), and the order follows the reader's path through the subject,
   not the author's path through the sources. Combining sources is where this fails silently: a
   document assembled in the order the material was encountered reads as content vomit however
   good each section is.
   **For a LONG document (substantially more than a page), the structure plan is itself a
   reviewable artifact and is reviewed BEFORE drafting** — headings plus topic bullets, tested
   against the brief's objective the way a software design is reviewed before code: review is
   testing, and the outline is the cheapest artifact the document will ever be, so a structural
   bug found there costs a bullet edit instead of a rewrite. Revising an existing long document's
   structure re-triggers this — edit and re-review the plan first, then the prose; iterating
   structure in place is the failure mode this step exists to stop.

## Stop / output contract

The brief is an ARTIFACT, not a thought: written down, kept with the draft, and handed to
`/comms-review` — its knowledge model (especially the falsely-assuming cell and the list of terms
the reader has used themselves, which is the evidence of adoption) is what the audience reviewer's
briefing is built from.

If objective, audience, knowledge model, evidence, or form factor cannot be adequately answered, do
not proceed to a polished guess — produce a **missing-info / assumptions note** (ask if live; else
flag the gaps). If prep cannot support any responsible draft, that note is the only responsible
draft: “terminal” names its output type, not a review waiver, so hand it to `/comms-review`. If a
partial draft is still responsible, carry the parked gaps into it and into review.

**Retroactive use (the degraded path).** If a draft already exists with no brief, run this skill
FIRST, on the draft's intended purpose rather than its text — then hand both to `/comms-review`.
Name the degradation in the audit record.

## Completion rubric — the brief is done when all six hold (P1–P6)

This table is the skill's exit condition, and BY CONSTRUCTION it is also `/comms-review`'s entry
rubric — the two are the same rubric stated in both skills; if they ever diverge, that divergence is
a bug in this pack.

| # | The brief satisfies |
|---|---|
| P1 | It exists as inspectable written text kept with the draft — a file, draft body, or clearly delimited section in the current response; not a thought or memory. Durable attachment is a whole-pass completion condition, not this entry condition. |
| P2 | Objective: what this is for, and what reader response means it worked. |
| P3 | Audience & context, including the attention budget. |
| P4 | The six-cell knowledge model, with the falsely-assuming cell non-empty or its emptiness justified — every label, abbreviation, coined phrase, or specialized term the reader hasn't themselves used defaulted into it; ordinary words in their ordinary sense need no adoption evidence. |
| P5 | Evidence & uncertainty mapped: solid / assumption / guess / blocked / open decision, with a stated home for uncertainty in this form. |
| P6 | Form factor chosen deliberately and scaled to the artifact — furniture included (title, headings, captions planned for the reader); multi-section documents have a written structure plan (each section's job and kind; siblings the same kind; reader-path order); long documents (substantially more than a page) have that plan reviewed against the objective before drafting, and re-reviewed before any structural revision. |

## Eval (all must pass)

- [ ] P1–P6 all hold (the completion rubric above). **Fail** on any silently unmet row.
- [ ] Unanswerable items are explicitly parked with how they resolve — and if prep is inadequate
  overall, the output is a missing-info / assumptions note, not a polished guess.
- [ ] Retroactive runs name the degradation.

## Pitfalls

- Running after the draft exists and not naming it — the degraded path hidden as the normal one.
- The brief as a mental exercise instead of an artifact — `/comms-review`'s reviewer briefing is
  BUILT from it; an unwritten brief rebuilds the author's blind spots downstream.
- Marking the author's own coinages (or another agent's jargon) as "already known" — mentioning is
  not evidence that the reader can use the term without friction.
- Answering the knowledge model for a generic reader instead of THIS reader under THIS attention
  budget.
- Collaging sources in encounter-order — a combined or synthesized document inheriting its
  section structure from wherever the content happened to come from, instead of from the reader's
  ontology of the subject. The tell: sibling headings of mixed kinds, and a topic the reader would
  ask for first buried under the author's first source.
