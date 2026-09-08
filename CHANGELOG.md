# Changelog

## 0.4.0 — 2026-09-08

- Clarify that routine, low-stakes replies need quick preparation and self-review, without a
  mandatory written brief or audience-review loop.
- Remove the assumption that a second failed review requires a decision outside the author’s
  authority; ask only when the fix actually needs someone else’s input.
- Exempt cosmetic corrections from another audience review, while rechecking changes to meaning.
- Tell the audience reviewer the terms the brief's knowledge model accepted, instead of restating
  the evidence rules in the reviewer prompt.
- Define low-stakes by cost of failure: a misunderstanding would be cheap to correct in the next
  exchange.
- Add a fourth router question about stakes and order the router's rows, so a routine reply has
  one matching row.
- Reopen audience review as a new first round when a change after a passed review affects meaning.
- Split `comms-prep` and `comms-review` into a short entry point and reference files, so the
  routine path loads only the decision text. `comms-prep` points to `references/brief.md` and
  `references/structure.md`; `comms-review` points to `references/content-checks.md` and
  `references/audience-review.md`.

## 0.3.0 — 2026-09-02

Behavioral rewrite of all three skills. They are shorter, plainer, and test-driven: the previous
candidate failed a controlled retest because review machinery leaked into deliveries, source
meaning drifted in rewrites, and the process was too heavy to follow. Every change below targets
one of those failures.

- Drop the mandatory audit record, reviewer seal, and row-by-row proof that each check was
  applied. The brief, check notes, reviewer prompts and returns, and superseded drafts are working
  state, kept outside the returned workspace. An audit is produced only when it is itself
  requested, as a separate communication.
- Add a pre-delivery check over every file and message about to be returned: it contains the
  requested communication and nothing else.
- Keep the brief's five lines (objective, audience and context, knowledge model, source meaning,
  form factor) and drop the separate P1 to P6 proof table; the brief's own completion list is the
  check.
- Add source-meaning preservation as an explicit check. Before rewriting, list the required
  elements, asks and their order, distinctions, conflicts, explicit exclusions, and requested
  scope; recheck the list after every substantive revision.
- Replace the binary "reader has used the term" rule with an evidence ladder: reader usage, then
  task-provided context, then ordinary role knowledge. Terms with none of these are introduced in
  the reader's words when material, otherwise avoided.
- Add a direct-statement check: use the literal phrase where one exists; keep a metaphor only
  where it carries meaning the literal phrase cannot.
- Review the complete delivery bundle: titles, headings, captions, and the exact chat handoff are
  reviewed together with the body. The handoff names what was delivered and any material limit; it
  does not describe the review, claim a pass that did not happen, or imply implementation when
  only a specification was written.
- Send the fresh audience reviewer only the reader, their situation, their evidenced knowledge,
  the objective, the complete delivery, and the verdict format. The brief and the checks stay with
  the author.
- Replace "loop until pass" with one stop rule: a second failed round ends the loop, with one
  brief refresh allowed when the findings show the brief was wrong, and otherwise an escalation
  with a concrete proposal or a partial delivery that states its limit.
- Scope guard: a missing fact limits only the claim that needs it. Unavailable implementation
  access does not invalidate a completed writing or specification task.
- Use degraded written self-review only when a fresh subagent or delegated agent is unavailable or
  fails to start; record that in working notes and say nothing about review mechanics in the
  delivery.
- Remove the mandatory Live/Non-interactive declaration. Ask or state an assumption only when an
  unresolved question changes the deliverable.
- Move `/comms-prep` to the authoring boundary and reuse the brief across replies in the same
  conversation and objective.
- Add Codex interface metadata for all three skills.

## 0.2.0 — 2026-07-29

