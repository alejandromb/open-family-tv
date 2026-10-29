# Project plan

Initial research checkpoint: October 28, 2026.

## Purpose

Give children broad, enjoyable video discovery and give parents practical controls
over recurring content patterns. Entertainment, fantasy, comedy, and silliness
belong in the experience. The product should reduce ongoing parent maintenance.

## Initial scope

Start with one household and one Fire OS device. The first usable version should
offer a varied catalogue, remote navigation, video playback, local parent settings,
and understandable filtering decisions. Fire OS and Vega OS are separate platform
targets; verify the actual device before choosing build tools.

Initial exclusions from scope: public accounts, subscriptions or billing,
cross-device synchronization, a mobile parent app, unrestricted internet search,
and universal full-video AI moderation. Public distribution follows household
validation and review of platform, privacy, and content-source requirements.

## Parent preference model

| Preference | Distinction to investigate |
| --- | --- |
| Toy promotion | Product selling and showcasing versus imaginative toy play |
| Shopping and consumption | Hauls and acquisition-focused content versus ordinary story scenes |
| Staged family drama | Influencer-style manufactured conflict versus family activities and stories |
| Challenges and pranks | Extreme or humiliating challenges versus constructive games |

Each preference supports allow, show less, or hide. Age suitability is a separate
eligibility condition. Explicit video and channel exceptions require parent
authority and visible explanations; a favourite channel must not silently bypass
a hard exclusion. Define and test precedence before implementation.

Labels describe observable content patterns rather than a universal judgement of
"good" or "bad." Store evidence, confidence, provenance, and review time. Unknown
is a real state, not an implicit approval. The parent-selected treatment of unknown
content must be explained during setup and tested for its effect on variety.

## Broad discovery

Build an app-owned candidate catalogue and ranking process. Initial subject areas
include cartoons, comedy, stories, animals, crafts, music, science, and languages.
The starter catalogue should contain many distinct sources and an explicit process
for adding unfamiliar sources, rather than relying only on favourites.

Ranking should mix familiarity with novelty and avoid domination by one creator
or format. Explore a configurable novelty share and creator caps; choose values
from evaluation rather than presenting an arbitrary ratio as established.

The initial catalogue is bounded. Children can search within it. New-source
suggestions and catalogue expansion are separate parent-visible flows. We must
measure whether those boundaries leave meaningful choice and manageable upkeep.

## Milestones

### 1. Feasibility

Deliver a minimal TV screen, a supported playback experiment, a small extracted
matching core, and an initial labelled content sample.

Verify remote focus, play/pause, seeking, captions, Back, fullscreen, episode
completion, errors, suspend/resume, and player links or recommendations that may
lead outside the selected content. Record device model, OS, app build, and results
privately; publish only a sanitized compatibility summary.

Investigate both the supported embedded-player path and the technical assumptions
behind a managed web surface. Do not treat a browser-extension demonstration as
proof of a maintainable or distributable TV integration. Decide the playback path
before building the full catalogue UI.

Exit: a written go/no-go decision on playback and navigation, evidence of which
matching components can be isolated, and known limits on available content data.

### 2. Family alpha

Build the native TV shell, local parent profile and PIN, a broad starter catalogue,
preference controls, varied feed, catalogue search, decision explanations, and
parent corrections. Validate matching before rendering and again at selection so
stale cards cannot bypass changed rules. Handle unavailable videos without falling
back to an uncontrolled feed.

### 3. Household trial

Run ordinary viewing for two weeks. Measure unwanted content exposure, worthwhile
content wrongly excluded, discovery variety, playback failures, remote usability,
and parent maintenance time. The trial is evidence about this household and
catalogue, not a general safety certification.

### 4. Small parent pilot

Interview and test with 5–10 families after the alpha works. Recruitment and
contact require a separate authorized step. Compare preference differences,
current workarounds, weekly maintenance tolerance, supported devices, and actual
use. Determine whether one policy model serves multiple families without imposing
the same values on all of them.

## Classification evaluation

Start with roughly 300 public candidate videos spanning wanted, unwanted, and
ambiguous cases. Parent labels are accept, reject, or unsure, with a reason.
Differentiate metadata-only assessment from actual content review. Reserve an
evaluation subset with different creators or series from development examples.

Compare precise phrase rules and source knowledge against any proposed automated
classifier. Report both missed unwanted content and wrongly hidden worthwhile
content, plus coverage, abstentions, and review effort. Manually check videos that
the proposed rules would actually surface. Set acceptance targets before tuning
against the held-out sample.

Do not build the plan around obtaining arbitrary full transcripts. The official
caption download API requires permission to edit the video. Metadata or thumbnails
alone do not prove what happens throughout a video. Creator-provided material or
other authorized evidence may be needed for stronger classification.

## Effort and operating costs

Planning estimate for one experienced developer: 1–2 focused development weeks for
feasibility, followed by 4–8 additional weeks for a bounded family alpha if playback
is viable. This is an estimate, not a commitment. It excludes public release,
universal moderation, and uncertain platform approvals. Part-time calendar time
will be longer.

Measure catalogue refresh quota, classification cost per candidate, cache hit rate,
human review effort, and compatibility maintenance during feasibility. Use those
measurements to propose a budget before committing to recurring infrastructure.

## Open decisions

- Exact device model and installed software; Fire OS first versus a Vega target.
- Playback integration and the extent of navigation containment it can support.
- Catalogue sourcing and a practical age-suitability assessment process.
- Default treatment of unknown or weakly classified content.
- Evidence available for semantic classification without unsupported extraction.
- Criteria for accepting new sources and correcting stale classifications.
- Whether maintainer cooperation could provide access to reusable native work.

## Research references

- [FilterTube reuse assessment](filtertube-reuse.md)
- [Amazon Fire OS and model table](https://developer.amazon.com/docs/fire-tv/fire-os-overview.html)
- [YouTube player parameters](https://developers.google.com/youtube/player_parameters)
- [YouTube developer policies](https://developers.google.com/youtube/terms/developer-policies)
- [Caption download access](https://developers.google.com/youtube/data/reference/rest/v3/captions/download)
