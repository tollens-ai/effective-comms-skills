# Effective Comms Skills — make agent-written communication usable and trustworthy

Skills for helping agent-written communication land with its reader.

Effective Comms adds a **prepare → write → review** pass to human-facing communication. It has
two gate skills used at different points.

`/comms-prep` prepares the communication immediately before drafting; `/comms-review` reviews the
draft before delivery. `/effective-comms` is a router skill that chooses the next action, including
when no communication gate is due.

> **Status: early alpha.** Expect rough edges. Please report confusing behavior or missed
> communication failures through [GitHub issues](#feedback).

## Why it exists

The pack targets three failure families that dominate agent communications:

- **Missing the audience or objective:** sharing information the audience doesn't care about while
  omitting what they really want or need to know.
- **Claude-ese/Neuralese:** writing in the agent's own dialect — coined labels, bare coordinates,
  process narration, task-shaped titles, and other terms the reader cannot understand unaided.
- **Falsehood:** delivering inferred, guessed, or misunderstood claims that do not match the real
  thing being described.

These are defects in the communication's contents, not merely its style. Effective Comms is not a
prose-polish template, and it does not replace any house style conventions that also apply.

## What it is for

Think about `/comms-prep` any time an agent is writing something for people, including:

- reports, updates, findings, and debriefs;
- recommendations, decision notes, and strategy documents;
- READMEs, tutorials, documentation, and website copy;
- PR messages, error messages, titles, headings, captions, and other visible framing;
- handoffs and worker reports.

Do the underlying work first. Preparation begins at the **authoring boundary**, once the substance
is known and immediately before drafting the communication. A one-line acknowledgement or direct
yes/no answer with no audience to model can be written without a communication gate.

## The workflow

### 1. Prepare with `/comms-prep`

Write a brief covering:

- the objective and what should change for the reader;
- the audience, context, expectations, and attention budget;
- what the audience needs, doesn't need, wants, doesn't want, already knows, and might falsely be
  assumed to know;
- the right form, including the purpose of any titles, headings, captions, labels, or accompanying
  notes.

Scale the brief to the artifact. A small communication may need four lines answered in seconds. A
multi-section or multi-document communication gets a structure plan; a long document gets that
plan reviewed against its objective and audience before drafting and before structural revision.

Generally reuse an adequate brief while the conversation and objective remain the same. Refresh it
when something material changes. In a Live session, ask about gaps; in a Non-interactive run, record
the ambiguity and escalate if it prevents a trustworthy communication.

### 2. Write from the brief

The brief is an artifact, not a thought. Keep it with the draft so it can become the reviewer's
briefing.

During preparation, decide whether the communication's objective, audience, and cost of failure
justify a full review. When they do, the brief tells the drafting agent to invoke `/comms-review`
once the draft is complete. A few review rounds generally cost less than repeated back-and-forth
with a confused reader, and far less than misleading a wide audience.

### 3. When justified, review with `/comms-review`

The review proceeds through three separately gated phases:

1. **Brief verification:** locate the brief and verify it against the same entry rubric as
   `/comms-prep`. If it is missing or inadequate, prepare it retroactively and record that degraded
   path.
2. **Rubric review:** apply all 15 content checks, cite concrete instances, revise failures, and
   re-check affected rows.
3. **Audience review:** ask whether the intended reader, knowing only what the evidence says they
   know, can achieve the communication's objective. Use a fresh independent reviewer when one is
   available; a written self-review is the named degraded fallback.

Failed audience reviews return to the rubric and then run again. Findings that remain unresolved
across multiple rounds, or decisions the author does not own, are escalated with a concrete
proposal instead of being polished in a loop. After a pass, finalization has its own gate for
attaching the audit record and reviewer-authored seal.

## Core review checks

The 15 checks are grouped by the question they answer.

**Trustworthy — can the reader believe every claim?**

- Is uncertainty legible and placed appropriately?
- Was every falsifiable claim checked against the source being described?

**In the reader's language — can they understand it without stopping?**

- Do names lead and coordinates support?
- Are unfamiliar or context-specific terms introduced in language the reader can use?

**The right content — is this what the reader needs, and nothing else?**

- Does the artifact avoid hidden author context, rejected ideas, and irrelevant process history?
- Does it fit the audience and objective, start with why when there is a proposal or decision, and
  make every clause earn its place?

**Shaped for consumption — does the form serve how the reader will actually read it?**

- Are recommendations and next actions easy to find?
- Do lists and sections contain one kind of thing?
- Do structure and density match the way the artifact will be consumed?
- Are references identified as required reading or supplemental material?
- Do titles, headings, captions, labels, and other visible framing meet the same standard as the
  body?

## Install

This repository is packaged as a public Claude Code plugin:

```text
/plugin marketplace add tollens-ai/effective-comms-skills
/plugin install effective-comms@tollens-effective-comms
```

Then invoke `/comms-prep` at the authoring boundary and, when the brief says a full review is
justified, `/comms-review` before delivery. Use `/effective-comms` when you want the pack to choose
the next action. If a bare skill name collides with another plugin, use the plugin's namespaced form
in Claude Code.

## Review trace

`/comms-review` keeps an audit trace of the review mode and any degradation, the phases and checks
run, cited instances, audience-review findings, dispositions, and escalations. During review this is
a side file so the audience reviewer sees only the bare draft. On a final pass, it is attached on a
review surface for auditors and labelled safe for the primary reader to skip.

If the agent cannot complete or attach the review, the honest result is **BLOCKED / PARTIAL**, not a
pass. It never presents nonexistent artifact paths or people as real.

## Roadmap

Planned follow-ups include:

- multiple-audience staged passes;
- artifact-specific companion skills if dogfooding shows they carry reusable judgement;
- more public examples once they have been intentionally selected and reviewed for publication.

## Feedback

The most useful feedback is a concrete example of where Effective Comms helped, got in the way, or
missed something important:

- **Report a misfire publicly:** open a
  [GitHub issue](https://github.com/tollens-ai/effective-comms-skills/issues) with what you ran,
  what it produced, and what you expected instead. Redacted examples are ideal.
- **Share privately:** [join the Tollens mailing list](https://tollens.ai/) and reply through the
  contact details you receive there.
- **Tell us where it would land:** name the workflow or decision the communication was meant to
  support, who would read it, and what would make it hard to use.
- **Ask for an integration:** open an issue naming the output another skill pack or workflow should
  gate with Effective Comms.

Do not include private project data, credentials, customer data, or non-public agent scratchpads in
public issues.

## License

Choose either of these required legal terms:

- [Apache License, Version 2.0](LICENSE-APACHE); or
- [MIT License](LICENSE-MIT).
