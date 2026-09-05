# Effective Comms Skills

Skills that help agent-written communication land with its reader.

When an agent writes a report, README, tutorial, or PR description, three things go wrong more
than any others:

- **Wrong reader or objective.** The text covers what the agent did and skips what the reader
  needs to understand or decide.
- **The agent's private dialect.** Coined labels, bare ticket numbers and paths, process
  narration, task-shaped titles, and metaphors that stand in for plain statements.
- **Falsehood.** Claims inferred from the plan or from memory instead of from the thing being
  described, and source meaning that drifts in a rewrite: a dropped ask, a reordered priority, a
  contradiction silently resolved.

Effective Comms is a pack of three Claude Code skills that add a **prepare, write, review** pass
scaled to the communication's complexity and consequences. It fixes the content of a communication,
not its style, and it works alongside any house style you already apply.

> **Status: alpha.** Expect rough edges. Please report confusing behavior or missed communication
> failures through [GitHub issues](#feedback).

## The three skills

| Skill | When | What it does |
|---|---|---|
| `/comms-prep` | Immediately before drafting, once the substance is known | Checks the audience and source meaning for routine replies; writes or reuses a brief for substantial artifacts. Chooses the review depth. |
| `/comms-review` | When requested or preparation calls for it | Checks content against the audience, objective, and sources. Adds a fresh reader for long, public, or consequential writing. |
| `/effective-comms` | When you want the pack to choose | Decides whether preparation, review, or nothing is due, and does it. |

The brief and the review notes are working state. They stay with the agent and never appear in
the delivered communication or the returned files.

## How a pass works

**Prepare.** Do the underlying work first. For a routine reply, the agent checks who is reading,
what they need to understand or do, what it might falsely assume they know, and what source meaning
must survive. It uses those answers directly; a written brief is unnecessary. Detailed briefing,
structure-planning, and review guides are loaded only for the tasks that need them.

For a substantial artifact or consequential message, the agent writes or reuses a short brief:
objective; audience and context; what the reader needs, wants, and knows, including possible false
assumptions; source meaning to preserve; form and structure; and applicable house style. Related
answers can be combined. Long documents get a structure plan before prose. A short approval
request may need more care than a long informal reply. Preparation is reused while it still fits.

**Write.** The agent drafts from that preparation, saying what it means in literal phrases.

**Review.** Every draft gets a self-review for reader fit, source fidelity, and applicable style.
For routine replies, that normally completes the pass. The detailed `/comms-review` checks cover
the whole delivery, including titles, headings, and the chat message accompanying a file:

- *Trustworthy:* every claim about a source comes from inspecting that source now; uncertainty
  is stated where it limits a claim.
- *In the reader's language:* names lead and coordinates support; terms are ones the reader can
  use or are introduced in their words; literal phrases are used where they exist.
- *The right content:* self-standing, no rejected ideas, no process history, fit for the
  objective, opening with the problem when there is a proposal, every clause necessary.
- *Shaped for consumption:* the next action is easy to find, each list holds one kind of thing,
  structure matches how the reader will read, references are typed, and titles describe the
  effect for the reader.

For long, public, or consequential writing, a fresh agent also reads the complete delivery with
only the objective and supported audience context. Reader usage, task context, and ordinary
knowledge for an evidenced role can support that context; local jargon needs its own explanation.
The reviewer tests whether the reader can understand and use the communication. The author remains
responsible for verifying facts against sources. If independent review is unavailable or not
permitted, a careful self-review from the audience's perspective is the fallback.

The author fixes writing defects within the requested scope. A missing fact or choice that needs
someone else's input can prompt a concrete question; a second failed review does not itself
require approval. Repeated reviews that make no progress prompt a reassessment of the reader's
needs or a specific statement of the unresolved limit. Ordinary wording choices stay with the
author.

Later edits get checks proportionate to their effect. A typo needs proofreading; a changed claim,
number, recommendation, or structure needs the affected content and source checks. Independent
review repeats when the change could materially alter the reader's understanding or action and
the communication warrants that depth. A one-character change to a number or negation can matter.
Working notes stay outside the delivered files and messages.

## Install

Effective Comms is a public Claude Code plugin:

```text
/plugin marketplace add tollens-ai/effective-comms-skills
/plugin install effective-comms@tollens-effective-comms
```

In Claude Code, use the router with your writing request, for example:

```text
/effective-comms:effective-comms Draft a customer update from these incident notes: …
```

The router chooses preparation and review at the right depth. To choose a step yourself, use
`/effective-comms:comms-prep` before drafting or `/effective-comms:comms-review` with an existing
draft. These are the plugin's fully namespaced commands, as described in
[Claude Code's plugin guide](https://code.claude.com/docs/en/plugins).

**Codex CLI or IDE extension:** ask the built-in installer to install the three skill directories:

```text
$skill-installer Install skills/comms-prep, skills/comms-review, and skills/effective-comms from the GitHub repository tollens-ai/effective-comms-skills.
```

Then include `$effective-comms` with your writing request, or choose `$comms-prep` before drafting
and `$comms-review` for a draft. Codex detects newly installed skills automatically; restart if they
do not appear. See [Codex's skill guide](https://learn.chatgpt.com/docs/build-skills) for local
installation and discovery details.

## Roadmap

- Staged passes for communications with more than one audience.
- Companion skills for specific artifact types, if dogfooding shows they carry reusable
  judgement.
- More public examples once they have been selected and reviewed for publication.

## Feedback

The most useful feedback is a concrete example of where Effective Comms helped, got in the way,
or missed something important.

- **Report a misfire:** open a
  [GitHub issue](https://github.com/tollens-ai/effective-comms-skills/issues) with what you ran,
  what it produced, and what you expected instead. Redacted examples are ideal.
- **Share privately:** [join the Tollens mailing list](https://tollens.ai/) and reply through the
  contact details you receive there.
- **Ask for an integration:** open an issue naming the output another skill pack or workflow
  should pass through Effective Comms.

Do not include private project data, credentials, customer data, or non-public agent scratchpads
in public issues.

## License

Choose either of these required legal terms:

- [Apache License, Version 2.0](LICENSE-APACHE); or
- [MIT License](LICENSE-MIT).
