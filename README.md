# .github

This repository maintains the FAIR bioHeaders GitHub organization profile.
Edit [profile/README.md](profile/README.md) to update the introduction displayed
at [github.com/FAIR-bioHeaders](https://github.com/FAIR-bioHeaders).

## Documentation checks

Pull requests and pushes to `main` run Markdown linting and link checking.
Links are also checked every Monday and can be checked manually from the
**Documentation checks** workflow in GitHub Actions.

Markdown rules are configured in `.markdownlint.json`. Line length is unrestricted
to allow readable links and tables. To run the same linter locally:

```bash
npx markdownlint-cli2@0.23.2 '**/*.md'
```

With [Lychee](https://github.com/lycheeverse/lychee) installed, run:

```bash
lychee --config lychee.toml --no-progress './**/*.md'
```

`lychee.toml` checks local and web links, excludes email verification, and retries
failed requests with limited concurrency. HTTP 429 responses are accepted as
inconclusive rate limits; they do not prove that a link works. Other failures
fail the check. Link results appear in the workflow's job summary.

The FHR paper's DOI is checked through its Crossref metadata record because the
publisher blocks automated requests. This verifies the DOI record rather than
access to the publisher's article page; other DOI links are checked normally.

## Licensing

[![License: MPL-2.0](https://img.shields.io/badge/License-MPL--2.0-blue.svg)](LICENSE)

FAIR BioHeaders contributions use [MPL-2.0](LICENSE), subject to the scope and preserved permissions stated there.
