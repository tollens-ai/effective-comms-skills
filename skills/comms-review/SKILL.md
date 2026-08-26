---
name: comms-review
description: Review a drafted non-trivial user-facing communication before delivery. Verify its /comms-prep brief, apply the 15-check rubric, loop a fresh audience review until pass, and attach the audit record.
---

# Comms Review — make the draft ready to deliver

Review the draft for trustworthiness, reader language, content fit, and consumption shape.

**Scope.** Review judgment and consumption form, not prose polish or house style. C10 covers form
and layout because they affect the reader's parsing cost; ornament is outside scope.

Apply the review without assuming a specific product, project, company, or tool.

When the request is to choose the next communication action rather than review an existing draft,
route through `/effective-comms`. This skill is terminal on every route that invokes it.

**Narrate.** Name Phase 1 brief verification, Phase 2 rubric review, and Phase 3 audience review up
front, then say which phase is running.

## Phase 1 — Pick up the prep, or do it now

| # | The brief satisfies |
|---|---|
| P1 | It exists as inspectable written text kept with the draft — a file, draft body, or clearly delimited section in the current response; not a thought or memory. Durable attachment is a whole-pass completion condition, not this entry condition. |
| P2 | Objective: what this is for, and what reader response means it worked. |
| P3 | Audience & context, including the attention budget. |
| P4 | The six-cell knowledge model, with the falsely-assuming cell non-empty or its emptiness justified — every label, abbreviation, coined phrase, or specialized term the reader hasn't themselves used defaulted into it; ordinary words in their ordinary sense need no adoption evidence. |
| P5 | Evidence & uncertainty mapped: solid / assumption / guess / blocked / open decision, with a stated home for uncertainty in this form. |
| P6 | Form factor chosen deliberately and scaled to the artifact — furniture included (title, headings, captions planned for the reader). |

Execute these stages in order:

1. **Locate** the written brief `/comms-prep` produced and kept with the draft.
2. **Compare and verify** every P1–P6 row. If the two skills' tables differ, stop and report a pack
   defect rather than choosing one.
3. **Prepare and re-verify when needed.** If the brief is missing or any row is unmet, run
   `/comms-prep` retroactively on the draft's intended purpose, name the degraded path in the audit
   record, and re-verify. Do not proceed to Phase 2 with an unmet row.
4. **Select the draft.** If retroactive preparation leaves a gap that would force invention or
   overstatement needed for the reader's objective, use the missing-info / assumptions note as the
   delivered draft. Otherwise carry each parked gap into the responsible partial draft. Continue
   with Phase 2 and Phase 3 on the selected draft.

## Phase 2 — Review against the rubric

Run **every** check below. For each, cite concrete instances in the draft. Mark each **pass /
revised / residual-risk candidate**; every row must be marked. Revise any
unmet check within the author's authority. A check may be a residual-risk candidate only when an
identified constraint or unavailable fact prevents resolution and the draft discloses the
resulting limit. Re-check after revision. The candidate becomes residual risk only if the Phase 3
reviewer passes with that disclosed limit; otherwise it remains an unmet check.

Before applying a check, handle a **check mismatch**: if it has no applicable subject and supplies
no N/A path, or satisfying it would contradict the verified objective or evidence, stop and surface
the mismatch with a proposal. Content and fact mismatches go to the requestor; rubric mismatches go
to the standard owner.

**Trustworthy** — *can the reader believe every claim?*

| # | Check | Catches |
|---|---|---|
| C7 | **Uncertainty is legible.** Solid findings, assumptions, guesses, blockers, and open decisions are distinguished and sit in the right place for the form. | Uncertainty hidden, overstated, or misplaced. |
| C14 | **True against the referent (the source being described).** Derive every factual claim — what the artifact is and contains, counts, statuses, quotes — from direct inspection of that source (the diff, logs, or data) at writing time. Check anything the reader could falsify by opening the source. If no source is reachable or none exists, remove the claim or disclose it as unverifiable under C7. | A PR described as "a validation pass" while its diff carries substantive rule changes; a summary whose counts do not match its source; a description inherited from the author's plan rather than the outcome. |

