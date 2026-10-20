# Agent instructions

## Repository context

This is the FAIR-bioHeaders organization profile repository. `profile/README.md`
is the public organization landing page. Keep its repository map aligned with
shared publication in FAIR-bioHeaders-Specification, per-type development in
FHR/FHP/FHT-Specification and FHGFF3, active tooling in FAIR-bioHeaders-Tools,
GFF3 feature validation in gff3-validator, and the public website. Do not describe
retired FHT-File-Converter as an active implementation or advertise drafts as
released support. This profile does not adopt schemas or mappings.

Read README, LICENSE, `.markdownlint.json` and `lychee.toml`. For Markdown changes,
run the documented Markdown lint and relevant local/link checks; report network
limits honestly. AGENTS.md-only changes need `git diff --check` and Markdown lint.
Preserve verified citations, third-party notices and published destinations.

## Schema additions and their own development cycle

A new optional field, structured alternative, enum value, constraint, required
field or changed meaning is a schema-contract change, even when motivated by a
UI, exporter, parser fix or documentation task. Identify it explicitly as a
**schema addition** or other contract change in its issue and PR. Supporting an
already adopted field in a consumer is implementation work, not a new field.

Schema additions have their own proposal, review, compatibility, versioning and
release cycle. Keep them separately reviewable from routine fixes, website work,
packaging and dependency updates; link dependent implementation PRs rather than
silently adopting a field downstream. Shared fields/objects and cross-type rules
belong in FAIR-bioHeaders-Specification; type-specific design starts in the owning
development repository and is coordinated into shared publication. Name affected
types, requiredness, semantics, mappings, serializers and conformance fixtures.

During active construction of FHP, FHT and FHGFF3, maintainers may iterate on draft
fields with lighter process and include coordinated schema/implementation work in
one clearly scoped PR. Record the proposal and compatibility impact in that PR;
this flexibility does not make every field adopted or supported. Preserve already
published contracts and cited versions, label draft behavior, and obtain joint
maintainer review before publication. FHR additions retain the separate cycle.
Do not apply draft flexibility to released FHP/FHGFF3 schemas retroactively.

Use the shared specification's `docs/SCHEMA-VERSIONS.md` and
`schemas/versions.json`: contract versions are per type, distinct from repository
release tags and biological resource versions. Additive changes that preserve all
valid values and meanings qualify for a minor increment; invalidating records or
changing meanings requires a major increment. Do not assign a new version merely
for implementing an existing contract. Never rewrite immutable releases, fixed
schema aliases or existing file-bound headers as incidental cleanup. Header edits
require checksum recomputation and may affect downstream parent links.

Proposals are not adopted contracts: FAIR-bioHeaders-Specification#139 / draft
PR #140 (structured vouchers) and profiles still under review in that repository
(#56) remain proposals until adopted. Implemented subsets do not establish full
profile or header-family support. The mapping page in fair-bioheaders.github.io#29
depends on approved profiles.
