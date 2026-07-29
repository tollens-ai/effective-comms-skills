# Changelog

## 0.2.0 — unreleased

- Split the pass into two gate skills: `/comms-prep` (the brief, at authoring time) and `/comms-review` (entry rubric P1–P6 confirming preparation, then the C-rubric and audience loop); `/effective-comms` becomes a router. Both gates carry eval checks, pitfalls, and dogfood logs.
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

Validation note: the companion validation system remains internal, following the QSS model. Public release should summarize validation status without publishing internal fixtures or dogfood traces by default.
