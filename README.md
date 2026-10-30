# National University of Singapore

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

The National University of Singapore is Singapore's flagship public research university, ranked eighth in the QS World University Rankings 2025, and it is a near-perfect illustration of why a university is a federation of buyers rather than a producer. NUS operates exactly one substantial machine-readable API surface of its own: the federated identity service at vafs.nus.edu.sg, which publishes a live OpenID Connect discovery document, a JWKS, and signed SAML 2.0 metadata for entityID https://vafs.nus.edu.sg/adfs/services/trust, and which registers NUS as an identity provider in the Singapore Access Federation. Everything else that looks like an NUS API belongs to a platform NUS rents — ScholarBank@NUS is Atmire's DSpace, the learning management system is Instructure's Canvas, the blogs are CampusPress, the library guides are Springshare. NUS has an API gateway hostname at api.nus.edu.sg on a certificate issued to the university, and it returns HTTP 500 on every path. The campus shuttle bus API at nnextbus.nus.edu.sg is genuinely NUS's and genuinely live, but sits behind HTTP Basic credentials the university does not issue publicly. Most strikingly, NUS's own course vocabulary — modules, modular credits, prerequisite trees — has no public machine-readable expression from the university at all; the only OpenAPI describing NUS course data is published by NUSMods, a student organisation, from a non-NUS domain. There is no NUS developer portal, no institution-wide GitHub organisation, no public open-data portal, no llms.txt, and no self-service registration path to any NUS API.

**Areas:** University · Higher Education · Education · Singapore · Research · Identity Federation · Research Repository · Course Catalog · Open Access · LMS

## National University of Singapore on APIs.io

Everything profiled for National University of Singapore is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/nus/](https://apis.io/providers/nus/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [NUS NextBus (Internal Shuttle Bus) API](https://apis.io/apis/nus/nextbus/) — The API behind the NUS internal shuttle bus service — bus stops, services and arrival times across the Kent Ridge and Bukit Timah campuses.…
- [ScholarBank@NUS DSpace REST API](https://apis.io/apis/nus/scholarbank-rest/) — The HAL-style REST API of ScholarBank@NUS, the university's institutional repository — communities, collections, items, bitstreams and a 485-field metadata…
- [ScholarBank@NUS OAI-PMH Interface](https://apis.io/apis/nus/scholarbank-oai/) — OAI-PMH 2.0 metadata harvesting endpoint for ScholarBank@NUS, advertising twelve metadata formats including oai_dc, qdc, mods, mets, marc, etdms and…
- [NUS Canvas LMS API](https://apis.io/apis/nus/canvas/) — The learning management system for NUS courses, running on Instructure's Canvas as a vanity tenant. The REST API is live and returns a structured 401 to…
- [National University of Singapore Website (WordPress REST)](https://apis.io/apis/nus/blog-nus-edu-sg-website-wordpress-rest/) — The public WordPress REST API (wp-json) of the National University of Singapore website at blog.nus.edu.sg: the route index of the site's content management…
- [NUSMods API (student-operated, not endorsed)](https://apis.io/apis/nus/nusmods/) — The only public machine-readable description of NUS course data that exists — module lists, module information, prerequisite trees, timetables and venue…
- [NUS entry in the Singapore Access Federation](https://apis.io/apis/nus/sgaf/) — NUS is one of fourteen identity providers registered in the Singapore Access Federation, which SingAREN operates and which interfederates with eduGAIN. The…
- [National University of Singapore Authorization API](https://apis.io/apis/nus/nus-authorization-api/) — OAuth 2.0 / OpenID Connect authorization and token issuance.
- [National University of Singapore Discovery API](https://apis.io/apis/nus/nus-discovery-api/) — Machine-readable metadata describing the identity service and its signing keys.
- [National University of Singapore Session API](https://apis.io/apis/nus/nus-session-api/) — End-user claims and session termination.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Nus Agentic Access](https://apis.io/agentic-access/nus/nus-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [NUS JSON Web Key Set](https://apis.io/schemas/nus/nus-jwks/)
- [NUS OpenID Provider Metadata](https://apis.io/schemas/nus/nus-openid-configuration/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Nus Context](https://apis.io/jsonld/nus/nus-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [NUS NUSMods API Vocabulary](https://apis.io/vocabularies/nus/nus-vocabulary/)

#### Examples (3)

Example requests and responses.

- [Nus Jwks Example](https://apis.io/examples/nus/nus-jwks-example/)
- [Nus Openid Configuration Example](https://apis.io/examples/nus/nus-openid-configuration-example/)
- [Nus Scholarbank Dspace Root Example](https://apis.io/examples/nus/nus-scholarbank-dspace-root-example/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [National University of Singapore API Rules](https://apis.io/rules/nus/nus-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Nus Authentication](https://apis.io/security/nus/nus-authentication/)
- [Nus Domain Security](https://apis.io/security/nus/nus-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Nus Scopes](https://apis.io/scopes/nus/nus-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Nus Plans Pricing](https://apis.io/plans/nus/nus-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Nus Rate Limits](https://apis.io/rate-limits/nus/nus-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Nus Finops](https://apis.io/finops/nus/nus-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://nus.edu.sg/)
- [Blog](https://news.nus.edu.sg/)

## API Evangelist rating

**Kin Score 26.4** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 24.7 |
| Contract governance | 11.4 |
| Operational transparency | 23.7 |
| Developer ergonomics | 23.8 |
| Access clarity | 21.1 |

**Agent readiness 29.0** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 26.5** — Education & Research

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/nus/](https://apis.io/providers/nus/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for National University of Singapore: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/nus/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
