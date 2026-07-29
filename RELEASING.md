# Releasing this plugin

1. **Branch final:** `claude plugin validate .` exits 0; the changelog's top section
   describes the release delta (no process narration); the skill docs have passed a
   cold-agent execution review.
2. **Neutrality/privacy sweep:** a full re-read of every consumer-visible file for private
   references, internal doctrine, and incident residue.
3. **Date the changelog** section and merge the release PR into `main`.
4. **Tag** `vX.Y.Z` matching `.claude-plugin/plugin.json`.
5. **Fresh-install verification** in a clean environment:
   `/plugin marketplace add tollens-ai/effective-comms-skills` →
   `/plugin install effective-comms@tollens-effective-comms` → the pack's skills are listed
   and loadable.
6. **Existing installs** pick the release up with:
   `claude plugin marketplace update tollens-effective-comms && claude plugin update effective-comms@tollens-effective-comms`
   (restart required).
