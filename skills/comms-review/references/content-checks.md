# Content review

Consider each check below and look for concrete defects in the draft. Skip checks with no
applicable subject; no row-by-row record is required. Fix supported issues within your authority,
preserving source meaning. Keep only useful working notes: material changes and unresolved issues.
After a revision, recheck the affected criteria and source meaning rather than restarting every
check for a cosmetic change.

**Every part of the communication is under review.** Its title, subject line, headings, bylines,
captions, annotations, link text, any metadata the reader sees, and the exact chat handoff that
will accompany it are reviewed text, held to every check below exactly as the main body is. If the
title is bad, the audience might not even read the rest.

### Source meaning

Check the source meaning identified during preparation against the sources and draft. For a
written brief, confirm each listed item is in the draft or visibly dispositioned. A readable draft
still fails if an ask was dropped, a priority reordered, a distinction lost, a contradiction silently resolved, an
exclusion ignored, or the scope changed. Recheck source meaning after every substantive revision.

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
