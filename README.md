# National University of Singapore (nus)

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

The National University of Singapore (NUS) is Singapore's flagship public research university, ranked #8 in the QS World University Rankings 2025. This repository catalogs the institution's public developer and API footprint as an [APIs.json](https://apisjson.org) profile. NUS does not run a single unified public developer portal; its confirmed programmatic surface is concentrated in open scholarly infrastructure (ScholarBank@NUS) plus a community-maintained module/timetable API.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/nus/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=nus-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Singapore, Research, Open Access, Repository

## APIs

- **ScholarBank@NUS DSpace REST API** — HAL-style REST API for the NUS institutional repository (DSpace 7.6): communities, collections, items, bitstreams, metadata. Docs: https://scholarbank.nus.edu.sg/server/api
- **ScholarBank@NUS OAI-PMH Interface** — Standard OAI-PMH metadata harvesting endpoint. Docs: https://scholarbank.nus.edu.sg/oai/request?verb=Identify
- **NUSMods API (Unofficial / Community)** — Community-maintained JSON API for NUS module, course, and timetable data. Docs: https://github.com/nusmodifications/nusmods-api/blob/master/README.md

## Plans

- [plans/nus-plans-pricing.yml](plans/nus-plans-pricing.yml)

## Rate Limits

- [rate-limits/nus-rate-limits.yml](rate-limits/nus-rate-limits.yml)

## FinOps

- [finops/nus-finops.yml](finops/nus-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://nus.edu.sg/
- LinkedIn: https://www.linkedin.com/school/national-university-of-singapore/
- Twitter/X: https://twitter.com/NUSingapore
- Authentication (ADFS/SAML SSO): https://vafs.nus.edu.sg/adfs/ls/
- Review: [review.yml](review.yml)

## Notes

- All endpoints were probed live on 2026-06-03. ScholarBank@NUS REST (`/server/api`) and OAI-PMH (`/oai/request`) both returned HTTP 200 and identify as DSpace 7.6.
- The NUSMods API is **unofficial** — maintained by the open-source NUSModifications project, not by NUS itself.
- `github.com/nus` is **not** National University of Singapore; it resolves to an unrelated individual user and was deliberately excluded. No official NUS GitHub organization was confirmed.
- Most student/administrative systems sit behind ADFS/SAML single sign-on and are not publicly documented APIs.

## Maintainers

- Kin Lane — kin@apievangelist.com
