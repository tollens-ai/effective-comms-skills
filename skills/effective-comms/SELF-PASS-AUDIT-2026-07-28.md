# Effective Comms self-pass audit — 2026-07-28

## Why this record exists

The skill now requires every non-trivial artifact to pass C1–C11, carry an artifact-attached audit trace, and end its audience-review loop only on a reviewer verdict. Those rules had not yet been applied to the document that defines them. This record makes that self-pass inspectable rather than asking a reviewer to trust an unrecorded author judgment.

**Required artifact under review:** [`SKILL.md`](SKILL.md)

## Verdict

**PASS.** One Phase 2 tightening round corrected concrete C1, C5, C7, C8, C9, and C10 failures. The first fresh-audience review then returned **PASS**, so no post-review edit or second self-pass review round was needed. C2, C3, C4, C6, and C11 passed with the cited evidence below. No residual communication risk remains.

## Phase 1 — Communications brief

### Objective

Make the standard executable and auditable:

- a mid-task agent can run the pass correctly under a token budget without repeatedly re-reading the skill; and
- Qing can inspect the rule intent, evidence, revisions, and review outcome before deciding whether to merge the proposal.

The pass succeeds only if both audiences can identify what the skill requires, why each requirement exists, when work may stop, and what evidence supports the self-pass verdict.

### Audiences and context

| Audience | Context and attention budget |
|---|---|
| **Mid-task executing agent** | Already producing a non-trivial artifact, with limited tokens and attention. Needs an unambiguous sequence, checkable rows, typed structures, and no contradictory stop rules. |
| **Qing reviewing the standard** | Reviewing asynchronously and at leisure as the final decider. Needs the intent behind changes, cited evidence, epistemic limits, and a proposal that is safe to leave unmerged. |

### Knowledge model

| Knowledge cell | Mid-task executing agent | Qing reviewing the standard |
|---|---|---|
| **Need to know** | Entry mode, all Phase 1 fields, every C1–C11 check, Phase 3 input boundary, pass/fail rule, re-review trigger, output types, and audit requirements. | Why the self-pass was needed; which checks failed; what changed; whether any rule weakened; how Phase 3 was run; and whether the installed pack version changes. |
| **Do not need to know** | Repository history, author scratch work, pull/branch mechanics, or alternative redesigns. | Tool-by-tool narration, raw agent transcript, or unrelated repository findings. |
| **Want to know** | The shortest reliable path from raw findings or a draft to a finalizable artifact. | Whether the skill obeys its own rules and whether the proposal is reviewable without hidden context. |
| **Do not want to know** | Repeated rules, separator-glyph run-ons, vague “use judgment” gaps, or exceptions that silently weaken the gate. | A polished claim of success without cited rows and reviewer evidence. |
| **Already know** | The artifact and task they are currently handling; ordinary terms such as draft, audience, assumption, and review. | The founder direction for C8–C11, artifact-attached audits, and loop termination on review. |
| **Might be falsely assumed to know** | Why the gate exists, the difference between a disclosed residual risk and a failed audience review, what information a reviewer may receive, or that any edit after review requires re-review. | Exactly where the newly appended rules created mixed lists, density, or stop-contract tension in the current file. |

### Evidence and uncertainty

**Solid evidence:** the pulled `main` version of `README.md`, the pre-revision `SKILL.md`, the revised `SKILL.md`, the complete C1–C11 table below, and the recorded fresh-audience verdict.

**Assumptions:** a mid-task agent knows ordinary software-delivery language but has no prior knowledge of this skill; Qing remains the merge decider.

**Unknowns or blockers:** none block this proposal. Whether Qing prefers different wording is a review decision, not evidence that the procedure is incomplete.

**Uncertainty placement:** this polished audit records any remaining risk at the end. The final pass found none.

### Form factor

The skill remains a product-neutral executable standard: a short why-first introduction, phased procedure, rubric table, typed stop contract, and typed boundaries. This companion audit holds provenance so execution instructions do not become an author-history dump.

## Phase 2 — C1–C11 review and revision

