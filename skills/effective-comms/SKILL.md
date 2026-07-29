---
name: effective-comms
description: Run a prepare → review → revise pass over an agent-written user-facing output (report, status update, strategy doc, review finding, handoff, recommendation) before it is finalized. Builds a communications brief, then checks named failure modes including hidden context, coordinate-first references, retained rejected ideas, leaked process history, buried recommendations, missing why, mixed-kind lists, consumption-mismatched form, and untyped references.
when_to_use: Before finalizing any non-trivial user-facing output you want checked for its reader. Trigger words/phrases include — "run effective comms", "comms-check this", "is this ready to send/ship?", "review this report/update/handoff for the reader", "did I bury the recommendation?", "turn these findings into a message for X".
---

# Effective Comms

Agents write with context their readers do not have; without a deliberate gate, a technically correct output can still hide its purpose, assumptions, or next action. This skill makes the output land with its reader through a **prepare → review → revise** pass over a draft — or over raw findings about to become one — checking judgment, not prose style. Product-neutral: assume no specific project, company, or tool.

Run it before finalizing any non-trivial output: report, update, strategy/test-strategy/tooling doc, review finding, audit, handoff, worker report, recommendation, decision note. Skip only for genuinely trivial messages (one-line ack, yes/no) with no audience to model. When in doubt, run it — the brief (Phase 1) is cheap.

**Two entry points.** A draft to gate, or raw findings with no message yet. From raw findings you produce either a revised message or, if prep is inadequate, a missing-info / assumptions note. Never silently guess your way to a polished-looking output.

**Interactivity.** Choose one mode before Phase 1:

- **Live** — you can get a user reply within this turn. Ask the user to resolve any brief gap you cannot answer.
- **Non-interactive** — you are a dispatched subagent, background or scheduled run, or mid-task with no one to ask. Do not block and do not guess: park every unresolved gap in a missing-info / assumptions note, place it where **Evidence & uncertainty** (Phase 1, item 4) says uncertainty belongs for this form, and finalize the rest.

**Narrate.** Name the three phases up front; say which you are on. Do not run silently.

## Phase 1 — Communications brief

Write a short brief. Every line is answered or explicitly marked *unknown — and how it resolves* (assume X / ask the user / flag as a gap). An unanswered line is a prep failure.

1. **Objective.** What is this for — explain, convince, surface risk, get a decision? What reader response means it worked? Default for technical/project comms: *help the reader understand the key points well enough to surface genuine confusion, objections, and risks.*
2. **Audience & context.** Who reads it? More than one reader? Under what attention budget?
3. **Knowledge model** — answer all six: what they **need** / **don't need** / **want** / **don't want** to know, what they **already know**, and what you **might be falsely assuming** they know. The last cell is highest-value — assumed-context failures hide there. Never skip it, even for a short output. Author-coined names, labels, and ontologies (IDs, codenames, cluster numbers) belong in the falsely-assuming cell by default: mentioning a label to the reader is not the reader adopting it — it counts as known only once the reader has used it back.
4. **Evidence & uncertainty.** What is solid, an assumption, a guess, blocked, or a decision still needed? Where does uncertainty belong for this form (working note → up front; polished artifact → end/appendix)?
5. **Form factor.** Short message, full report, checklist, handoff, decision note? A single long async dump is not the default shape.

If objective, audience, knowledge model, evidence, or form factor are not adequately answered, do not produce a polished guess — produce a **missing-info / assumptions note** (ask if live; else flag the gaps in the output). If prep cannot support any responsible draft, that note is the terminal output and Phases 2–3 are moot; if you can still finalize part, run Phases 2–3 over what you do produce and carry the parked gaps into it.

## Phase 2 — Review against the rubric

Run **every** check below. For each, find concrete instances in the draft, not a vibe-level "looks fine". Mark each **pass / revised / residual-risk**. An unmarked check means the pass was vibes. Loop Phase 2 → revise → re-check until every row is pass or carries an explicit residual-risk line. A check that cannot be satisfied becomes a residual-risk line in the output or note — never a silent pass.

