---
name: effective-comms
description: >-
  Catcher for the "effective comms" skill trigger — route work to /comms-prep or /comms-review
  depending on whether we are preparing for or reviewing the communication.
---

# Effective Comms — choose the right communication gate

This skill helps you route to the correct part of the Effective Comms skill pack.

## Procedure

Answer the following questions, then select AND PERFORM the action from the table below.

1. Are you ready to start drafting the communication, or do you need to do more underlying work?
2. Is the communication more than a one-line acknowledgement or direct answer (for example,
   yes/no)?
3. Is there already an adequate brief for the communication? An adequate brief is inspectable and
   has accurate, complete answers for objective, audience and context, knowledge model, and form
   factor, including whether a full review is justified.
4. Have you already drafted the communication, or are you reviewing an existing communication?
5. Does the brief say that a full `/comms-review` is justified?

| State | Do |
|---|---|
| Underlying work is still producing the substance to communicate | Stay with that work; no comms gate is due yet. |
| Ready to draft a one-line acknowledgement or yes/no answer with no audience to model | Write it directly; no comms gate is due. |
| Ready to draft, with an adequate brief for the same conversation and objective | Reuse the brief and write the draft from it. When the brief says a full review is justified, run `/comms-review` after drafting. |
| Ready to draft any other communication, with no adequate brief | Run `/comms-prep`, then write the draft from the brief and follow its review decision. |
| Draft exists, with no adequate brief | Run `/comms-prep` retroactively on the draft's intended purpose — the degraded path, named in the audit record — then follow its review decision. |
| Draft and adequate brief both exist; the brief says a full review is justified | Run `/comms-review` (it verifies the prep, then reviews). |
| Draft and adequate brief both exist; the brief does not call for a full review | Deliver the draft directly; no further comms gate is due. |

The gates carry all rules, rubrics, eval checks, and stop contracts. This router adds none.

**No stack, no return.** Skill invocations are context injections, not a call stack: this router
holds no state and never regains control after sending you to a gate. Any path that runs
`/comms-review` uses its completion rubric, judged over the written brief and audit record that
survive context loss rather than remembered router state.
