---
name: comms-prep
description: Create or materially refresh a communications brief at the authoring boundary, immediately before drafting substantive communication. Generally reuse an adequate brief while the conversation and objective remain the same. Use retroactively when a draft exists without an adequate brief.
---

# Comms Prep — prepare before drafting (Phase 1)

Create a written communications brief at authoring time for substantive communication. If the
communication is a one-line acknowledgement or yes/no answer with no audience to model, write it
directly. Otherwise write the draft from the brief, keep them together, and pass both to
`/comms-review`.

## 1. Choose the run mode

**Interactivity.** Choose one mode before starting:

- **Live** — you can get a reply within this turn from someone who holds the answer. Ask them to
  resolve any brief gap you cannot answer.
- **Addressed, no reply channel** — the audience is a real, nameable person, but no reply can reach
  you this turn (the ordinary shape of dispatched writing work). Brief against the REAL audience;
  treat every judgment call as Non-interactive does — park, never guess-and-proceed silently.
- **Non-interactive** — a background or scheduled run, or mid-task with no one to ask. Park every
  unresolved gap in a missing-info / assumptions note, choose where that uncertainty belongs in
  the form, and finalize the rest.

A session can be Live and still hold gaps nobody present can resolve (jargon whose meaning only an
absent author knows): those gaps are handled as Addressed-no-reply-channel — parked and disclosed,
never fabricated.

**Scale.** Scale the brief to the artifact. For a small artifact it may be three lines answered in
seconds: who reads this and when · what must they understand · what would mislead them.

**Adequacy.** A brief is adequate when it is inspectable and its answers for objective, audience
and context, knowledge model, evidence and uncertainty, and form factor are accurate and complete
for the communication.

**Authoring boundary.** Generally run this skill once you can state the intended findings, results,
decision, or recommendation and the evidence or uncertainty supporting it, immediately before
drafting the substantive communication. When the requested work is itself writing, that boundary
is the start of drafting. When underlying work must happen first, stay with that work until those
answers exist; the fact that a report will eventually follow does not move the boundary to task
start.

**Reuse.** The brief belongs to the conversation's communication objective, not to each reply.
While the conversation and objective remain the same, generally reuse an adequate existing brief.
Refresh the affected answers when it is no longer adequate.

**Retroactive use (the degraded path).** If a draft already exists with no brief, prepare the brief
from the draft's intended purpose rather than its text. Name the degradation in the audit record,
then hand both to `/comms-review`.

**Narrate creation or refresh.** Say when you create or materially refresh the brief. Reusing an
adequate brief needs no repeated ceremony.

## 2. Write the communications brief

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

## 3. Check and hand off

Check P1–P6 below, then the additional Eval requirements. The brief is ready to hand off only when
both sets pass. The P1–P6 table is also `/comms-review`'s entry rubric; if the two tables differ,
stop and report a pack defect rather than choosing one.

| # | The brief satisfies |
|---|---|
| P1 | It exists as inspectable written text kept with the draft — a file, draft body, or clearly delimited section in the current response; not a thought or memory. Durable attachment is a whole-pass completion condition, not this entry condition. |
| P2 | Objective: what this is for, and what reader response means it worked. |
| P3 | Audience & context, including the attention budget. |
| P4 | The six-cell knowledge model, with the falsely-assuming cell non-empty or its emptiness justified — every label, abbreviation, coined phrase, or specialized term the reader hasn't themselves used defaulted into it; ordinary words in their ordinary sense need no adoption evidence. |
| P5 | Evidence & uncertainty mapped: solid / assumption / guess / blocked / open decision, with a stated home for uncertainty in this form. |
| P6 | Form factor chosen deliberately and scaled to the artifact — furniture included (title, headings, captions planned for the reader). |

## Eval (all must pass)

- [ ] P1–P6 all hold (the completion rubric above). **Fail** on any silently unmet row.
- [ ] One interactivity mode was chosen before preparation, and unresolved gaps were handled by
      that mode's rule.
- [ ] A reused brief still fits the current objective and material briefing conditions; refresh it
      when it does not.
- [ ] Unanswerable items are explicitly parked with how they resolve — and if prep is inadequate
      overall, the output is a missing-info / assumptions note, not a polished guess.
- [ ] Retroactive runs name the degradation in the audit record.
- [ ] Creation or material refresh was narrated; reuse required no repeated ceremony.

Fix every failed check before handoff. The brief is an artifact, not a thought: keep it with the
draft and hand both to `/comms-review`.

When any brief field remains unresolved, produce a **missing-info / assumptions note**: ask if live;
otherwise flag each gap and how it resolves. If drafting past the gaps would require inventing or
overstating information needed for the reader's objective, the note is the only draft and still
goes through `/comms-review`. Otherwise carry the parked gaps into the partial draft and into
review.
