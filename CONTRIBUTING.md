# Contributing

Open Family TV is in the feasibility stage. Contributions that answer an open
question with clear evidence are especially useful.

## Start with a focused proposal

Read the [plan](docs/plan.md), [architecture](docs/architecture.md), and
[reuse assessment](docs/filtertube-reuse.md). Open an issue describing the problem,
the proposed change, and how you would evaluate it. Small documentation corrections
can go directly into a pull request.

There are no application build or test commands yet. Add instructions alongside
the first implementation, and distinguish emulator checks from physical-device
results.

## Useful early work

- Supported playback and remote-navigation experiments on Fire TV.
- Small, independently testable extraction of suitable FilterTube helpers.
- Public-content examples that reveal mistakes in proposed preference categories.
- A TV interface that supports broad discovery and clear parent settings.
- Parent research about current workarounds and maintenance effort.

## Evidence and privacy

Use public video links and synthetic profiles. For content examples, state the
relevant preference, expected decision, evidence basis, and uncertainty. Distinguish
reviewing metadata from watching the actual content.

Do not include children's names or viewing histories, credentials, cookies,
authentication URLs, private screenshots, household device identifiers, IP
addresses, or network captures. Redact diagnostics before sharing them. The local
`evidence/`, `private/`, and `local-research/` directories are ignored by Git.

## Pull requests

Explain what changes for the user and why. Include verification appropriate to the
change and disclose known limitations. Runtime changes need meaningful tests for
the affected behaviour; documentation-only changes need link and consistency checks.
Do not claim compatibility, safety, classifier accuracy, or upstream endorsement
without supporting evidence.

For copied third-party code, preserve notices and record the source commit,
paths, modifications, and applicable licences. No contributor licence agreement is
currently required. Contributions are offered under this repository's MIT licence,
subject to the rights and notices of any identified third-party material.

## Working together

Treat contributors and families with respect. Different families may choose
different boundaries. Discuss concrete content patterns and user needs without
harassing creators, parents, or children.
