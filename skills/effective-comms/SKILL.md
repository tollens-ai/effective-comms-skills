---
name: effective-comms
description: Run an Effective Comms pass over an agent-written user-facing output before it is finalized — a report, status update, strategy doc, review finding, handoff, or recommendation. Prepares a communications brief (objective, audience, what they need/know), reviews the draft against it and against named communication failure modes (assumed context, numbered references without meaning, retained rejected ideas, leaked process history, buried recommendation), then revises or flags residual risk. Use before any non-trivial user-facing output is considered done.
when_to_use: When an agent is about to finalize a non-trivial user-facing output and you want it checked for its reader. Trigger phrases — "run effective comms", "comms-check this", "is this ready to send/ship?", "review this report/update/handoff for the reader", "will the reader actually understand this?", "did I bury the recommendation?", "turn these findings into a message for X".
---

# Effective Comms

Make an agent's user-facing communication actually land with its reader. This skill runs a **prepare → review → revise** pass over a draft — or over raw findings about to become a draft — so the output meets its communication objective, fits its audience, and avoids known agent-writing failure modes.

It is **product-neutral**: nothing here assumes a particular project, company, or toolchain. It is a **judgment** process, not a template — it tells you what to check, not what shape every report must take. It applies to anyone whose agent writes reports, updates, strategy docs, review findings, handoffs, or recommendations for a human reader.

## When to use it

Run the pass **before finalizing** any non-trivial user-facing output: a report, status update, or debrief; a strategy / test-strategy / tooling-strategy document; a review finding or audit result; a handoff or worker report; a recommendation or decision note.

Skip it only for genuinely trivial messages — a one-line acknowledgement, a yes/no answer — where there is no audience to model. When in doubt, run it; the brief is cheap.

It runs two ways:

- **As a gate on an existing draft** — you have a draft and want it checked and revised before it ships.
- **From raw findings** — you have agent notes and no reader-ready message yet. The pass produces either a revised message or, if prep is inadequate, a short missing-info / assumptions note. It never silently guesses its way to a polished-looking output.

## Interactivity

**Either.** When run live with a user, ask them to resolve any brief gap you cannot answer. When run non-interactively (e.g. dispatched to a subagent), do not block and do not guess: **the deferral mechanism is the missing-info / assumptions note** — park every unresolved gap there, in the output at the right place for the form, and finalize the rest. Never invent context to fill a blank.

## Narrate as you go

Before you begin, give a one-line rundown of the three phases. At each phase, say which one you are on and whether you are running the pass or just discussing it. Do not run silently.

## The pass — three phases

### Phase 1 — Prepare the communications brief

Before drafting or reviewing, write a short **communications brief**. It need not be long, but every line must be answered or explicitly marked *unknown — and how it will be resolved* (will assume X / will ask the user / will flag as a gap). An unanswered line is a prep failure, not a blank to skip.

1. **Objective / what good looks like.** What is this communication *for* — explain, convince, present critical information, get a decision made, surface confusion/objections/risks? What reader response would mean it worked? Usual default for technical/project comms: *help the reader understand the key points well enough to surface genuine confusion, objections, and risks, because we're working together and want the work to go well.*
2. **Audience and context.** Who reads this? More than one audience? Where and under what attention budget will they read it?
3. **The audience knowledge model** — answer all six explicitly:
   - what they **need** to know;
   - what they **do not need** to know;
   - what they **want** to know;
   - what they **do not want** to know;
   - what they **already know**;
   - what you **might be falsely assuming** they know.
   The last cell is the highest-value one — it is where assumed-context failures hide.
4. **Evidence, uncertainty, confidence.** What is solid, what is an assumption, what is a guess, what is blocked, what decision is still needed? Where should uncertainty sit for this form (working note → up front; polished artifact → end / appendix / side note)?
5. **Form factor / medium.** Short message, back-and-forth, full report, checklist, handoff, decision note? A single long async dump is not the default-correct shape.

**Judge the brief before drafting.** If objective, audience, the knowledge model, evidence/uncertainty, or form factor are not adequately answered, do not produce a polished-looking guess — produce a **missing-info / assumptions note** instead (ask the user if live; otherwise flag the gaps in the output). If the output is short and the reader/objective are already explicit from context, the brief can be a few lines — but the six-cell knowledge model, and the "what am I falsely assuming" cell, are never skipped.

### Phase 2 — Review the output for comms quality

Compare the draft against the brief and the objective, then run **every** check in the self-review rubric below. For each check, find concrete instances in the draft, not a vibe-level "looks fine". The output of this phase is either a **revised** draft that passes the rubric, or a draft plus an explicit **residual-risk note** where a check could not be fully satisfied (e.g. an assumption that cannot be resolved without the user).

### Phase 3 — Audience-perspective review

The audience checkpoint is hard to self-review from the perspective that wrote the draft — the author knows the hidden context, so they cannot feel its absence. For **non-trivial** outputs, get a fresh perspective:

