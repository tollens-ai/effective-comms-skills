# Phase 3 — Audience review

First, determine whether subagents or delegated agents are available: inspect the offered
capability or tool surface, or attempt to create a fresh reviewer. If the capability is absent or
the attempt fails, run a written self-review as the degraded form: drop the author frame, read
carefully line by line and review it against the brief's described audience perspective, and write
the findings down. A same-frame skim does not count. This is not as effective as independent
review but is better than nothing.

Each round uses a FRESH agent, new each round, with no memory of earlier rounds. The reviewer's
prompt contains exactly these things and nothing else:

- the target reader and their situation, including attention budget;
- what the reader knows, limited to what the brief's evidence supports: the terms its knowledge
  model found the reader can use. The brief has already weighed reader usage, task context, and
  role knowledge; do not add terms here that it did not accept;
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

- **PASS.** Finalize the communication as described in the skill's *After Phase 3 — finalize*
  section.
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