| # | Check | Catches |
|---|---|---|
| C1 | **Names before coordinates.** Every section/item/ticket/path/ID is named in plain English before or alongside the coordinate; names lead, coordinates support. | "Item 2 fails here" with no meaning. |
| C2 | **No hidden author context.** Self-standing for the brief's audience — nothing relies on context only the author had: working notes, prior conversation, earlier drafts, or reasoning that was never written down. Each needed fact is stated, or flagged as an assumption. | Output assumes the reader shares context only the author had. |
| C3 | **No retained rejected ideas.** When the artifact is the accepted strategy/recommendation, rejected ideas are absent — not kept with rejection notes. (Keep them only when the objective *is* audit / provenance / decision-history.) | Current output carries rejected ideas. |
| C4 | **No process-history leakage.** Tool narration, retries, routing, and the agent's decision history are stripped unless load-bearing for the reader's trust, decision, reproducibility, or handoff. | Reader does not care about your decision history. |
| C5 | **Purpose/audience fit.** Content matches what the audience needs and the objective. No spurious detail, no assumed knowledge they lack. | Written for the agent's logbook, not the reader. |
| C6 | **Recommendation not buried.** Where action is part of the objective, findings carry their implication and the next action is explicit and easy to find. | Reader must re-derive "so what?". |
| C7 | **Uncertainty is legible.** Solid findings, assumptions, guesses, blockers, and open decisions are distinguished and sit in the right place for the form. | Uncertainty hidden, overstated, or misplaced. |
| C8 | **Starts with why.** Any proposal, design, or decision-request opens with the problem it solves and what changes if accepted — stated in the reader's terms and rooted in observed fact, before any mechanics. | Reader meets mechanisms (tiers, lists, schemas) with no idea what they are for; or a "why" asserting projected costs as current facts. |
| C9 | **One list, one kind.** Every list, queue, or section contains a single kind of thing; mixed kinds are split into typed groups (or each item is explicitly typed). A mixed list is an ontology failure surfacing as a comms failure. | A giant list mixing decisions, FYIs, defects, and ideas — the reader must re-sort by kind before they can act on anything. |
| C10 | **Form matches consumption.** Structure, layout, and density are chosen for how the reader will actually consume the artifact: scannable headings, typed lists or tables for parallel/enumerable content, one idea per block, summary before detail. Structure that exists in the content appears on the page. | A wall-of-text paragraph encoding what is really a list or table; a long dump where a layered summary-plus-reference would serve; separator-glyph run-ons standing in for layout. |
| C11 | **References are typed.** Every linked or cited artifact is one of two things, and the text says which: (a) **required reading** — declared as such (it is an extra action being asked of the reader, so it is priced) and reachable as a working clickable link on the surface where the reader will actually read; or (b) **supplemental reference** — in which case the artifact stands alone without it and nothing downstream assumes it was read. | A load-bearing "see X" whose argument collapses unless X is read, never declared required; a required doc cited as a bare file path the reader cannot click on their surface; text that silently assumes a "reference" was actually read. |
| C12 | **Reader's words, not author's coordinates.** Things are named as the reader names them; author-minted identifiers appear parenthetically at most, and count as unknown vocabulary until the reader has adopted them. | A report keyed to the author's private ontology sails through audience review because the author assured the reviewer the reader 'knows the terms'. |

## Phase 3 — Audience review (mandatory; loop until pass)

The author cannot feel the absence of context they hold, so every non-trivial output gets one fresh-perspective review before it is finalized. This is **mandatory** — not optional, not a skim. Judge each round against the **Objective**, **Audience & context**, and audience knowledge model from the brief.

Use exactly one review form in each round:

- **Sub-agent review** (the default whenever you can dispatch a sub-agent) — dispatch one told to *stand in for the target audience*. Pass it, inline, only the audience's likely prior knowledge (from the brief), the objective, and the draft — **not** your working notes, decision history, or this rubric. Build the reviewer's reader-knowledge model from EVIDENCE of adoption — terms the reader has used themselves — never from what the author has told the reader. The author-written briefing is the one unreviewed channel in the loop: an optimistic known-terms list passes the author's blind spots straight through the review.
- **Written self-review** (only when you cannot dispatch a sub-agent; state why in the audit record) — drop the author frame, re-read the draft as the brief's reader, and **write the findings down**. A same-frame skim or an unwritten "looks fine" does not count and does not satisfy this phase.

Either form answers one question: **does this reader, knowing only what the brief says they know, succeed at the objective?**

**Pass — and only then —** when the communication achieves the objective without confusing the reader with spurious information and without omitting anything the reader needs to act.

**Fail** if any of these is true for the reader. Each is a fail on its own:

- left confused, lost, or frustrated;
- unclear what a word, term, phrase, or number refers to;
- unclear why a piece of information is relevant to the objective;
- unclear what they should do or conclude;
- any ambiguity that blocks understanding or action.

On any fail: **log the specific finding, fold it into Phase 2, revise, and run Phase 3 again.** A residual-risk note does not turn a fail into a pass. The reviewer may pass with a residual-risk note only when the disclosed limit does not trigger a fail-condition or block the reader's understanding or action.

## Stop / output contract

Do not finalize until Phase 3 returns a passing review. A passing review may carry explicit residual risks only under the Phase 3 criterion above.

Final output must include the applicable output types:

- a **revised output** when there is enough information to produce one; it must pass the rubric and Phase 3 review;
- a short **residual-risk note** only for a genuine irreducible limit that does not trigger a Phase 3 fail-condition;
- a **missing-info / assumptions note** only when prep is inadequate to finalize responsibly, either as the terminal output or attached to the partial output it qualifies.

Attach the audit record to the artifact itself — as a footer, appendix, or named companion file linked or bundled with it on the review surface — not only to the delivery chat. Record:

- the phases run;
- every check, marked with a cited instance from the draft rather than a bare "pass";
- the Phase 3 form and verdict for every round;
- every Phase 3 finding and its disposition.

A pass claim with no trace outside the author's context counts as not run.

After folding any Phase 3 finding, run Phase 3 again. The loop ends only on the reviewer's passing verdict, never on the author's judgment; committing folded fixes without re-review is a **cut loop** and voids the pass.

Written self-review is permitted only when dispatch is genuinely impossible and that impossibility is stated in the attached record. An instruction forbidding sub-agents does not create impossibility: skill-mandated sub-agents override such fences.

## Boundaries & friction

**Pass-invalidating failures:**

- treating the rubric as optional;
- polishing over an inadequate brief instead of writing the missing-info / assumptions note;
- skipping Phase 3, using a same-frame skim, or passing on a vibe rather than the explicit fail-conditions;
- declaring a pass while any fail-condition still holds;
- giving the audience reviewer the rubric, working notes, or decision history instead of only the reader's prior knowledge, objective, and draft;
- cutting the loop by folding fixes without another Phase 3 review;
- keeping the audit record only in chat or claiming phases that left no visible trace.

**Scope:** This is not a prose-polish or house-style template; it checks judgment, not aesthetics. Form and layout under C10 are judgment because they set the reader's parsing cost. Ornament is aesthetics.

**Extension:** If a check misfires or does not fit the output in hand, surface it to the user rather than silently working around it. To extend the skill, **append** a new failure mode and rubric row; do not redesign it.
