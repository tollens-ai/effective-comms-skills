# Effective Comms Skills — make agent-written communication usable and trustworthy

Claude Code skills for making agent-written communication land with its reader.

The pack runs a **prepare → write → review** pass over a report, update, strategy doc, review finding, handoff, or recommendation — as **two gates, each its own skill**: `/comms-prep` produces the communications brief at authoring time, BEFORE drafting; `/comms-review` gates the draft before delivery, and its entry rubric sends you back to `/comms-prep` if the brief is missing. `/effective-comms` remains as a router that picks the right gate. It targets the two failure families that dominate agent communications: **claude-ese** — output in the agent's own dialect that a human can't comprehend unaided — and **falsehood** — claims that don't survive comparison with the thing they describe. A communication passes only when its reader can understand it without help and trust every claim in it.

> **Status: early alpha.** Expect rough edges. Please report confusing behavior or missed communication failures via [GitHub issues](#feedback).

## What it is for

Use Effective Comms when an agent is about to produce a non-trivial user-facing output, especially:

- reports, updates, or debriefs;
- technical or project strategy documents;
- review findings or audit results;
- handoffs and worker reports;
- recommendations or decision notes.

It is not a prose-polish template. It is a judgment checklist: what is this communication for, who is reading it, what do they already know, what might the agent be falsely assuming they know, and what failure modes need to be checked before the output is done?

## Install

This is a public Claude Code plugin. Install with:

```text
/plugin marketplace add tollens-ai/effective-comms-skills
/plugin install effective-comms@tollens-effective-comms
```

Then run `/comms-prep` before writing, `/comms-review` before delivering — or `/effective-comms` to be routed to the right gate.

If a bare skill name collides with another plugin, use the plugin's namespaced form in Claude Code.

## The pass

Two gates, three phases:

1. **`/comms-prep` (Phase 1)** — the communications brief: objective, audience, audience knowledge model, evidence/uncertainty, form factor. Runs the moment you know the communication will exist; the draft is written from it.
2. **`/comms-review` (Phases 2–3)** — an entry rubric first confirms the brief is satisfied (missing → run `/comms-prep` retroactively, the named degraded path); then the 15-check rubric; then an audience-perspective review by a new reviewer each round, given only the target audience and consumption context, evidenced prior knowledge, objective, and complete visible draft — revised and re-run until the reviewer passes.

The pass ends with one of:

- a revised user-facing output that passes the rubric and audience review;
- a revised output plus explicit, non-blocking residual-risk notes;
- or a missing-info / assumptions note if the brief is too incomplete to finalize responsibly; the note itself goes through the same review.

The artifact carries an audit trace — phases and checks run with cited instances, audience-review verdicts, finding dispositions — attached on its review surface (a report's appendix, a PR's description or comment), never shipped inside a deliverable package. It is required for the reviewer verifying the pass and supplemental for the primary reader: Phase 2 checks its verifier fitness, while Phase 3 checks that it does not obstruct the primary reader. The final reviewer-authored seal block is appended verbatim; tool metadata is excluded, and any later authored change reopens review. If the agent cannot attach the audit, the honest result is blocked/partial, not a pass; nonexistent artifact paths or people are never presented as real.

## Core checks

The rubric is grouped into four kinds of check:

**Trustworthy** — can the reader believe every claim?

- illegible uncertainty;
- factual claims written from the author's narrative instead of derived from the thing described.

**In the reader's language** — can they understand it without stopping?

- coordinate or internal references that lack plain-English meaning;
- jargon that is not ready-to-hand for this reader — including other agents' and tools' vocabulary — or new terms introduced without a first-use expansion in the reader's own words.

**The right content** — is this what this reader needs, and nothing else?

- hidden scratch/context assumptions;
- rejected ideas retained in current accepted outputs;
- process-history leakage that carries no decision, reproducibility, or handoff value;
- purpose/audience mismatch;
- proposals or decision requests that lead with mechanics instead of why.
- padding, restatement, and sentences that exist to sound thorough — length the objective didn't buy.

**Shaped for consumption** — does the form serve how they will actually read it?

- buried recommendations or unclear next actions;
- lists that mix different kinds of information;
- structure or density that does not match how the reader will consume the artifact;
- linked or cited artifacts whose required-versus-supplemental role is unstated;
- unreviewed visible framing (“furniture”) — titles, headings, and captions held to a lower bar than the body.

## Roadmap

Planned follow-ups include:

- multiple-audience staged passes;
- artifact-specific companion skills, such as handoff writing or report polishing, if dogfooding shows they carry reusable judgment;
- more public examples once examples are intentionally selected and reviewed for publication.

## Feedback

The most useful feedback is a concrete example of where `/effective-comms` helped, got in the way, or missed something important:

- **Report a misfire publicly:** open a [GitHub issue](https://github.com/tollens-ai/effective-comms-skills/issues) with what you ran, what it produced, and what you expected instead. Redacted examples are ideal.
- **Share privately:** [join the Tollens mailing list](https://tollens.ai/) and reply through the contact details you receive there.
- **Tell us where it would land:** what workflow or decision the communication was meant to support, who would read it, and what would make it hard to use.
- **Ask for an integration:** if another skill pack or workflow should invoke `/effective-comms`, open an issue naming the output it should gate.

Please do not include private project data, credentials, customer data, or non-public agent scratchpads in public issues.

## License

Choose either of these required legal terms:

- [Apache License, Version 2.0](LICENSE-APACHE); or
- [MIT License](LICENSE-MIT).
