# Contributing

Thanks for helping improve Effective Comms Skills.

## File feedback

Use GitHub issues for public feedback:

- **Missed communication failure:** include a minimal redacted example of the output and what the reader needed instead.
- **Wrong process shape:** describe the output type, audience, and what the skill asked for that felt unnecessary or missing.
- **Integration request:** name the skill pack or workflow that should invoke `/effective-comms` and the output it should gate.

Do not include private project data, credentials, customer data, or non-public agent scratchpads in public issues.

## Preserve the skills' intent

These skills are carefully human-written. Their purpose is to help a communication achieve its
objective for its reader; preparation, writing guidance, checks and review support that purpose.
Preserve the goals, orientation, invocation guidance and substantive sections when maintaining them.

Astra-proofing means making narrowly targeted changes to instructions associated with a specific
reported or observed Astra confusion. Identify that confusion and explain why each change addresses
it. Preserve the original wording when moving or reordering chunks of meaning; reword only for a
concrete reason. Shortening, restyling or reorganizing the skills requires its own justification
and scope, rather than being an assumed part of model adaptation.

## Pull request checklist

Before opening a PR:

- [ ] Public copy contains no private paths, internal agent notes, credentials, or customer data.
- [ ] Skill instructions remain product-neutral unless the change is explicitly an integration example.
- [ ] New behavior is reflected in `README.md` and `CHANGELOG.md` when user-facing.
- [ ] Validation-sensitive changes have corresponding internal validation coverage or a clear follow-up note.
- [ ] License files remain intact.
