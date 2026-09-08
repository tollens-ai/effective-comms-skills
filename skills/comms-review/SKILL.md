---
name: comms-review
description: >-
  Review a drafted communication before delivery to humans. Use when writing human-facing
  communications such as documents, reports, website copy, and READMEs, once a draft is complete,
  at review time.
---

# Comms Review — make the draft ready to deliver

The goal of communication is to make yourself understood by your audience so that you can achieve
your goals together. A communication that fails to serve this purpose is a waste of time, effort
and tokens for both parties. It is therefore worth the effort to ensure that a communication will
land, by reviewing it to the best of your ability, and repeatedly fixing any issues you can find,
such that there are no more issues that you can discover before sending it. This skill gives
detailed instructions about how to do this to best mitigate common failure modes.

This skill is aimed at fixing defects in the *contents* of communications. It is not primarily
focused on changing or improving style. It also does not override any house style conventions — if
they exist, you must apply both these content rubrics and house style conventions when reviewing.

**Above all, do your best to make the communication achieve its objective. The following are all
rubrics intended to help you in this goal, not ends in themselves.**

Review notes, reviewer prompts and returns, and superseded drafts are working state. Keep them in
your own scratch space or in context, never in the workspace or files you will return to the
reader. The current draft is the artifact under review; revise it in place.

For routine, low-stakes replies, the quick preparation and self-review in `/comms-prep` is enough.
For a cosmetic correction to an already reviewed communication, proofread the change; a new brief
or audience review is unnecessary. Judge by effect on meaning, not edit size: a changed number or
negation is not cosmetic. Otherwise, follow the phases below.

## Phase 1 — Pick up the prep, or do it now

The review relies on there being a brief about the communication's objective and audience. The
companion skill `/comms-prep` writes this brief. In this phase, you will look for an existing brief
and check whether it is adequate. If an adequate brief doesn't exist, you will have to make a call
to `/comms-prep` to prepare it now, from the draft's intended purpose. The brief tells you the
objective, the audience and their context, the terms the reader can use, key points about the
source meaning, the form factor and structure draft, and the style conventions and skills that
apply.

## Phase 2 — Review against the rubric

In this phase, you will do a manual self review against the criteria below.

Run **every** check below. For each, look for concrete instances in the draft. If it has no
applicable subject in the draft, or satisfying it would contradict the communication objective or
factual information, say so in your notes and move on. If a check finds issues, revise inline if
it is within your authority and knowledge. Don't make things up just to fix issues or change the
meaning; it's better to leave the draft as it is and note and escalate an issue. If you revise the
communication, apply the checks again. Note two things as you go: changes you made, and issues
you could not resolve.

**Every part of the communication is under review.** Its title, subject line, headings, bylines,
captions, annotations, link text, any metadata the reader sees, and the exact chat handoff that
will accompany it are reviewed text, held to every check below exactly as the main body is. If the
title is bad, the audience might not even read the rest.

### Source meaning

Go through the brief's list of source meaning that must be preserved. Confirm each item is in
the draft or visibly dispositioned. There's no point having a communication that reads well if an
ask was dropped, a priority reordered, a distinction lost, a contradiction silently resolved, an
exclusion ignored, or the scope changed! *Redo this check after every substantive revision* to
avoid errors creeping in.

**Trustworthy** — *can the reader believe every claim?*

| # | Check | Catches |
|---|---|---|
| C14 | **True against the referent (the source being described).** Every factual claim about a source (what it is, contains, counts, says) comes from inspecting that source now, not from memory or plan. Anything the reader could falsify by opening a source is checked. | Counts that do not match; a PR described from its intent rather than its diff. |
| C7 | **Uncertainty is legible.** Findings, assumptions, guesses, and open decisions are distinguished, and each sits where it limits a claim. | Uncertainty hidden, overstated, or piled at the end. |

**In the reader's language** — *can they understand it without stopping?*

| # | Check | Catches |
|---|---|---|
| C1 | **Names before coordinates.** Every section, item, ticket, path, or ID is named in plain words before or beside its coordinate. | "Item 2 fails here.", "According to C-1A" |
| C12 | **Use only terms the reader can use without friction; introduce the rest properly.** Every term is one we are confident the reader uses, or it is defined in their terms at first use. New terms that help are welcome once introduced. | A worker's jargon passed through as if shared; a term the reader must stop and decode. |
| C16 | **Direct statement.** Metaphors are used selectively and only where they carry meaning the literal phrase cannot and help accomplish the objective. | "A dial worth turning" for "a parameter worth varying"; "earns its keep" for "still matters"; flourish that displays the writer and makes the reader work to recover the idea. |

**The right content** — *is this what this reader needs — and nothing else?*

