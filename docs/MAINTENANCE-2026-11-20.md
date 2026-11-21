# Round 16A maintenance review — 2026-11-20

Refs FAIR-bioHeaders/FAIR-bioHeaders-Specification#211.
Repository: `FAIR-bioHeaders/.github`.
Base: `74d082df8103f758961221625a206482e5b56613`.
Initial implementation reviewed: `1d4fac1`. Scan date: 2026-11-20 UTC.
The final head and current hosted checks are recorded on PR #13.

This repository contains organization documentation and its validation workflow;
it has no runtime package, application functions or dependency manifest to audit.
The review covers all seven tracked baseline files and the documentation added
here. It corrects stale draft/release descriptions, distinguishes publication
authority from implementation support, documents setup and human-only merges,
and preserves license and citation provenance. No schema, fixture or release is
changed. Historical plans elsewhere remain dated evidence, not merge permission.

## Security and workflow review

Gitleaks 8.30.1 scanned all baseline refs: 17 commits, 36,419 bytes, zero findings.
That history scan precedes the implementation commit. A separate current-tree
Gitleaks scan covers the added documentation and also found zero matches.
This is a bounded credential-pattern scan, not assurance that no secret exists.
Actionlint 1.7.12 passed the existing workflow. Manual review found pinned action
SHAs, read-only contents permission, disabled persisted checkout credentials,
constant linter arguments, and no pull_request_target or untrusted shell input.
The GitHub token is used by the link checker with read-only workflow permissions.
There is no first-party runtime manifest or application code for a language
package audit. Pinned third-party actions do have upstream dependency graphs;
those transitive graphs were not independently audited here. Pinning alone is
not an advisory check. Action and documentation checks remain applicable.

Link-check limitations are documented in README: accepted HTTP 429 is inconclusive,
email destinations are excluded, and one DOI is checked through Crossref rather
than publisher access. Hosted CI must pass at the final PR head; local network
failures or omitted checks must be reported separately.

## Branch and review handoff

The Round 16 branch is isolated from the existing checkout. Existing branches and
worktrees have been retained because ownership, active use or squash-equivalence
is not established. No force deletion or historical rewrite is authorized by this
cleanup. The PR records exact head, independent reviewer, check results and any
remaining limitations. Only a human may merge it.