**In the reader's language** — *can they understand it without stopping?*

| # | Check | Catches |
|---|---|---|
| C1 | **Names before coordinates.** Every section/item/ticket/path/ID is named in plain English before or alongside the coordinate; names lead, coordinates support. | "Item 2 fails here" with no meaning. |
| C12 | **Use only terms the reader can use without friction; introduce the rest properly.** Here **term** means a label, abbreviation, coined phrase, tool or domain jargon, or an ordinary word used in a non-ordinary local sense; ordinary words in their ordinary sense need no adoption evidence. A term may be used bare only when you KNOW it is usable without friction for this reader (evidence: they use it themselves). Introducing NEW terminology is welcome when it genuinely helps: expand the first instance in the reader's own terms in a parenthetical, then use the term freely; it counts as adopted once the reader uses it back. Everything else — the author's coinages, other agents' vocabulary, tool and domain jargon — is translated out. | Any agent's private ontology keyed into a report as if shared; a worker's jargon passed through as author-endorsed; a term the reader technically knows but must stop and decode mid-read; a useful new term introduced without its first-use expansion. |

**The right content** — *is this what this reader needs — and nothing else?*

| # | Check | Catches |
|---|---|---|
| C2 | **No hidden author context.** Self-standing for the brief's audience — nothing relies on context only the author had: working notes, prior conversation, earlier drafts, or reasoning that was never written down. Each needed fact is stated, or flagged as an assumption. | Output assumes the reader shares context only the author had. |
| C3 | **No retained rejected ideas.** When the artifact is the accepted strategy/recommendation, rejected ideas are absent — not kept with rejection notes. (Keep them only when the objective *is* audit / provenance / decision-history.) | Current output carries rejected ideas. |
| C4 | **No process-history leakage.** Strip tool narration, retries, routing, incident provenance, and decision history unless required for the reader's decision, reproducibility, or handoff. State required provenance as a fact about the thing ("verified against the repo"), not the author's activity ("I went and checked the repo"). | Non-load-bearing process history presented as reader-facing content. |
| C5 | **Purpose/audience fit.** Content matches what the audience needs and the objective. No spurious detail, no assumed knowledge they lack. | Written for the agent's logbook, not the reader. |
| C8 | **Starts with why.** Any proposal, design, or decision-request opens with the problem it solves and what changes if accepted — stated in the reader's terms and rooted in observed fact, before any mechanics. Purely informational artifacts with no ask may mark this row N/A with one line of reasoning — N/A without the reasoning is an unmarked row. | Reader meets mechanisms (tiers, lists, schemas) with no idea what they are for; or a "why" asserting projected costs as current facts. |
| C15 | **Every clause earns its place.** Length is set by the objective and the reader's attention budget, not the author's momentum: cut padding, throat-clearing, restatement, hedge boilerplate, decorative qualifiers, and anything the brief says the reader neither needs nor wants — at clause grain, not just sentence grain. Brevity comes from SELECTIVITY — dropping what doesn't change the reader's understanding or action — never from compressing what remains into fragments or unglossed jargon. | The same point made in intro, body, and summary; sentences that exist to sound thorough; a two-line answer delivered as a page; "as mentioned above". |

**Shaped for consumption** — *does the form serve how they will actually read it?*