| # | Check | Catches |
|---|---|---|
| C2 | **No hidden author context.** Nothing relies on context only an author had: working notes, earlier drafts, prior conversation. | "As discussed" with no discussion in view. |
| C3 | **No retained rejected ideas.** Rejected ideas are absent unless documenting provenance is part of the objective. | Options kept with rejection notes. |
| C4 | **No process-history leakage.** Process history is absent unless it is important to the objective or audience. Provenance is stated as a fact about the thing ("verified against the repo"), not the author's activity. | Tool narration, retries, "I went and checked.", "This does not contain (irrelevant thing)" |
| C5 | **Purpose/audience fit.** Content fits the objective and reader. | Stream of consciousness writing, text for the convenience of the author. |
| C8 | **Starts with why.** Proposals and decision requests open with the problem and what changes if accepted, in the reader's terms. Purely informational pieces skip this. | Mechanisms and details introduced without the audience understanding why they matter. |
| C15 | **Every clause is necessary.** Brevity comes from cutting what does not change understanding or action. | The same point in intro, body, and summary. Sentences-for-decoration that are irrelevant to the objective. |

**Shaped for consumption** — *does the form serve how they will actually read it?*

| # | Check | Catches |
|---|---|---|
| C6 | **Recommendation not buried.** The recommendation and next action are explicit and easy to find. | Reader must derive "so what?" |
| C9 | **One list, one kind.** Each list holds one kind of thing; mixed kinds are split into typed groups. | Decisions, FYIs, and defects in one list. |
| C10 | **Form matches consumption.** Structure and density match consumption: summary before detail, typed lists for parallel content, one idea per block or bullet. | A paragraph encoding a table. |
| C11 | **References are typed.** Each reference is declared required reading with a working link, or stands as supplemental with nothing depending on it. | A required "see X" the reader cannot open. |
| C13 | **Visible framing is part of the artifact.** Titles, headings, captions, and labels describe the artifact's effect for the reader, not the author's task. | A precise body under a task-shaped title. |

## Phase 3 — Audience review

It is very hard to self-review for some of the issues above consistently, because you already have
in your head what the audience doesn't know. Therefore it is important to have an independent agent
simulating the reader's perspective review the communication.

First, determine whether subagents or delegated agents are available: inspect the offered
capability or tool surface, or attempt to create a fresh reviewer. If the capability is absent or
the attempt fails, run a written self-review as the degraded form: drop the author frame, read
carefully line by line and review it against the brief's described audience perspective, and write
the findings down. A same-frame skim does not count. This is not as effective as independent
review but is better than nothing.

Each round uses a FRESH agent, new each round, with no memory of earlier rounds. The reviewer's
prompt contains exactly these things and nothing else:

- the target reader and their situation, including attention budget;
- what the reader knows, limited to what the brief's evidence supports (reader usage is strong
  evidence; task context or ordinary knowledge for the reader's role can also support familiarity,
  as in `/comms-prep`, but neither guarantees it);
- the objective;
- the complete delivery as the reader will see it, including the chat handoff;
- the question and answer format below.

Never send the rubric, the brief, working notes, or unevidenced knowledge claims. The reviewer
answers one question — **does this audience, knowing only the evidenced knowledge, succeed at the
objective?** — and FAILS on any of: left confused, lost, or frustrated · unclear what a term or
number refers to · unclear why something is relevant · unclear what to do or conclude · any
ambiguity blocking understanding or action. It ends its response with reviewer-authored text in
this form:

```text
Verdict: <PASS or FAIL>
Blocking findings: <none, or a concise list>
```

Then take exactly one of these options:

- **PASS.** Finalize the communication as described below.
- **First FAIL.** Fold the findings through Phase 2, redo the source-meaning check, and run a NEW
  round.
- **Second FAIL.** Reassess why the review is not converging. If the findings show the brief itself
  was wrong about the reader or objective, rerun `/comms-prep` folding everything found so far.
  Fix issues within your authority, revise, and allow one final round. A review count does not
  create a need for approval. If a fix actually needs information or a decision you do not own,
  bring a concrete proposal to the person who can supply it. **Who decides:** content, scope, and
  facts → the artifact's requestor/reader; the rubric or this process itself → the standard's
  owner. Wait only for that required input; if it is unavailable or the final round still fails,
  deliver as partial.

A partial delivery is the last reviewed version plus one plain statement of the unresolved limit
in the handoff. That statement is the only text added after review.

## After Phase 3 — finalize

Deliver only the communication selected by the final review. After the final PASS, proofread
cosmetic corrections locally. Changes that could affect the reader's understanding or action
require the affected Phase 2 checks, including source meaning, and reopen Phase 3.

Before returning, look at every file and message you are about to return. It contains the
requested communication and nothing else: no brief, no rubric notes, no reviewer prompts or
returns, no revision history, no audit text. If audit, provenance, or decision history is
explicitly part of the user's objective, produce it as a separate communication with its own
audience.

The chat handoff says what was delivered and any material limit. It does not describe the review
that produced it, claim a pass that did not happen, or imply that something was built when only a
specification was written.

## Maintainer reference

To extend the standard, append a new failure mode and rubric row. Change an existing row only with
the standard owner's decision. Do not redesign the standard through an extension.