| Check | Initial cited instance and judgment | Revision or final cited instance | Final |
|---|---|---|---|
| **C1 — Names before coordinates** | The interactivity rule said uncertainty belonged where “Phase 1 item 4” specified, making the coordinate lead without its meaning. | It now names **Evidence & uncertainty** before “Phase 1, item 4.” Other coordinates are similarly paired with names, such as **Form and layout under C10**. | **Revised → pass** |
| **C2 — No hidden author context** | The procedure already defined both entry points, live versus non-interactive behavior, every brief field, every review check, and the stop conditions without relying on repository history or this audit. | The final skill remains self-standing; the opening explains the reader problem, and **Two entry points** plus **Interactivity** state the context an executing agent needs. | **Pass** |
| **C3 — No retained rejected ideas** | No rejected wording or abandoned design was retained. Statements such as “not a prose-polish or house-style template” define the accepted scope rather than narrating discarded options. | The final **Scope** block keeps only the operative boundary. | **Pass** |
| **C4 — No process-history leakage** | The skill contains procedure because procedure is its purpose, but no tool retries, branch history, or drafting narration. | Self-pass history lives in this companion audit, not in the executable skill. The skill keeps only load-bearing reproducibility rules such as re-review after a Phase 3 finding. | **Pass** |
| **C5 — Purpose/audience fit** | The frontmatter description named only the earlier failure modes even though the executable rubric now included C8–C11, weakening discoverability for agents deciding whether to invoke it. | The description now also names missing why, mixed-kind lists, consumption-mismatched form, and untyped references. Detailed self-pass provenance stays outside the execution path. | **Revised → pass** |
| **C6 — Recommendation not buried** | Operative actions were already explicit: **Run every check**, **On any fail**, and **Do not finalize until Phase 3 returns a passing review**. | The final stop contract keeps the next action visible and states that every post-review edit triggers another Phase 3 round. | **Pass** |
| **C7 — Uncertainty is legible** | The old Phase 3 text allowed stopping when only residual risks remained, while the appended stop rule said the loop ended on a passing review. That made the status of an unresolved fail-condition ambiguous. | The final rule says a residual-risk note never converts a fail into a pass; a reviewer may pass with one only when it does not trigger a fail-condition or block understanding or action. | **Revised → pass** |
| **C8 — Starts with why** | The opening began “Make an agent's user-facing output land” and immediately introduced the prepare/review/revise mechanism, without first naming the observed author-context problem. | The skill now opens: “Agents write with context their readers do not have,” then states what the gate prevents before introducing mechanics. | **Revised → pass** |
| **C9 — One list, one kind** | **Boundaries & friction** was one mixed list containing pass-invalidating failures, a scope definition, and an extension rule. Its first bullet also accumulated several distinct invalidators in a semicolon chain. | The final section has three typed groups: **Pass-invalidating failures**, **Scope**, and **Extension**. The invalidators are one list of one kind. | **Revised → pass** |
| **C10 — Form matches consumption** | The live/non-interactive branches were embedded in one paragraph. The appended audit, loop, written-review exception, and void rules had become dense run-ons that a token-constrained agent had to unpack. | Interactivity is now a two-item typed list; audit fields are a list; loop termination and the written-review exception are separate blocks; pass invalidators are individually scannable bullets. | **Revised → pass** |
| **C11 — References are typed** | The skill cited no external artifact, so it did not silently impose required reading. Its one same-document coordinate was a C1 problem, not an external-reference dependency. | The final skill remains self-standing and has no external linked or cited artifact. In this audit, `SKILL.md` is explicitly typed above as the **required artifact under review** and linked on the review surface. | **Pass** |

### Internal-coherence re-check

The four appended amendments now agree with the earlier procedure:

- **Phase 3 and stop contract:** both require a reviewer pass before finalization.
- **Residual risks:** only non-blocking disclosed limits may accompany a pass; unresolved fail-conditions remain failures.
- **Loop termination:** every folded audience finding triggers another Phase 3 round; only the reviewer ends the loop.
- **Reviewer form:** sub-agent review is the default; written self-review is allowed only when dispatch is genuinely impossible.
- **Audit placement:** the trace must be attached as a footer, appendix, or named companion on the review surface, not left only in chat.
- **Extension convention:** new failure modes still append a rubric row rather than redesigning the skill.

No rule was weakened, and the skill remains product-neutral.

## Phase 3 — Fresh audience review

### Round 1 setup

**Form:** sub-agent review.

The reviewer was told to stand in for a mid-task agent under a tight token budget with no prior knowledge of Effective Comms. It received only the revised `SKILL.md` and a realistic gating task: turn raw flaky-deploy findings into a concise decision note for an engineering lead. The task supplied measured production and staging outcomes, an immediate timeout mitigation, an unknown root cause, and a follow-up investigation. The reviewer was not given the work brief, author notes, change rationale, or this audit.

**Done oracle:** produce the phase narration, complete brief with all six knowledge cells, decision note, C1–C11 cited outcomes, skill-mandated audience review, and a binary verdict on whether the procedure was executable without re-reading or inferred steps.

### Round 1 verdict and dispositions

**Verdict: PASS.**

The reviewer completed every requested output. Its simulated execution caught a C8 ordering issue in its own first decision-note draft, moved the observed deploy problem before the timeout request, and re-ran its own audience review before finalizing. It reported no blocking confusion, omitted action, or missing procedure in `SKILL.md`.

| Reviewer observation | Type | Disposition |
|---|---|---|
| C6 requires an easy-to-find action while C8 requires the problem to lead. | Non-blocking friction | No skill change. The checks are compatible: the simulation passed by using a short why section followed immediately by a named decision section. Adding another rule would create redundancy. |
| Mandatory review has a noticeable token cost even for a short artifact. | Non-blocking friction | No skill change. The cost is intentional and the skill already provides a narrow reviewer-input contract. Weakening the mandatory gate would violate the brief. |

Because the reviewer passed the revised skill and produced no fixable finding, no edit followed this verdict and no second self-pass review round was required. The loop terminated on the reviewer's judgment, not the author's.

## Final status

- **Phases run:** Phase 1, complete C1–C11 Phase 2 review/revision/re-check, and Phase 3 sub-agent review.
- **Final reviewer verdict:** PASS.
- **Residual risks:** none.
- **Missing information:** none.
- **Release propagation:** plugin version bumped from `0.1.0` to `0.2.0` so installed caches can receive the revised rubric.