- **If a subagent/reviewer is available**, dispatch one prompted to *stand in for the target audience*. A dispatched subagent inherits none of your context, so pass it, inline, only the audience's likely prior knowledge from the brief and the draft — **not** the agent's scratch context, decision history, or this rubric's answer key. Ask it to read as that audience and flag: assumed knowledge it does not have; internal coordinates/IDs/section-numbers it cannot interpret; spurious detail it does not care about; agent decision/process history irrelevant to it; and any place the output does not achieve its purpose.
- **If no subagent is available**, still perform a separate, explicit audience-perspective pass yourself: drop the author frame, re-read as the reader described in the brief, and answer the same flag list. A same-frame skim does not count — it must be a distinct, written step.

Fold what it flags back into Phase 2 and revise.

## Self-review rubric

This is the eval, and it is mandatory: apply every check and record the result (**pass / revised / residual-risk**) — a check left unmarked means the pass was run as vibes. Loop Phase 2 → revise → re-check until every row is pass or carries an explicit residual-risk line. Each check names the failure mode (bad-output smell) it guards; the first three are the feedback-derived failures this v0 exists to catch.

| # | Check | Failure mode it guards | Verdict |
|---|---|---|---|
| C1 | **Numbered references carry meaning.** Every oracle/section/strategy-item/ticket referenced by number or ID is named in plain English before or alongside the coordinate. | FM-NAMES: "Oracle 2 fails here" with no plain-English meaning. | |
| C2 | **No hidden scratch context.** The output is self-standing for the brief's audience. It does not rely on "as decided in scratch", unstated internal reasoning, or anything only the agent saw. Needed decisions are explained at the right level, or the assumption is flagged as missing. | FM-HIDDEN-CONTEXT: final output assumes the reader saw `.scratch` or internal agent decisions. | |
| C3 | **No retained rejected ideas.** When the artifact is the current accepted strategy/recommendation, rejected agent ideas are absent — not retained with rejection notes. Rejection notes appear only when the objective *is* audit / provenance / decision-history. | FM-REJECTED: current output carries rejected ideas with rejection notes. | |
| C4 | **Names before coordinates.** Human-readable names lead; file paths, ticket IDs, line numbers, and internal labels support recognition rather than replace it. | FM-COORDINATES: coordinate-before-name reference. | |
| C5 | **No agent process-history leakage.** Tool-run narration, retries, internal routing, and the agent's decision history are stripped unless load-bearing for the reader's trust, decision, reproducibility, or handoff continuity. | FM-PROCESS-NOISE: reader does not care about your decision history. | |
| C6 | **Purpose/audience fit.** Content matches what the brief's audience needs and the stated objective. No spurious detail the audience does not care about; no assumed knowledge it does not have. | FM-MISMATCH: written for the agent's logbook, not the reader. | |
| C7 | **Recommendation/next action is not buried.** Where action is part of the objective, findings carry their implication and the recommendation/decision/next-action is explicit and easy to find — the reader does not re-derive "so what?". | FM-BURIED: buried recommendation / unclear next action. | |
| C8 | **Uncertainty is legible.** Solid findings, assumptions, guesses, blockers, and decisions-still-needed are distinguished, and uncertainty sits in the right place for the form. | FM-UNCERTAINTY: uncertainty hidden, overstated, or misplaced. | |

A check that cannot be satisfied is not silently passed — it becomes an explicit residual-risk line in the output or in the note back to the user.

## How this skill grows

This is a living checklist, not a frozen ontology. When a new recurring communication failure is found in a real output, fold it in — in the same change — as all of: a **named failure mode** (FM-…), a **review check** (a new rubric row or a clause on an existing one), its **verdict cell**, and a **regression example** in the separately maintained validation suite. Append; do not redesign the rubric to add a check.

## Stop / output contract

The pass ends with exactly one of:

- a **revised user-facing output** that passes the rubric (the common success case); or
- the output plus a short **residual-risk note** for checks that could not be fully resolved; or
- a **missing-info / assumptions note** when prep was inadequate and the output cannot responsibly be finalized.

Record which phases and checks ran or were explicitly waived, so the pass is auditable and cannot have been a vibes pass.

## Pitfalls / boundaries — and what it does NOT do

- **Failure modes that void the pass:** treating the rubric as optional (an unmarked check is a failed pass); polishing over an inadequate brief instead of writing the missing-info note; doing Phase 3 as a same-frame author skim; or handing the audience reviewer the rubric/agent context instead of only the reader's prior knowledge and the draft.
- **Not a prose-polish / copywriting template.** It does not impose a house style, tone, or fixed report shape; it checks judgment, not aesthetics.
- **Not in v0 (stated as plan, not behavior):** multiple-audience staged passes; artifact-specific companion skills (`write-handoff`, `polish-technical-report`, …) earned only if dogfooding shows recurring template-carrying judgment; other packs invoking this as a final comms gate.

## Friction note

If applying this skill hits a bug, friction, or a check that doesn't make sense for the output in hand (a spurious pass/fail, an unclear cell, a rubric row that doesn't fit), surface it to the user / superagent rather than silently working around it. The skill improves by being challenged.

## Dogfood log

- **v0** — validated against three failure modes (numbered references without meaning, hidden scratch context, retained rejected ideas) through fixture-level runs, and dogfooded as the final comms gate on real outputs.
