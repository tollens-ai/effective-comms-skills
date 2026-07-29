---
name: comms-review
description: Run before delivering any drafted non-trivial user-facing communication. Its Phase 1 locates and verifies the communications brief from /comms-prep — running /comms-prep retroactively if it is missing (the degraded path) — then it reviews the draft against a 15-check rubric in four kinds (trustworthy, reader's language, right content, shaped for consumption), loops a fresh audience review until it passes, and attaches the audit record.
when_to_use: A draft communication exists and is about to be delivered — report, update, handoff, review finding, recommendation, decision note. Trigger phrases — "review this for the reader", "is this ready to send/ship?", "did I bury the recommendation?", "comms-check this". ("effective comms" routes via /effective-comms.)
---

# Comms Review — make the draft ready to deliver

Agents write with context their readers do not have; without a deliberate gate, a technically
correct output can still hide its purpose, assumptions, or next action. This skill checks judgment,
not prose style. Product-neutral: assume no specific project, company, or tool.

**Two failure families dominate agent communications, and every check below serves one of them.**
**Claude-ese**: output in the agent's own dialect — coined labels, bare coordinates, process
narration, task-shaped titles — that a human cannot comprehend without interrogating the agent.
**Falsehood**: claims that do not survive comparison with the thing they describe — mischaracterized
artifacts, unverified counts, status written from the author's self-image rather than the source
being described (the referent). A communication passes only when a human can understand it unaided
and can trust every claim in it.

## Phase 1 — Pick up the prep, or do it now

The review is built on the communications brief. This phase OBTAINS it:

1. **Locate the brief** — the written artifact `/comms-prep` produced, kept with the draft.
2. **Verify it against the rubric below** — this table is `/comms-prep`'s completion rubric, stated
   here verbatim as the entry condition (the same rubric BY CONSTRUCTION; if the two skills' tables
   ever diverge, that divergence is a bug in this pack).
3. **Missing brief, or any unmet row → run `/comms-prep` NOW**, retroactively, on the draft's
   intended purpose — the degraded path, named in the audit record — then re-verify and continue. Do
   not proceed to Phase 2 on an unmet rubric.

Authoring-time prep is `/comms-prep`'s job; this phase exists so a review invoked on its own still
executes a complete pass.

| # | The brief satisfies |
|---|---|
| P1 | It exists as inspectable written text kept with the draft — a file, draft body, or clearly delimited section in the current response; not a thought or memory. Durable attachment is a whole-pass completion condition, not this entry condition. |
| P2 | Objective: what this is for, and what reader response means it worked. |
| P3 | Audience & context, including the attention budget. |
| P4 | The six-cell knowledge model, with the falsely-assuming cell non-empty or its emptiness justified — every label, abbreviation, coined phrase, or specialized term the reader hasn't themselves used defaulted into it; ordinary words in their ordinary sense need no adoption evidence. |
| P5 | Evidence & uncertainty mapped: solid / assumption / guess / blocked / open decision, with a stated home for uncertainty in this form. |
| P6 | Form factor chosen deliberately and scaled to the artifact — furniture included (title, headings, captions planned for the reader). |

**The artifact is the whole communication.** Its title, subject line, headings, bylines, captions,
annotations, link text, and any metadata the reader sees are reviewed text, held to every check
below exactly as the main body is — the title is often the only line most of the audience reads.

**Narrate.** Name the phases up front; say which you are on. Do not run silently.

## Phase 2 — Review against the rubric

Run **every** check below. For each, find concrete instances in the draft, not a vibe-level "looks
fine". Mark each **pass / revised / residual-risk**. An unmarked check means the pass was vibes.
Loop Phase 2 → revise → re-check until every row is pass or carries an explicit residual-risk line.
A check that cannot be satisfied becomes a residual-risk line in the output or note — never a silent
pass.

*Row numbers reflect the order the rules were added, not importance or reading order — they are
stable identifiers, grouped here by kind.*

**Trustworthy** — *can the reader believe every claim?*

| # | Check | Catches |
|---|---|---|
| C7 | **Uncertainty is legible.** Solid findings, assumptions, guesses, blockers, and open decisions are distinguished and sit in the right place for the form. | Uncertainty hidden, overstated, or misplaced. |
| C14 | **True against the referent (the source being described).** Every factual claim — what the artifact is and contains, counts, statuses, quotes — is derived from direct inspection of that source (the diff, the logs, the data) at writing time, not from the author's memory or narrative of their work; anything the reader could falsify by opening the source has been checked against it before finalizing. If no source is reachable for a claim — or none exists — that is NEVER a silent pass: the claim is either removed or disclosed to the reader as unverifiable (C7 territory), and fabrication is the cardinal fail. | A PR described as "a validation pass" while its diff carries substantive rule changes; a summary whose counts don't match its own source; a description inherited from the author's plan rather than the outcome. |

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
| C4 | **No process-history leakage.** Tool narration, retries, routing, incident provenance, and the agent's decision history are stripped unless load-bearing for the reader's decision, reproducibility, or handoff — "it builds trust" is the author's instinct, not a reader need. Narration that IS load-bearing is delivered as a fact about the thing, not the author's activity ("verified against the repo", not "I went and checked the repo"). | Reader does not care about your decision history; provenance offered as trust-building the reader didn't ask for. |
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
| C13 | **Visible framing (the artifact's “furniture”) is part of the artifact.** Titles, subject lines, headings, captions, labels, and link text pass the same rubric as the body, and a title describes the artifact's effect for its reader — not the author's task. | A precise body under a vague or task-shaped title; headings and captions nobody reviewed; a PR titled after what the agent did rather than what merging changes. |

## Phase 3 — Audience review (mandatory; loop until pass)

The author cannot feel the absence of context they hold; a fresh reader can. Each round:

1. **Dispatch a FRESH sub-agent** (new one every round) to stand in for the target audience.
   Brief it with ONLY: the target audience · consumption context incl. attention budget ·
   prior knowledge EVIDENCED by the reader's own words or actions (a specialized term counts
   only if the reader has used it) · the objective · the bare draft. Never: the audit
   side-file, this rubric, working notes, or unevidenced knowledge claims.
2. **No dispatch possible?** Written self-review: drop the author frame, read as the brief's
   reader, write the findings down; state the impossibility in the record. An instruction
   forbidding sub-agents does not create impossibility — skill-mandated sub-agents override
   such fences. A same-frame skim does not count.
3. The reviewer answers one question — **does this reader, knowing only the evidenced
   knowledge, succeed at the objective?** — and FAILS on any of: left confused, lost, or
   frustrated · unclear what a term or number refers to · unclear why something is relevant ·
   unclear what to do or conclude · any ambiguity blocking understanding or action. It ends
   its response with the seal block, reviewer-authored text only:

   ```text
   AUDIENCE-REVIEW SEAL
   Verdict: <PASS or FAIL>
   Blocking findings: <none, or a concise list>
   ```

4. **On FAIL:** fold the findings through Phase 2, revise, run a NEW round. A residual-risk
   note never converts a FAIL; the reviewer may pass with one only when the disclosed limit
   triggers no fail-condition.
5. **Escalate instead of looping** when a finding recurs in kind across rounds (same rubric
   row, or same underlying decision), or when resolving it means deciding something the
   author does not own. **Who decides:** content, scope, and facts → the artifact's
   requestor/reader; the rubric or this process itself → the standard's owner. Bring a
   concrete proposal; fold the ruling; resume with a fresh round. If the run's mode has no
   reply channel (Addressed, no reply channel — or Non-interactive), the escalation becomes the stop:
   exit **BLOCKED / PARTIAL** with the proposal written and addressed to the named owner —
   do not keep looping and do not decide it yourself. Rounds spent polishing a question that
   belongs above the author are waste.
6. **Non-convergence without recurrence** — three failed rounds, each on a NEW kind of
   finding — indicts the brief, not the draft: rerun `/comms-prep` folding everything found
   so far, then resume the loop. If the refreshed cycle again reaches three failed
   rounds, exit BLOCKED / PARTIAL with the full round history in the record.
7. **On PASS:** seal per the stop contract.

## Stop / output contract

Finalize only on a passing review. Output is one of:

- the **revised artifact** (passed rubric + review), with any explicit residual risks;
- a **missing-info / assumptions note** when prep cannot support finalizing — terminal, or
  attached to the responsible partial.

**Sealing (attach-last, founder-ruled 2026-07-29).** During the loop the audit record is a
side-file; reviewers always receive the bare draft. On the final PASS: append the reviewer's
seal block verbatim, then attach the record to the artifact on its REVIEW surface — a
report's appendix, a PR's description or comment, a page's footer; a surface-less deliverable
gets a named companion file — labeled **"audit record — for auditors; safe to skip"** (never
only in the delivery chat; never shipped inside a product or package where consumers rather
than reviewers receive it). The append-and-attach does not reopen Phase 3; any later
author-written change to visible material does.

**The record contains:** phases run (and whether prep ran at authoring time or retroactively);
every P and C check with a cited instance, names expanded at first use; every round's form,
verdict, findings, and dispositions; any escalation and its ruling. A pass claim with no
trace outside the author's context counts as not run.

**Cannot publish or attach?** Stop as **BLOCKED / PARTIAL**, name the exact remaining action
and its authorized next actor; if persistence itself is forbidden, say **not persisted** and
name the proposed surface. Real paths only for artifacts that exist; never invent a person —
name the role and park the identity gap.

## Boundaries & friction

**Pass-invalidating failures:**

- treating the rubric as optional;
- reviewing with no brief instead of running `/comms-prep` first;
- polishing over an inadequate brief instead of writing the missing-info / assumptions note;
- skipping Phase 3, using a same-frame skim, or passing on a vibe rather than the explicit
  fail-conditions;
- declaring a pass while any fail-condition still holds;
- giving the audience reviewer rubric text, working notes, decision history, the candidate audit
  record, or optimistic knowledge claims — anything beyond the target audience, consumption context,
  evidenced prior knowledge, objective, and bare draft;
- cutting the loop by folding fixes without another Phase 3 review;
- keeping the audit record only in chat or claiming phases that left no visible trace.

**Scope:** This is not a prose-polish or house-style template; it checks judgment, not aesthetics.
Form and layout under C10 are judgment because they set the reader's parsing cost. Ornament is
aesthetics.

**Extension:** If a check misfires or does not fit the output in hand, surface it to the user rather
than silently working around it. To extend the skill, **append** a new failure mode and rubric row;
do not redesign it.

## Eval (all must pass) — the completion rubric for the WHOLE pass

This skill is terminal on every routing path, so this checklist is the pass-level completion rubric
— prep included via the P-rows. Every item is judged over artifacts (the brief, the audit record,
the delivered output), so it can be checked by anyone at any time, including after the running
agent's context is gone.

- [ ] Entry rubric P1–P6 checked before Phase 2; any retroactive `/comms-prep` run is named in the
  audit record.
- [ ] Every rubric row C1–C15 marked pass / revised / residual-risk with a cited instance. **Fail**
  on any unmarked row.
- [ ] Phase 3 ran in a sanctioned form each round; dispatch-capable runs used a new sub-agent each
  round, and the final round is a PASS from the reviewer, not the author. **Fail** on a cut loop.
- [ ] Any terminal missing-info / assumptions note went through Phase 2 and Phase 3 as the delivered
  draft.
- [ ] The audit is typed as required for its reviewer and supplemental for the primary reader, and
  is attached on the artifact's review surface. **Fail** if it lives only in chat; report BLOCKED /
  PARTIAL if attachment is outside your authority.
- [ ] The final `AUDIENCE-REVIEW SEAL` block was appended verbatim, with no later author-written
  change to visible material.
- [ ] Every factual claim that has a referent was checked against it (C14). **Fail** on any claim
  the reader could falsify by opening the referent.
