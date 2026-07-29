---
name: effective-comms
description: Router for the comms pass. Determines which gate the communication is at and invokes it — /comms-prep (the brief, at authoring time, Phase 1) or /comms-review (verify-the-prep, rubric, audience review — before delivery). Kept for compatibility; the gates are the skills.
when_to_use: Any moment something written for people is in play and you have not already picked a gate — reports, docs, explainers, commit messages, PR descriptions, help text — "run effective comms", "effective-comms this", "is this ready to send?", "turn these findings into a message for X".
---

# Effective Comms — the router

The comms pass targets the two failure families that dominate agent communications:
**claude-ese** — output in the agent's own dialect that a human cannot comprehend unaided —
and **falsehood** — claims that do not survive comparison with the thing they describe. It
runs as two gates, each its own skill; this router only decides where you are and sends you
there.

## Procedure

Determine the state of the communication, then invoke the gate:

| State | Do |
|---|---|
| No draft yet (a communication is about to exist, or a report trigger fired) | Run `/comms-prep`, write the draft FROM the brief, then run `/comms-review`. |
| Draft exists, no brief (typically: the reader asked "can you effective-comms this") | Run `/comms-prep` retroactively on the draft's intended purpose — the degraded path, named in the audit record — then `/comms-review`. |
| Draft and brief both exist | Run `/comms-review` (it verifies the prep, then reviews). |

The gates carry all rules, rubrics, eval checks, and stop contracts. This router adds none.

**No stack, no return.** Skill invocations are context injections, not a call stack: this
router holds no state and never regains control after sending you to a gate. The pass's
completion rubric therefore lives in `/comms-review` — terminal on every path above — and is
judged over ARTIFACTS (the brief and the audit record), which survive context loss; never
over remembered router context, which may not.

## Exit rubric

This router is complete the moment one of the two gate skills is your NEXT action — you can
name which (`/comms-prep` or `/comms-review`) and the draft/brief state that decided it.
Anything more is the gates' work.

## Pitfalls

- Treating this router as the pass: invoking it and doing neither gate's work.
- Landing here at review time by habit — if communications only ever reach the pass after a
  reader complained, the authoring-time trigger (`/comms-prep` bound to your report
  triggers) is what is missing, not more review.