- Degradations disclosed where the reader looks: written self-review is named the DEGRADED review form; the audit record opens with the review mode (independent ×N rounds vs degraded self-review + reason) so a weaker pass never masquerades as the skill failing.
- Phase 3 rewritten as six numbered steps with an ESCALATION path (recurrence-in-kind = same rubric row or decision; owner defined per question type; no-reply-channel runs exit BLOCKED with the proposal addressed; three fails of new kinds re-runs the prep) ; stop contract consolidated; prose tightened throughout.
- Furniture planned at prep time: form factor (brief item 5, P6) now includes the artifact's attached text — titles, headings, captions — planned for the reader before drafting; C13 remains the review-side check.
- Attach-last (founder-ruled): the audit record is a side-file during the review loop — reviewers always receive the bare draft — and attaches only at the final PASS, labeled for-auditors-safe-to-skip; a fresh reviewer is required every round.
- C15: every clause earns its place — brevity by selectivity (cut what doesn't change understanding or action), never by compression into fragments.
- Correct rubric totals and ranges to C1–C15, and describe the public package as three skills.
- Translate pack-specific terms at first use and give the skill and README titles reader-effect wording.
- Remove incident-history logs from shipped skills; keep validation evidence on review surfaces.
- Declare linked license texts as required legal terms.
- Bound “term” to labels, abbreviations, coined phrases, specialized jargon, and non-ordinary local uses; ordinary language needs no adoption evidence.
- Define the audience-review briefing as target audience, consumption context, evidenced prior knowledge, objective, and the complete visible draft; required audit text in that draft is not extra briefing context.
- Require a new audience-review sub-agent with no hidden prior-round context for every dispatch-capable round.
- Type the audit as required for the reviewer verifying the pass and supplemental for the primary reader, with subordinate placement.
- Seal the audit with a fixed reviewer-authored block; exclude tool metadata, and reopen review after any later authored change.
- Make unavailable attachment BLOCKED / PARTIAL, requiring real paths only for persisted artifacts and explicit “not persisted” disclosure otherwise.
- Let inspectable brief text in a file, draft body, or delimited current response satisfy P1 entry while durable attachment remains a whole-pass completion condition.
- Treat the mandatory audience-review seal format as response control, outside the `ONLY` limit on audience/context briefing content.
- Review the audit's verifier fitness in Phase 2; Phase 3 remains the primary-audience check that supplemental audit text does not obstruct.
- Expand preparation checks (P1–P6) and communication checks (C1–C15) on first use in the audit before using stable identifiers alone.
- Permit a responsible role or owner in BLOCKED / PARTIAL handoff when the authorized person's identity is unavailable; never invent a name.
- Treat terminal missing-info / assumptions notes as delivered drafts that still pass through the full review gate.
- Interactivity and completion hardening: Addressed/no-reply mode; C14 unreachable-source disclosure; C8 explicit N/A path; C4 fact-framed load-bearing narration; audit-record fallback for deliverables without a review surface.
- P1–P6 unified: comms-prep's completion rubric and comms-review's entry rubric are one rubric stated verbatim in both skills, with divergence declared a pack bug.
- Liberal prep triggering: comms-prep fires for anything written for people — including commit messages, PR titles/descriptions, help text, error messages, page copy — with the brief scaling to the artifact (three lines for a commit message).
- Split the pass into two gate skills: `/comms-prep` (the brief, at authoring time) and `/comms-review` (entry rubric P1–P6 confirming preparation, then the C-rubric and audience loop); `/effective-comms` becomes a router. Both gates carry eval checks and pitfalls.
- The pass starts at authoring time: Phase 1 runs before drafting; review-time invocation is named the degraded path.
- Name the mission: two failure families — claude-ese (output humans can't comprehend unaided) and falsehood (claims that don't survive comparison with the referent); every check serves one.
- New rubric checks: C8 starts with why · C9 one list, one kind · C10 form matches consumption · C11 references are typed · C12 ready-to-hand terms only (new terminology welcome when the first instance is expanded in the reader's own terms in a parenthetical) · C13 furniture is part of the artifact (titles, headings, captions under the rubric) · C14 true against the referent (factual claims derived from inspecting the thing described).
- Reader-model rules: terms the reader hasn't used themselves default to the falsely-assuming cell; audience-reviewer knowledge models are built from evidence of adoption, never author say-so.
- Tighten C4: process history survives only when load-bearing for the reader's decision, reproducibility, or handoff.
- Tighten pass semantics: the Phase 3 loop ends only on a passing audience review (a cut loop voids the pass); a residual-risk note cannot convert a fail; written self-review only when sub-agent dispatch is genuinely impossible.
- Require the audit record attached to the artifact on its review surface, each check with a cited instance — never shipped inside the package.
- Group the rubric into four kinds (Trustworthy · Reader's language · Right content · Shaped for consumption); row numbers stay stable identifiers in addition order.
- Restructure the skill document for mid-task execution (typed run-modes, itemized stop contract and pass-invalidating failures).

## 0.1.0

- Add `/effective-comms` v0 as a standalone Claude Code skill.
- Add plugin metadata for `effective-comms`.
- Add public README, feedback path, and dual Apache-2.0/MIT licensing.

Validation note: the companion validation system remains internal. Public release should summarize validation status without publishing internal fixtures or dogfood traces by default.
