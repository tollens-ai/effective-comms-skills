---
name: effective-comms
description: Run a prepare → review → revise pass over an agent-written user-facing output (report, status update, strategy doc, review finding, handoff, recommendation) before it is finalized. Builds a short communications brief, reviews the draft against it and against named agent-writing failure modes (assumed context, numbered references without meaning, retained rejected ideas, leaked process history, buried recommendation), then revises or flags residual risk.
when_to_use: Before finalizing any non-trivial user-facing output you want checked for its reader. Triggers — "run effective comms", "comms-check this", "is this ready to send/ship?", "review this report/update/handoff for the reader", "did I bury the recommendation?", "turn these findings into a message for X".
---

# Effective Comms

Make an agent's user-facing output land with its reader. Run a **prepare → review → revise** pass over a draft — or over raw findings about to become one — checking judgment, not prose style. Product-neutral: assume no specific project, company, or tool.

Run it before finalizing any non-trivial output: report, update, strategy/test-strategy/tooling doc, review finding, audit, handoff, worker report, recommendation, decision note. Skip only for genuinely trivial messages (one-line ack, yes/no) with no audience to model. When in doubt, run it — the brief is cheap.

**Two entry points.** A draft to gate, or raw findings with no message yet. From raw findings you produce either a revised message or, if prep is inadequate, a missing-info / assumptions note. Never silently guess your way to a polished-looking output.

**Interactivity.** Live with a user: ask them to resolve any brief gap you cannot answer. Non-interactive (e.g. dispatched subagent): do not block, do not guess — park every unresolved gap in a missing-info / assumptions note at the right place in the output, and finalize the rest.

**Narrate.** Name the three phases up front; say which you are on. Do not run silently.

## Phase 1 — Communications brief

Write a short brief. Every line is answered or explicitly marked *unknown — and how it resolves* (assume X / ask the user / flag as a gap). An unanswered line is a prep failure.

1. **Objective.** What is this for — explain, convince, surface risk, get a decision? What reader response means it worked? Default for technical/project comms: *help the reader understand the key points well enough to surface genuine confusion, objections, and risks.*
2. **Audience & context.** Who reads it? More than one reader? Under what attention budget?
3. **Knowledge model** — answer all six: what they **need** / **don't need** / **want** / **don't want** to know, what they **already know**, and what you **might be falsely assuming** they know. The last cell is highest-value — assumed-context failures hide there. Never skip it, even for a short output.
4. **Evidence & uncertainty.** What is solid, an assumption, a guess, blocked, or a decision still needed? Where does uncertainty belong for this form (working note → up front; polished artifact → end/appendix)?
5. **Form factor.** Short message, full report, checklist, handoff, decision note? A single long async dump is not the default shape.

If objective, audience, knowledge model, evidence, or form factor are not adequately answered, do not produce a polished guess — produce a **missing-info / assumptions note** (ask if live; else flag the gaps in the output).

## Phase 2 — Review against the rubric

Run **every** check below. For each, find concrete instances in the draft, not a vibe-level "looks fine". Mark each **pass / revised / residual-risk**. An unmarked check means the pass was vibes. Loop Phase 2 → revise → re-check until every row is pass or carries an explicit residual-risk line. A check that cannot be satisfied becomes a residual-risk line in the output or note — never a silent pass.

| # | Check | Catches |
|---|---|---|
| C1 | **Names before coordinates.** Every oracle/section/strategy-item/ticket/path/ID is named in plain English before or alongside the coordinate; names lead, coordinates support. | "Oracle 2 fails here" with no meaning. |
| C2 | **No hidden scratch context.** Self-standing for the brief's audience — no reliance on `.scratch`, unstated reasoning, or anything only the agent saw. Needed decisions explained, or flagged as an assumption. | Output assumes the reader saw internal agent context. |
| C3 | **No retained rejected ideas.** When the artifact is the accepted strategy/recommendation, rejected ideas are absent — not kept with rejection notes. (Keep them only when the objective *is* audit / provenance / decision-history.) | Current output carries rejected ideas. |
| C4 | **No process-history leakage.** Tool narration, retries, routing, and the agent's decision history are stripped unless load-bearing for the reader's trust, decision, reproducibility, or handoff. | Reader does not care about your decision history. |
| C5 | **Purpose/audience fit.** Content matches what the audience needs and the objective. No spurious detail, no assumed knowledge they lack. | Written for the agent's logbook, not the reader. |
| C6 | **Recommendation not buried.** Where action is part of the objective, findings carry their implication and the next action is explicit and easy to find. | Reader must re-derive "so what?". |
| C7 | **Uncertainty is legible.** Solid findings, assumptions, guesses, blockers, and open decisions are distinguished and sit in the right place for the form. | Uncertainty hidden, overstated, or misplaced. |

## Phase 3 — Audience-perspective review

The author cannot feel the absence of context they hold. For **non-trivial** outputs, take a fresh perspective:

- **Subagent available:** dispatch one told to *stand in for the target audience*. Pass it, inline, only the audience's likely prior knowledge (from the brief) and the draft — **not** your scratch context, decision history, or this rubric. Ask it to flag: assumed knowledge it lacks; IDs/section-numbers it cannot interpret; spurious detail; agent process history; anywhere the output misses its purpose.
- **No subagent:** still do a distinct, written audience pass yourself — drop the author frame, re-read as the brief's reader, answer the same flags. A same-frame skim does not count.

Fold what it flags back into Phase 2 and revise.

## Stop / output contract

End with exactly one of:

- a **revised output** that passes the rubric (common case);
- the output plus a short **residual-risk note** for checks that could not be fully resolved;
- a **missing-info / assumptions note** when prep was inadequate to finalize responsibly.

Record which phases and checks ran or were waived, so the pass is auditable.

## Boundaries & friction

- **Voids the pass:** treating the rubric as optional; polishing over an inadequate brief instead of writing the note; doing Phase 3 as a same-frame skim; handing the audience reviewer your rubric/context instead of only the reader's prior knowledge and the draft.
- **Not** a prose-polish or house-style template — it checks judgment, not aesthetics.
- If a check misfires or doesn't fit the output in hand, surface it to the user rather than silently working around it. To extend, **append** a new failure mode and rubric row; don't redesign.
