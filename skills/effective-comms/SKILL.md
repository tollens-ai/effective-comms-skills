---
name: effective-comms
description: Run an Effective Comms pass over an agent-written user-facing output before it is finalized — a report, update, strategy doc, review finding, handoff, or recommendation. Prepares a communication brief (objective, audience, what they need/know), then reviews the draft against it and against named communication failure modes (assumed context, numbered references without meaning, retained rejected ideas, leaked process history, buried recommendation), revising or flagging residual risk. Use before any non-trivial user-facing output is considered done.
---

# Effective Comms

This skill makes an agent's user-facing communication actually land with its reader. It runs a **prepare → review → revise** pass over a draft, or over raw findings about to become a draft, so the final output succeeds at its communication objective, fits its audience, and avoids known agent-writing failure modes.

It is **product-neutral**: nothing here assumes a particular project, company, or toolchain. It is useful to anyone whose agent writes reports, updates, strategy docs, review findings, handoffs, or recommendations for a human reader.

This is an early v0. It is a **living checklist**: when a recurring communication failure is found, add it as a named failure mode, a review check, a rubric line, and a regression example in the validation suite. It is deliberately a *judgment* process, not a template — it tells you what to check, not what shape every report must take.

## When to use it

Run the Effective Comms pass **before finalizing** any non-trivial user-facing output:

- a report, status update, or debrief;
- a strategy, test strategy, or tooling strategy document;
- a review finding or audit result;
- a handoff or worker report;
- a recommendation or decision note.

Skip it only for genuinely trivial messages, such as a one-line acknowledgement or a yes/no answer, where there is no audience modeling to do. When in doubt, run it — the brief is cheap.

It can be run two ways:

- **As a gate on an existing draft** — you have a draft and want it checked and revised before it ships.
- **From raw findings** — you have agent findings/notes and no reader-ready message yet. The pass produces either a revised message or, if prep is inadequate, a short missing-info/assumptions note. It never silently guesses its way to a polished-looking output.

## Resolving file paths — do this first

This skill is part of the `effective-comms` plugin. Before anything else, resolve one absolute path and use it throughout:

- **PLUGIN_ROOT** — the plugin's install directory: `${CLAUDE_PLUGIN_ROOT}`. Claude Code expands this to an absolute path when it loads this file; read it off and note it down.

The self-review rubric below lives inline in this file, so no other file is required to run the pass. If you dispatch a subagent for the audience-perspective review, pass it fully-resolved absolute paths and the rubric text it needs — a dispatched subagent inherits none of your context, and the Read tool does no variable expansion.

## The pass — three phases

### Phase 1 — Prepare the communications brief

Before drafting or reviewing, write a short **communications brief**. It does not need to be long, but every line must be answered or explicitly marked *unknown — and how it will be resolved* (will assume X / will ask the user / will flag as a gap). An unanswered line is a prep failure, not a blank to skip.

1. **Objective / what good looks like.** What is this communication *for* — explain, convince, present critical information, get a decision made, surface confusion/objections/risks? What reader response would mean it worked? For technical/project comms the usual default is: *help the reader understand the key points well enough to surface genuine confusion, objections, and risks, because we're working together and want the work to go well.*
2. **Audience and context.** Who reads this? Is there more than one audience? Where and under what attention budget will they read it?
3. **The audience knowledge model** — answer all six explicitly:
   - what they **need** to know;
   - what they **do not need** to know;
   - what they **want** to know;
   - what they **do not want** to know;
   - what they **already know**;
   - what you **might be falsely assuming** they know.
   The last cell is the highest-value one — it is where assumed-context failures hide.
4. **Evidence, uncertainty, confidence.** What is solid, what is an assumption, what is a guess, what is blocked, what decision is still needed? Where should uncertainty sit for this form (working note → up front; polished artifact → end / appendix / side note)?
5. **Form factor / medium.** Should this be a short message, a back-and-forth, a full report, a checklist, a handoff, a decision note? A single long async dump is not the default-correct shape.

**Judge the brief before drafting.** If objective, audience, the knowledge model, evidence/uncertainty, or form factor are not adequately answered, do not produce a polished-looking guess. Produce a **missing-info / assumptions note** instead, and either ask the user (if live) or flag the gaps in the output at the right place for the form.

If the output is short and the reader/objective are already explicit from context, the brief can be a few lines — but the six-cell knowledge model and the "what am I falsely assuming" cell are never skipped.

### Phase 2 — Review the output for comms quality

Compare the draft against the brief and against the communication objective, then run every check in the **self-review rubric** below. This is the gate that catches the named failure modes. For each check, find concrete instances in the draft, not a vibe-level "looks fine".

The output of this phase is one of:

- a **revised** draft that passes the rubric; or
- a draft plus an explicit **residual-risk note** where a check could not be fully satisfied, such as an assumption that cannot be resolved without the user.

### Phase 3 — Audience-perspective review

