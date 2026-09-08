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

Effective Comms is a pack of three skills that help agents write for their reader, preserve source
meaning, and catch misleading or confusing content before delivery. It fixes the content of a
communication, not its style, and it works alongside any house style you already apply.

> **Status: alpha.** Expect rough edges. Please report confusing behavior or missed communication
> failures through [GitHub issues](#feedback).

## The three skills

| Skill | When | What it does |
|---|---|---|
| `/comms-prep` | Immediately before drafting, once the substance is known | Uses a quick check for routine, low-stakes replies; otherwise writes a short brief: the objective, the audience and context, a knowledge model of what they know and what the agent may be falsely assuming, the source meaning that must be preserved, the form factor, and the style conventions that apply. |
| `/comms-review` | When a draft is complete and the brief called for review | Checks the draft against the brief and a set of content checks, then puts it in front of a fresh reader who knows only what the real reader knows. |
| `/effective-comms` | When you want the pack to choose | Decides whether preparation, review, or nothing is due, and does it. |

The brief and the review notes are working state. They stay with the agent and never appear in
the delivered communication or the returned files.

## Writing for the reader

For routine, low-stakes replies, a quick check of the objective, audience and source meaning,
followed by self-review, is enough. Other communications follow the guidance below.

Do the underlying work first. When the substance is ready and drafting is about to
start, the agent writes a short brief at a scale that fits the artifact: the objective and what
should change for the reader; the audience, their attention budget, and their expectations; a
knowledge model of what they need, want, and already know, and what the agent might be falsely
assuming they know; the source meaning that must be preserved in a rewrite; the form factor,
including where uncertainty goes and whether a full review is worth running; and the house style
conventions and skills that apply. A small artifact may
need four lines answered in seconds. A document needs a page. The brief is reused across replies
while the conversation and objective stay the same.

The agent drafts from the brief, saying what it means in literal phrases.

The agent reads the whole delivery as the reader will see it, including titles,
headings, and the chat message that accompanies a file, and fixes what it can see against these
checks:

- *Trustworthy:* every claim about a source comes from inspecting that source now; uncertainty
  is stated where it limits a claim.
- *In the reader's language:* names lead and coordinates support; terms are ones the reader can
  use or are introduced in their words; literal phrases are used where they exist.
- *The right content:* self-standing, no rejected ideas, no process history, fit for the
  objective, opening with the problem when there is a proposal, every clause necessary.
- *Shaped for consumption:* the next action is easy to find, each list holds one kind of thing,
  structure matches how the reader will read, references are typed, and titles describe the
  effect for the reader.

Then a fresh subagent, told only who the reader is, what they know, what the communication is
for, and the complete delivery, answers one question: does this reader achieve the objective? A
failed round is fixed and reviewed again by a new reader. A second failure prompts reassessment
and one final round; the author asks for input only if a fix actually requires it. Cosmetic
corrections need proofreading, while changes to meaning reopen review. Before returning, the agent
checks every file and message it is about to return and removes anything that is not the requested communication.

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
[Claude Code's plugin guide](https://code.claude.com/docs/en/plugins). The bare forms
`/comms-prep` and `/comms-review` also work, and the skills refer to each other that way; if
another installed skill uses the same bare name, use the namespaced form.

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
