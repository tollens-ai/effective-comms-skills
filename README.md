# Effective Comms Skills

Claude Code skill for making agent-written communication land with its reader.

`/effective-comms` runs a **prepare → review → revise** pass over a report, update, strategy doc, review finding, handoff, or recommendation before it is finalized. It helps agents check the communication objective, model the audience, remove hidden-context assumptions, name internal references in plain English, and make uncertainty/next actions legible.

> **Status: early alpha.** The v0 skill exists and has been dogfooded through [Quality Strategy Skills](https://github.com/tollens-ai/quality-strategy-skills). Expect rough edges. Please report confusing behavior or missed communication failures via [GitHub issues](#feedback).

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

Then run:

```text
/effective-comms
```

If the bare skill name collides with another plugin, use the plugin's namespaced form in Claude Code.

## The pass

Effective Comms has three phases:

1. **Prepare the communications brief** — objective, audience, audience knowledge model, evidence/uncertainty, and form factor.
2. **Review the draft** — apply the rubric to catch known failure modes.
3. **Audience-perspective review** — for non-trivial outputs, re-read from the target reader's perspective or dispatch a fresh reviewer with only the audience brief and draft.

The pass ends with one of:

- a revised user-facing output that passes the rubric;
- a revised output plus explicit residual-risk notes;
- or a missing-info / assumptions note if the brief is too incomplete to finalize responsibly.

## Core checks

The v0 rubric checks for:

- numbered/internal references that lack plain-English meaning;
- hidden scratch/context assumptions;
- rejected ideas retained in current accepted outputs;
- coordinate-before-name references;
- irrelevant agent process-history leakage;
- purpose/audience mismatch;
- buried recommendations or unclear next actions;
- illegible uncertainty.

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

Licensed under either of:

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE)); or
- MIT License ([LICENSE-MIT](LICENSE-MIT));

at your option.
