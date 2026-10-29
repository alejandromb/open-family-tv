# YouTube review request draft

Status: DRAFT — not submitted. No API project or credentials have been created for
this project by the maintainers as part of this work. No YouTube approval has been
obtained. Research checkpoint: October 28, 2026.

This file is a public product description. Applicant identity, private contact
details, project identifiers, review credentials, and other submission-only
information must be supplied privately by the owner, not committed here.

## Proposed clarification text

**Subject: Open Family TV — clarification of parent-defined discovery and content-tagging use case**

We are developing Open Family TV, an independent open-source project exploring
a child-directed Fire TV viewing application with parent-controlled content
selection. The public planning repository is
https://github.com/alejandromb/open-family-tv. We have no released app, active users,
or production YouTube integration. We are seeking guidance on the appropriate
review route and whether the following proposed implementation can comply with
YouTube's API policies before committing to it.

Our intended added value is a varied discovery experience that lets parents
express family preferences without individually reviewing every video or
maintaining large channel blocklists. The app would distinguish age suitability
from family preferences; it would not advertise YouTube-approved safety ratings or
guaranteed child safety.

We are considering two distinct feature groups:

1. Parent-authored inclusion/exclusion rules for video or channel identifiers,
   precise phrases, and metadata supplied by the API. The app would select
   candidates for its own clearly identified catalogue and rank eligible items to
   preserve creator and subject variety. We request clarification on what
   selection, ranking, and search-result filtering is permissible, including under
   the permitted-feature-limitation provisions. We will not assume that parent
   consent waives other policy requirements.
2. Additive descriptive labels such as product showcasing, shopping hauls, staged
   family drama, or challenge formats, combined with parent choices to allow,
   reduce, or exclude matching items. These are proposed custom classifications,
   not fields returned by YouTube. We understand that the ordinary derived-data
   rules and compliance guide restrict inferred categories and suitability claims.
   We also read the additional derived-metrics policy allowing descriptive tags
   for accepted analytics use cases. Does that permission route apply to this
   disclosed viewing use case or to an associated parent-facing analysis component?
   If not, is another permission process available, or must this feature group be
   removed? We will not characterize the app as analytics-only if it is used for
   child viewing.

The candidate Data API endpoints are videos.list, channels.list, playlists.list,
playlistItems.list, videoCategories.list, and optionally search.list for public
catalogue discovery. Actual endpoint selection and quota needs remain unmeasured.
The initial design would not use OAuth, private account data, YouTube Kids profile
data, or API write operations. It would not scrape YouTube, use undocumented APIs,
download audiovisual content, or assume access to arbitrary video transcripts.

Playback would use the official embedded player, preserve required attribution,
metadata, advertisements, and player functionality, and identify the application
as required. We understand that related-video links cannot simply be removed or
blocked. Please clarify which parent-managed navigation or handoff controls, if
any, are permissible while preserving these player requirements. We will revise
our viewing-boundary claims or design if the required behaviour is incompatible.

Local profiles and parent preferences are proposed. We do not intend to require
child Google sign-in, use personalized advertising, or collect child activity for
model training. A public privacy policy and concrete data-flow diagram would be
prepared for the actual implementation; these are design intentions rather than
claims about an app that already exists. Please identify the child-directed
notification and review requirements for the proposed setup.

We are not requesting additional quota at this stage. We request guidance on the
appropriate policy-review channel and the materials needed for an accurate
submission. We understand that a standard API key or additional quota would not
grant an exception to prohibited functionality. Please distinguish ordinary
permitted behaviour, any amendment requiring explicit acceptance or approval,
and functionality that cannot be offered under the applicable policies.

## Submission readiness

The current linked audit form asks for project identifiers, owner/contact details,
a privacy-policy URL, and supporting implementation evidence. Its initial request
choices concern additional quota or a requested re-audit. Do not choose either
inaccurately to force this pre-development question through the form.

| Item | Current state / required next step |
| --- | --- |
| Public project description | Planning repository exists; it is not a running app or demo. |
| Applicant identity and contact | Owner to supply privately; no registered organization is assumed. |
| Cloud project number | Not created for this work. Creating one is a separate account action. |
| API credentials | Not created; never include keys or tokens in this repository or review text. |
| Audit request type | Appropriate route for a pre-development question needs confirmation. |
| Privacy policy and terms | Not yet drafted for an implemented data flow; planning docs are not substitutes. |
| Screenshots or demo | No prototype exists. Future mockups must be identified as mockups. |
| Child-directed notification | Not submitted; verify the applicable process for the chosen design. |
| Quota request | None at this stage. Measure actual use before requesting more. |
| Derived-data amendment | Eligibility unresolved; no amendment has been accepted. |

Review the exact final text, identity fields, evidence, and any form agreements
with the owner before submission. Preparing this draft does not authorize sending
it, supplying private information, creating credentials, or accepting amendments.

## Official references

- [API overview and setup](https://developers.google.com/youtube/data/getting-started)
- [Compliance guide and direction for uncertain use cases](https://developers.google.com/youtube/terms/developer-policies-guide)
- [Developer policies](https://developers.google.com/youtube/terms/developer-policies)
- [Additional derived-metrics and storage policy](https://developers.google.com/youtube/terms/derived-metrics-policy)
- [Quota and compliance audits](https://developers.google.com/youtube/data/guides/quota_and_compliance_audits)
- [Linked audit and quota form](https://support.google.com/youtube/contact/yt_api_form)