The audience checkpoint is hard to self-review from the same perspective that wrote the draft — the author knows the hidden context, so they cannot feel its absence. For **non-trivial** outputs, get a fresh perspective:

- **If a subagent/reviewer is available**, dispatch one prompted to *stand in for the target audience* — give it only the audience's likely prior knowledge from the brief and the draft, **not** the agent's scratch context, decision history, or this rubric's answer key. Ask it to read as that audience and flag: assumed knowledge it does not have; internal coordinates/IDs/section-numbers it cannot interpret; spurious detail it does not care about; agent decision/process history irrelevant to it; and any place the output does not achieve its purpose.
- **If no subagent is available**, still perform a separate, explicit audience-perspective pass yourself: deliberately drop the author frame, re-read as the reader described in the brief, and answer the same flag list. A same-frame skim does not count — the pass must be a distinct, written step.

Fold what it flags back into Phase 2 and revise.

## Self-review rubric

The pass cannot be loaded "as vibes". Every check below must be applied and the result recorded (pass / revised / residual-risk). Each check names a failure mode; the first three are the feedback-derived failures this v0 specifically exists to catch.

| # | Check | Failure mode it guards | Verdict |
|---|---|---|---|
| C1 | **Numbered references carry meaning.** Every oracle/section/strategy-item/ticket referenced by number or ID is named in plain English before or alongside the coordinate. | FM-NAMES: "Oracle 2 fails here" with no plain-English meaning. | |
| C2 | **No hidden scratch context.** The output is self-standing for the brief's audience. It does not rely on "as decided in scratch", unstated internal reasoning, or anything only the agent saw. Needed decisions are explained at the right level, or the assumption is flagged as missing. | FM-HIDDEN-CONTEXT: final output assumes the reader saw `.scratch` or internal agent decisions. | |
| C3 | **No retained rejected ideas.** When the artifact is the current accepted strategy/recommendation, rejected agent ideas are absent — not retained with rejection notes. Rejection notes appear only when the communication objective *is* audit / provenance / decision-history. | FM-REJECTED: current output carries rejected ideas with rejection notes. | |
| C4 | **Names before coordinates.** Human-readable names lead; file paths, ticket IDs, line numbers, and internal labels support recognition rather than replace it. | FM-COORDINATES: coordinate-before-name reference. | |
| C5 | **No agent process-history leakage.** Tool-run narration, retries, internal routing, and the agent's decision history are stripped unless load-bearing for the reader's trust, decision, reproducibility, or handoff continuity. | FM-PROCESS-NOISE: "I don't care about your decision history." | |
| C6 | **Purpose/audience fit.** Content matches what the brief's audience needs and the stated objective. No spurious detail the audience does not care about; no assumed knowledge it does not have. | FM-MISMATCH: written for the agent's logbook, not the reader. | |
| C7 | **Recommendation/next action is not buried.** Where action is part of the objective, findings carry their implication and the recommendation/decision/next-action is explicit and easy to find — the reader does not re-derive "so what?". | FM-BURIED: buried recommendation / unclear next action. | |
| C8 | **Uncertainty is legible.** Solid findings, assumptions, guesses, blockers, and decisions-still-needed are distinguished, and uncertainty sits in the right place for the form. | FM-UNCERTAINTY: uncertainty hidden, overstated, or misplaced. | |

A check that cannot be satisfied is not silently passed — it becomes an explicit residual-risk line in the output or in the note back to the user.

## The update loop — how this skill grows

When a new recurring annoying communication failure is found in a real output, fold it in — in the same change — as all four of:

1. a **named failure mode** (FM-…) in the rubric's "guards" column;
2. a **review check** (a new rubric row, or a clause on an existing one);
3. a **self-review rubric line** with its own verdict cell;
4. a **regression example** in the validation suite.

This is what keeps ECS a living checklist rather than a frozen ontology. Do not redesign the pack to add a check; append.

## Stop / output

The pass ends with one of:

- a **revised user-facing output** that passes the rubric (the common success case); or
- the output plus a short **residual-risk note** for checks that could not be fully resolved; or
- a **missing-info / assumptions note** when prep was inadequate and the output cannot responsibly be finalized.

Record which phases and checks ran or were explicitly waived, so the pass is auditable and cannot have been a vibes pass.

## Roadmap — not in v0

State these as plan, not as existing behavior:

- **Multiple-audience staged passes** — write/review for a lower-stakes or internal audience, then transform/review for important stakeholders or a wider audience. v0 proves the single-audience checkpoint first.
- **Artifact-specific leaves** — `write-handoff`, `polish-technical-report`, `convert-findings-to-user-update`, `write-decision-note`, etc. — earn their own skill only once dogfooding shows a recurring template carries judgment beyond this universal pass.
- **Pack integrations** — other public skill packs can invoke this skill as a final communication gate.

## Dogfood status

v0 has been dogfooded through fixture-level validation against three failure modes: numbered references without meaning, hidden scratch context, and retained rejected ideas. This public skill repo contains only the runtime skill/plugin and public docs; validation assets are maintained separately.