| # | Check | Catches |
|---|---|---|
| C6 | **Recommendation not buried.** Where action is part of the objective, findings carry their implication and the next action is explicit and easy to find. | Reader must re-derive "so what?". |
| C9 | **One list, one kind.** Every list, queue, or section contains a single kind of thing; mixed kinds are split into typed groups (or each item is explicitly typed). A mixed list is an ontology failure surfacing as a comms failure. | A giant list mixing decisions, FYIs, defects, and ideas — the reader must re-sort by kind before they can act on anything. |
| C10 | **Form matches consumption.** Structure, layout, and density are chosen for how the reader will actually consume the artifact: scannable headings, typed lists or tables for parallel/enumerable content, one idea per block, summary before detail. Structure that exists in the content appears on the page. | A wall-of-text paragraph encoding what is really a list or table; a long dump where a layered summary-plus-reference would serve; separator-glyph run-ons standing in for layout. |
| C11 | **References are typed.** Every linked or cited artifact is one of two things, and the text says which: (a) **required reading** — declared as such (it is an extra action being asked of the reader, so it is priced) and reachable as a working clickable link on the surface where the reader will actually read; or (b) **supplemental reference** — in which case the artifact stands alone without it and nothing downstream assumes it was read. | A load-bearing "see X" whose argument collapses unless X is read, never declared required; a required doc cited as a bare file path the reader cannot click on their surface; text that silently assumes a "reference" was actually read. |
| C13 | **Visible framing (the artifact's “furniture”) is part of the artifact.** Titles, subject lines, headings, bylines, captions, annotations, labels, link text, and any other reader-visible metadata pass the same rubric as the body. A title describes the artifact's effect for its reader — not the author's task. | A precise body under a vague or task-shaped title; headings, captions, or metadata nobody reviewed; a PR titled after what the agent did rather than what merging changes. |

## Phase 3 — Audience review (mandatory; loop until pass)

Each round:

1. **Choose the available review form.**
   - **Dispatch available:** dispatch a FRESH sub-agent, new each round, to stand in for the target
     audience. Brief it with ONLY: target audience · consumption context including attention
     budget · prior knowledge EVIDENCED by the reader's own words or actions (a specialized term
     counts only if the reader has used it) · objective · bare draft. Never send the audit
     side-file, this rubric, working notes, or unevidenced knowledge claims.
   - **No dispatch possible:** run a written self-review as **the DEGRADED review form**. Drop the
     author frame, read as the brief's reader, and write the findings down. State the impossibility
     and degradation in the visible record. A same-frame skim does not count.
2. The reviewer answers one question — **does this reader, knowing only the evidenced
   knowledge, succeed at the objective?** — and FAILS on any of: left confused, lost, or
   frustrated · unclear what a term or number refers to · unclear why something is relevant ·
   unclear what to do or conclude · any ambiguity blocking understanding or action. It ends
   its response with the seal block, reviewer-authored text only:

   ```text
   AUDIENCE-REVIEW SEAL
   Verdict: <PASS or FAIL>
   Blocking findings: <none, or a concise list>
   ```

3. **On FAIL, escalate instead of looping** when a finding recurs in kind across rounds (same rubric
   row, or same underlying decision), or when resolving it means deciding something the
   author does not own. **Who decides:** content, scope, and facts → the artifact's
   requestor/reader; the rubric or this process itself → the standard's owner. Bring a
   concrete proposal; fold the ruling; resume with a fresh round. If the run's mode has no
   reply channel (Addressed, no reply channel — or Non-interactive), the escalation becomes the stop:
   exit **BLOCKED / PARTIAL** with the proposal written and addressed to the named owner —
   do not keep looping and do not decide it yourself.
4. **On FAIL, test non-convergence without recurrence:** three failed rounds, each on a NEW kind of
   finding — indicts the brief, not the draft: rerun `/comms-prep` folding everything found
   so far, then resume the loop. If the refreshed cycle again reaches three failed
   rounds, exit BLOCKED / PARTIAL with the full round history in the record.
5. **On any other FAIL:** fold the findings through Phase 2, revise, and run a NEW round.
6. **On PASS:** finalize and attach below.

## After Phase 3 — finalize and attach

Finalize only on a passing review. Output the **revised artifact**, with any explicit residual
risks.

