---
name: effective-comms
description: Run a prepare → review → revise pass over an agent-written user-facing output (report, status update, strategy doc, review finding, handoff, recommendation) before it is finalized. Builds a short communications brief, reviews the draft against it and against named agent-writing failure modes (assumed context, numbered references without meaning, retained rejected ideas, leaked process history, buried recommendation), then revises or flags residual risk.
when_to_use: Before finalizing any non-trivial user-facing output you want checked for its reader. Trigger words/phrases include — "run effective comms", "comms-check this", "is this ready to send/ship?", "review this report/update/handoff for the reader", "did I bury the recommendation?", "turn these findings into a message for X".
---

# Effective Comms

Make an agent's user-facing output land with its reader. Run a **prepare → review → revise** pass over a draft — or over raw findings about to become one — checking judgment, not prose style. Product-neutral: assume no specific project, company, or tool.

Run it before finalizing any non-trivial output: report, update, strategy/test-strategy/tooling doc, review finding, audit, handoff, worker report, recommendation, decision note. Skip only for genuinely trivial messages (one-line ack, yes/no) with no audience to model. When in doubt, run it — the brief (Phase 1) is cheap.

**Two entry points.** A draft to gate, or raw findings with no message yet. From raw findings you produce either a revised message or, if prep is inadequate, a missing-info / assumptions note. Never silently guess your way to a polished-looking output.

**Interactivity.** You are *live* only if you can get a user reply within this turn; otherwise treat yourself as *non-interactive* (dispatched subagent, background or scheduled run, or mid-task with no one to ask). Live: ask the user to resolve any brief gap you cannot answer. Non-interactive: do not block, do not guess — park every unresolved gap in a missing-info / assumptions note, placed where Phase 1 item 4 says uncertainty belongs for this form, and finalize the rest.

**Narrate.** Name the three phases up front; say which you are on. Do not run silently.

## Phase 1 — Communications brief

Write a short brief. Every line is answered or explicitly marked *unknown — and how it resolves* (assume X / ask the user / flag as a gap). An unanswered line is a prep failure.

1. **Objective.** What is this for — explain, convince, surface risk, get a decision? What reader response means it worked? Default for technical/project comms: *help the reader understand the key points well enough to surface genuine confusion, objections, and risks.*
2. **Audience & context.** Who reads it? More than one reader? Under what attention budget?
3. **Knowledge model** — answer all six: what they **need** / **don't need** / **want** / **don't want** to know, what they **already know**, and what you **might be falsely assuming** they know. The last cell is highest-value — assumed-context failures hide there. Never skip it, even for a short output.
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

## Phase 3 — Audience review (mandatory; loop until pass)

The author cannot feel the absence of context they hold, so every non-trivial output gets one fresh-perspective review before it is finalized. This is **mandatory** — not optional, not a skim. Run exactly one of the two forms, judged against the **Objective**, **Audience & context**, and audience knowledge model from the brief:

- **Sub-agent review** (the default whenever you can dispatch a sub-agent): dispatch one told to *stand in for the target audience*. Pass it, inline, only the audience's likely prior knowledge (from the brief), the objective, and the draft — **not** your working notes, decision history, or this rubric.
- **Written self-review** (only when you cannot dispatch a sub-agent — state why in the audit record): drop the author frame, re-read the draft as the brief's reader, and **write the findings down**. A same-frame skim or an unwritten "looks fine" does not count and does not satisfy this phase.

Either form answers one question: **does this reader, knowing only what the brief says they know, succeed at the objective?**

**Pass — and only then —** when the communication achieves the objective without confusing the reader with spurious information and without omitting anything the reader needs to act.

**Fail** if any of these is true for the reader. Each is a fail on its own:

- left confused, lost, or frustrated;
- unclear what a word, term, phrase, or number refers to;
- unclear why a piece of information is relevant to the objective;
- unclear what they should do or conclude;
- any ambiguity that blocks understanding or action.

On any fail: **log the specific finding, fold it into Phase 2, revise, and run Phase 3 again.** Loop until the review passes, or until the only items left are genuine residual risks (irreducible limits, not fixable defects) recorded in the output.

## Stop / output contract

Do not finalize until Phase 3 has been run in one of its two forms and either passes or has its open items recorded as residual risk.

Final output must include:

- a **revised output** when there is enough information to produce one; it must pass the rubric and Phase 3 review, except for any explicit residual risks below;
- a short **residual-risk note** only when remaining fail-conditions are genuine irreducible limits, not fixable defects;
- a **missing-info / assumptions note** only when prep is inadequate to finalize responsibly, either as the terminal output or attached to the partial output it qualifies.

Record which phases and checks ran or were waived, the Phase 3 form used and its result, so the pass is auditable.

## Boundaries & friction

- **Voids the pass:** treating the rubric as optional; polishing over an inadequate brief instead of writing the note; skipping Phase 3, doing it as a same-frame skim, or passing it on a vibe instead of against the explicit fail-conditions; declaring a pass while any fail-condition still holds; handing the audience reviewer your rubric/context instead of only the reader's prior knowledge and the draft.
- **Not** a prose-polish or house-style template — it checks judgment, not aesthetics.
- If a check misfires or doesn't fit the output in hand, surface it to the user rather than silently working around it. To extend, **append** a new failure mode and rubric row; don't redesign.
