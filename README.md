# Open Family TV

Broad video discovery for children, with meaningful parent controls.

Open Family TV is an open-source project exploring a Fire TV app where children
can discover cartoons, comedy, stories, crafts, animals, music, and other interests,
while parents can express preferences about toy promotion, shopping hauls, staged
family drama, and extreme challenges.

Parents should be able to set understandable rules without maintaining thousands
of channel blocks. Children should have room to develop their own tastes.

**Status: planning and feasibility research. There is no installable app yet.**
Playback integration, filtering accuracy, and the proposed TV experience have not
been validated on hardware. This project does not provide a child-safety guarantee.

**YouTube integration is not cleared.** Its published compliance guide restricts
API-based content-category inference and suitability claims, as well as blocking
related-video links in its player. These restrictions directly affect the proposed
classifier and viewing boundaries. See the [policy review](docs/youtube-policy-review.md)
before implementing or describing a YouTube-backed version as permitted.

## The proposed experience

- A varied discovery feed that mixes familiar favourites with unfamiliar content.
- Parent preferences for **allow**, **show less**, and **hide**.
- Separate treatment of age suitability and family content preferences.
- Reasons for filtering decisions, including evidence and uncertainty.
- Simple parent corrections and exceptions.
- A TV interface designed for the remote, with protected parent settings.
- Local profiles and preferences, with minimal collection of child activity.

These are proposed features, not implemented capabilities. A broad starter
catalogue will still have boundaries; parents should understand and influence how
it expands.

## Start here

| Document | Purpose |
| --- | --- |
| [Project plan](docs/plan.md) | Scope, milestones, evaluation, and open decisions |
| [Architecture](docs/architecture.md) | Proposed components and playback decision gates |
| [YouTube policy review](docs/youtube-policy-review.md) | Material restrictions and the permission questions to resolve |
| [FilterTube reuse assessment](docs/filtertube-reuse.md) | What is publicly available and what needs new work |
| [Contributing](CONTRIBUTING.md) | How to help and what evidence to include |

The first milestone is a small feasibility experiment: play representative videos
on a Fire TV, operate them with the remote, and apply a few explainable filters.
We will evaluate filtering mistakes and discovery variety before expanding scope.

## Relationship to FilterTube and YouTube

[FilterTube](https://github.com/varshneydevansh/FilterTube) is an existing project
with a public MIT-licensed browser runtime. Its identity helpers, matching logic,
and relevant tests are candidates for reuse. Its documentation describes the
native app shell as living in a separate private repository.

This repository currently contains original planning documents and project setup;
it does not yet contain copied FilterTube code. Any future reuse must retain the
applicable notices and record its provenance.

Open Family TV is independent and is not affiliated with or endorsed by Amazon,
Google, YouTube, or FilterTube. Video rights remain with their respective owners.
The project name is a working name.

## Contribute

Useful early contributions include playback feasibility findings, Fire TV remote
UX experiments, filtering examples with public video links, and feedback on the
parent preference model. See [CONTRIBUTING.md](CONTRIBUTING.md).

Please use synthetic examples or public content. Do not upload children's viewing
histories, account details, device identifiers, or household network captures.

## License

[MIT](LICENSE). Third-party code, assets, services, and video content remain subject
to their own terms.
