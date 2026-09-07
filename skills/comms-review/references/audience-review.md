# Independent audience review

It is very hard to self-review for some of the content checks consistently, because you already have
in your head what the audience doesn't know. Therefore it is important to have an independent agent
simulating the reader's perspective review the communication.

This tests comprehension and usefulness; factual verification remains the author's
[content review](content-checks.md). A readability verdict does not establish source accuracy.

Use an available, permitted subagent or delegated-agent capability. If it is absent, prohibited,
or fails to start, use a careful audience-perspective self-review as the fallback: read the whole
delivery against what the reader knows and needs, and record material findings in working notes.
Do not treat missing review capability as missing authority to finish the communication.

Each round uses a FRESH agent, new each round, with no memory of earlier rounds. The reviewer's
prompt contains exactly these things and nothing else:

- the target reader and their situation, including attention budget;
- what the reader knows and the evidence for it, including reasonable role or task-context
  assumptions and their limits from prep;
- the objective;
- the complete delivery as the reader will see it, including the chat handoff;
- the question and answer format below.

Never send the rubric, the brief, working notes, or unevidenced knowledge claims.
The reviewer answers one question — **does this audience, with the stated knowledge and its limits, succeed at the
objective?** — and FAILS on any of: left confused, lost, or frustrated · unclear what a term or
number refers to · unclear why something is relevant · unclear what to do or conclude · any
ambiguity blocking understanding or action. It ends its response with reviewer-authored text in
this form:

```text
Verdict: <PASS or FAIL>
Blocking findings: <none, or a concise list>
```

Use findings as evidence about the reader's experience. Fix concrete problems and correct a
mistaken audience assumption rather than adding explanations solely to satisfy a reviewer.

- **No material reader problem remains.** Finalize after confirming source fidelity.
- **A writing defect is within your authority.** Fix it and recheck source meaning. Use a fresh
  reader again when the fix materially changes the reader's understanding or action.
- **A material fact or choice needs someone else's input.** Check available sources and existing
  authorization first. Ask the responsible person with a concrete proposal only when that input
  is needed to finish honestly; continue unaffected work. The number of failed reviews does not
  create an approval requirement.
- **Reviews repeat without progress.** Stop repeating the same review. Revisit the objective,
  audience assumptions, and disputed finding; change the approach if you can resolve the cause.
  If a material problem remains unresolved, deliver the useful portion with its specific limit
  and any decision needed. Do not represent an unresolved failure as a pass.
