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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Stanford University is a private research university in Stanford, California. It is one of the very
few institutions in the API Evangelist university cohort whose programmable footprint is **entirely
institution-operated** — every surface profiled here runs on a `stanford.edu` host. There is no
Figshare, Elsevier Pure, Ex Libris, Dataverse or Symplectic contract attributed to Stanford, and
none was removed to get to that state.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/stanford/refs/heads/main/apis.yml)

## Type
- **x-type:** university
- **x-category:** Private Research University
- **Position:** Producer / 1st-Party

## Operator attribution

Every entry in `apis.yml` carries an `x-operator`. For Stanford the count is **15 institution, 0
tenant, 0 vendor, 0 placeholder** — verified against `servers[]`, `info.title` and live host
resolution, not against where an artifact was fetched.

## APIs

### Open, no credential
- **PURL API** — `purl.stanford.edu/{druid}` with `.xml` (cocina publicObject), `.mods` (MODS 3.7)
  and `/iiif/manifest` projections.
- **IIIF API** — IIIF Presentation 2.1 manifests; Image v2 tiles from `stacks.stanford.edu`.
- **Library Hours API** — JSON:API document, 24 library locations, at
  `library-hours.stanford.edu/libraries.json`.
- **Embed API** — oEmbed 1.0 rich responses from the SUL Embed Service.
- **Digital Stacks API** — file and image delivery for repository content.
- **ExploreCourses** — the Registrar's course catalog as XML (`?view=xml-20140630`). The largest
  genuinely public dataset Stanford serves, and it reports its own deprecation in the response body.

### First-party OpenAPI contracts (SUL-DLSS, Apache 2.0)
Five contracts, 76 operations, 46 component schemas. Public specs on Stanford's own GitHub org;
the services themselves sit on the internal network.
- **DOR Services API** — OpenAPI 3.1.2, 40 paths / 53 operations. The largest contract Stanford publishes.
- **SDR API** — OpenAPI 3.0.0, deposit into the Stanford Digital Repository.
- **Preservation Catalog HTTP API**, **Technical Metadata API**, **SURI API** — OpenAPI 3.0.0.

### Gated
- **MaIS Registry APIs** — Account, Person, Student, CourseClass, Privilege, Workgroup. x509 client
  certificate signed by the MaIS team; no public base URL, no sandbox.
- **AI API Gateway** — LLM access inside Stanford's own cloud, keyed per API key and billed to a
  Stanford PTA, approved for High Risk data and PHI.
- **CAP / Stanford Profiles API** — 18,000+ profiles; console redirects to authentication.

### Identity federation
- **Stanford Identity Provider** — signed Shibboleth SAML 2.0 metadata at `idp.stanford.edu/metadata.xml`,
  entityID `https://idp.stanford.edu/`, valid until 2027-08-16, `shibmd:Scope` = `stanford.edu`.

## Education-regime conformance

Scored against the Kin Score `education` regime standards.

| Standard | Status | Evidence |
|---|---|---|
| `saml` | **conformant** | SAML 2.0 `EntityDescriptor` + `IDPSSODescriptor` + 3 SSO bindings |
| `shibboleth` | **conformant** | `urn:mace:shibboleth:metadata:1.0`, `shibmd:Scope stanford.edu` |
| `datacite` | indirect | `assign_doi` parameter in two SDR contracts; no registration agency named |
| `oai-pmh` | **absent** | six `?verb=Identify` probes, all 404 |
| `orcid`, `crossref`, `scim`, `lti`, `oneroster`, `ed-fi`, `caliper`, `qti` | absent | no evidence found |

Also observed, outside the regime list: IIIF Presentation 2.1, MODS 3.7, JSON:API, oEmbed 1.0,
OpenAPI 3.0/3.1.

## What Stanford does not publish

Recorded because an honest absence is a measurement:
- No OAI-PMH provider on any Stanford host.
- No institution-operated open-data portal.
- No OAuth or fine-grained scopes anywhere; authorization is per-service.
- No `info.contact` or `info.termsOfService` in any of the five contracts.
- No request or response examples on any of the 76 operations.
- No `deprecated` flag, Sunset header, or published deprecation policy.
- No unified developer portal spanning the Libraries and University IT surfaces.

## Probe limitation

`searchworks.stanford.edu`, `exhibits.stanford.edu` and `earthworks.stanford.edu` return a **200
with an F5/Shape JavaScript challenge body** to any automated client. They are live for humans and
unreadable to us. That is a limitation of our probe, not a finding about Stanford.

## Artifacts
- [openapi/](openapi/) + [openapi/_original/](openapi/_original/) — five first-party contracts
- [json-schema/](json-schema/) — 46 component schemas derived from those contracts
- [examples/](examples/) — seven live captures, provenance in [examples/index.yml](examples/index.yml)
- [authentication/](authentication/stanford-authentication.yml) · [scopes/](scopes/stanford-scopes.yml) · [errors/](errors/stanford-errors.yml)
- [conformance/](conformance/stanford-conformance.yml) · [lifecycle/](lifecycle/stanford-lifecycle.yml) · [vocabulary/](vocabulary/stanford-vocabulary.yml) · [rules/](rules/stanford-rules.yml)
- [json-ld/](json-ld/stanford-context.jsonld) · [plans/](plans/stanford-plans-pricing.yml) · [rate-limits/](rate-limits/stanford-rate-limits.yml) · [finops/](finops/stanford-finops.yml)

## Timestamps
- **Created:** 2026-06-03
- **Modified:** 2026-08-19

## Maintainers
**FN:** Kin Lane

**Email:** kin@apievangelist.com
