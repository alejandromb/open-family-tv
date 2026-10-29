# YouTube integration policy review

Research date: October 28, 2026. This is a record of published platform requirements
and open design questions, not legal clearance or a finding of approval by YouTube.

## Current disposition

Third-party playback through YouTube's supported player is documented. The complete
Open Family TV proposal is not cleared. An official player does not establish
permission for every classification, filtering, or navigation feature around it.
Being open source and reusing MIT-licensed code do not waive platform obligations.

## Material findings

The official [compliance guide](https://developers.google.com/youtube/terms/developer-policies-guide)
lists inferring video/channel content categories and making safety/suitability
claims as disallowed uses of its API. It also prohibits blocking related-video
links and other standard player functionality. These findings directly affect our
proposed semantic labels and the ability to contain playback within selected
content. The guide directs uncertain use cases to the API Compliance Audit process.

The [developer policies](https://developers.google.com/youtube/terms/developer-policies)
restrict derived API data, scraping, player modification, and interference with
advertisements. Child-directed API clients have additional obligations, including
notification to Google, applicable privacy compliance, and restrictions on API
write actions. This is not an exhaustive requirements list.

The [player parameters](https://developers.google.com/youtube/player_parameters)
do not offer a complete related-video disable switch. Player integration must also
follow the [required minimum functionality](https://developers.google.com/youtube/terms/required-minimum-functionality),
including application identification requirements.

## Questions to resolve before committing to this provider

1. Can the intended parent-defined selection/ranking service operate under the
   current policies, and which exact functions require permission?
2. Is any proposed classification based on independently obtained, authorized
   evidence permissible in this specific integration? Do not assume that changing
   a data source or relabelling a score avoids the restrictions.
3. What viewing boundaries can be provided while retaining required player links
   and functionality? Can that experience meet the actual family need?
4. Which child-directed registration, data handling, and distribution requirements
   apply to the planned implementation?

Prepare an implementation-specific description for YouTube's documented compliance
process and obtain appropriate legal review before public deployment. No request
has been submitted and no approval has been obtained.

## Work that can proceed independently

Prototype the TV interface, local parent policy, transparent explanations, and
ranking with synthetic fixtures or appropriately licensed independent content.
Keep a provider boundary so a negative YouTube feasibility outcome does not require
discarding the whole project. Explore creator partnerships or other authorized
catalogues as separate sourcing options, not as a presumed workaround to YouTube's
terms.

The earlier feasibility plan remains a product hypothesis. Its content-classifier
and playback-containment assumptions must not be presented as established YouTube
capabilities or permissions.
