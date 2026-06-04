# Stanford University (stanford)

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
