# Stanford University (stanford)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Stanford University (QS World 2025 #6) has a multi-pronged developer footprint. University IT (UIT) runs a developer hub exposing certificate-secured MaIS Registry APIs and an AI API Gateway; Stanford Libraries (DLSS) publishes a public API documentation site (IIIF, PURL, Embed, Digital Stacks, Library Hours) backing the Stanford Digital Repository; and the Registrar's ExploreCourses offers a course-data XML query interface.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/stanford/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=stanford-api-evangelist&utm_content=repo)

## Type
- **x-type:** Index (Consumer / 3rd-Party)

## Tags
- Education, Higher Education, University, Research, Library, Digital Repository, IIIF, Courses

## APIs
- **Stanford Libraries IIIF API** — IIIF Presentation (v2/v3) + Image v2 for the Digital Repository. Base `https://purl.stanford.edu`. [Docs](https://api.library.stanford.edu/docs/iiif/api/)
- **PURL API** — Persistent URLs to SDR content (HTML/XML/MODS). [Docs](https://api.library.stanford.edu/docs/purl/api/)
- **Library Hours API** — Library location operating hours. [Docs](https://api.library.stanford.edu/docs/library-hours/api/)
- **ExploreCourses API** — XML query of the Registrar's catalog (13,000+ courses). Base `https://explorecourses.stanford.edu/search`. [About](https://explorecourses.stanford.edu/about)
- **CAP / Stanford Profiles API** — Academic profiles directory (18,000+); credentialed via HelpSU. Base `https://cap.stanford.edu/cap-api`.
- **MaIS Registry APIs** — Account/Person/Student/CourseClass/Privilege/Workgroup; x509-cert gated. [Docs](https://uit.stanford.edu/developers/apis)

## Plans, Rate Limits, FinOps
- [Plans](plans/stanford-plans-pricing.yml) — Free/open library + course APIs; certificate/credentialed registry APIs.
- [RateLimits](rate-limits/stanford-rate-limits.yml) — No published global limit; harvest politely.
- [FinOps](finops/stanford-finops.yml) — Non-commercial; no usage-based API billing.

## Timestamps
- **Created:** 2026-06-03
- **Modified:** 2026-06-03

## Common Properties
- [Website](https://www.stanford.edu/)
- [Developer (UIT)](https://uit.stanford.edu/developers)
- [Developer (Libraries)](https://api.library.stanford.edu/)
- [GitHub (DLSS)](https://github.com/sul-dlss)

## Notes
- Two live public developer hubs verified: UIT (uit.stanford.edu/developers) and Stanford Libraries (api.library.stanford.edu); all library doc paths use hyphens (e.g. `/docs/digital-stacks/api/`). See [review.yml](review.yml).
- MaIS Registry APIs are documented publicly but require an x509 client certificate signed by the MaIS team (no public base URLs/sandbox).
- ExploreCourses has no formal public reference; the `?view=xml-20140630` query pattern is community-documented and confirmed live.
- The real SDR/library GitHub org is `sul-dlss` (`SUDigitalRepository` does not exist).

## Maintainers
**FN:** Kin Lane

**Email:** kin@apievangelist.com
