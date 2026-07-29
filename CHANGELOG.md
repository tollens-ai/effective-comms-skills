# Changelog

## 0.2.0 — unreleased

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