**Sealing (attach-last).** During the loop the audit record is a
side-file; reviewers always receive the bare draft. On the final PASS: append the reviewer's
seal block verbatim, then attach the record to the artifact on its REVIEW surface — a
report's appendix, a PR's description or comment, a page's footer; a surface-less deliverable
gets a named companion file — labeled **"audit record — for auditors; safe to skip"** (never
only in the delivery chat; never shipped inside a product or package where consumers rather
than reviewers receive it). The append-and-attach does not reopen Phase 3; any later
author-written change to visible material does.

**The record contains:** the review mode up front — independent sub-agent (×N rounds) or
**DEGRADED: written self-review**, with the reason — and any other degradation (retroactive
prep) named beside it; phases run (and whether prep ran at authoring time or retroactively);
every P and C check with a cited instance, names expanded at first use; every round's form,
verdict, findings, and dispositions; any escalation and its ruling. A pass claim with no
trace outside the author's context counts as not run.

**Cannot publish or attach?** Stop as **BLOCKED / PARTIAL**, name the exact remaining action
and its authorized next actor; if persistence itself is forbidden, say **not persisted** and
name the proposed surface. Real paths only for artifacts that exist; never invent a person —
name the role and park the identity gap.

## Eval (all must pass) — the completion rubric for the WHOLE pass

Use this checklist after finalization. Every item must hold over the brief, audit record, and
delivered output.

- [ ] Entry rubric P1–P6 was compared across both skills and satisfied before Phase 2; any table
  divergence was reported as a pack defect, and any retroactive `/comms-prep` run is named in the
  audit record.
- [ ] The phases were named up front and narrated as they ran.
- [ ] The review introduced no product, project, company, or tool assumption absent from the task.
- [ ] Every rubric row C1–C15 marked pass / revised / residual-risk with a cited instance. **Fail**
  on any unmarked row.
- [ ] Every Phase 2 revision was re-checked against its affected rows before Phase 3 or finalization.
- [ ] Every residual-risk row names the constraint or unavailable fact and the disclosed limit;
  the final reviewer passed with that limit.
- [ ] The selected delivered draft, including any terminal missing-info / assumptions note or
  responsible partial draft, completed Phase 2 and Phase 3.
- [ ] Phase 3 ran in a sanctioned form each round; dispatch-capable runs used a new sub-agent each
  round, and the final round is a PASS from the reviewer, not the author. **Fail** on a cut loop.
- [ ] Each reviewer received only the target audience, consumption context, evidenced prior
  knowledge, objective, and bare draft.
- [ ] Every failed round was followed by Phase 2 revision and a new review; any finding recurring
  in kind triggered the required escalation.
- [ ] Every check mismatch was either resolved by its N/A path or surfaced to the named decision
  owner with a proposal.
- [ ] Every escalation carried a concrete proposal, and its ruling was applied before a fresh
  review round.
- [ ] If three consecutive failed rounds introduced new finding kinds, `/comms-prep` was refreshed;
  if the refreshed cycle did the same, the result is BLOCKED / PARTIAL with the full round history.
- [ ] The audit is typed as required for its reviewer and supplemental for the primary reader, and
  is attached on the artifact's review surface. **Fail** if it lives only in chat; report BLOCKED /
  PARTIAL if attachment is outside your authority.
- [ ] The attached audit record names review mode and degradations, prep timing, every P and C check
  with a cited instance, each round's form, verdict, findings and dispositions, and every escalation
  with its ruling.
- [ ] The final `AUDIENCE-REVIEW SEAL` block was appended verbatim, with no later author-written
  change to visible material.
- [ ] Every factual claim that has a referent was checked against it (C14). **Fail** on any claim
  the reader could falsify by opening the referent.

## Maintainer reference

To extend the standard, append a new failure mode and rubric row. Change an existing row only with
the standard owner's decision. Do not redesign the standard through an extension.
