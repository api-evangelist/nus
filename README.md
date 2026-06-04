# National University of Singapore (nus)

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
