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

The National University of Singapore (NUS) is Singapore's flagship public research university. This
repository catalogs the institution's public developer and API footprint as an
[APIs.json](https://apisjson.org) profile, built under the API Evangelist **university pipeline**,
whose first question is never "is there a spec" but **who operates the thing the spec describes**.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/nus/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=nus-api-evangelist&utm_content=repo

## The short version

NUS operates **one** substantial machine-readable API surface of its own — its federated identity
service. Everything else that looks like an NUS API belongs to a platform NUS rents.

## Type

- University / Public Research University — Index / Consumer / 3rd-Party

## Surfaces, by operator

Every surface carries an `x-operator`. `institution` means NUS runs it; `tenant` means it is NUS's
data and NUS's account on somebody else's platform.

### Institution-operated

- **NUS Federated Identity Service (VAFS)** — `https://vafs.nus.edu.sg/adfs` — the one real find.
  Publishes a live OpenID Connect discovery document, a JWKS, and signed SAML 2.0 / WS-Federation
  metadata for entityID `https://vafs.nus.edu.sg/adfs/services/trust`. Anonymously readable.
  Ownership is not inferred: the TLS certificate is an Extended Validation certificate issued to
  `O=National University of Singapore`.
- **NUS NextBus (Internal Shuttle Bus) API** — `https://nnextbus.nus.edu.sg/` — genuinely NUS's,
  genuinely live, and gated behind HTTP Basic credentials NUS does not issue publicly (401).
- **api.nus.edu.sg** — an API gateway hostname on an NUS-issued certificate that returns HTTP 500
  on every path probed, including `/`, `/docs`, `/api-docs` and `/swagger.json`. Live host, no
  service. Recorded in `x-coverage`, not listed as a surface.

### Tenant — NUS's data, somebody else's contract

- **ScholarBank@NUS** (REST + OAI-PMH) — Atmire Open Repository's DSpace 7.6
  (`scholarbank.nus.edu.sg` CNAMEs to `nusor.cname.openrepository.com`).
- **NUS Canvas** — Instructure (`nus-vanity.instructure.com`). LTI 1.3 JWKS public, REST API 401.
- **Blog.nus** — CampusPress managed WordPress, 190 REST routes, anonymously readable.
- **NUSMods API** — the only public machine-readable description of NUS course data in existence,
  and it is a **student organisation's** work (NUSModifications, `api.nusmods.com`, MIT licensed),
  not the university's. No institutional endorsement was found.
- **SGAF federation entry** — NUS is one of fourteen identity providers in the Singapore Access
  Federation, but the entityID it is registered under is a SimpleSAMLphp proxy SingAREN operates
  on NUS's behalf.

## What is deliberately absent

No developer portal. No institution-wide GitHub organisation. No public open-data portal. No
`llms.txt` (the 200 at `nus.edu.sg/llms.txt` is a soft-404 returning HTML). No status page, no
changelog, no deprecation policy, and no self-service registration path to any NUS API.

Most notably: NUS's own course vocabulary — modules, modular credits, prerequisite trees — has no
public machine-readable expression from the university at all. The NUSMods specification states the
data is scraped daily from "official APIs provided by the Registrar's Office", so an institutional
course API exists; the public simply cannot reach it.

## Domain standards (Kin Score `education` regime)

Confirmed: `saml` (institution), `oai-pmh` (tenant), `lti` 1.3 (tenant).
Partial: `shibboleth` (institution, via SGAF/eduGAIN), `orcid` (tenant), `datacite` (tenant).
Not found: `scim` (probed, 404/503), `crossref`, `oneroster`, `caliper`, `qti`, `ed-fi`.

Only two of the six hits belong to NUS's own engineering, and both are identity federation. See
[conformance/nus-conformance.yml](conformance/nus-conformance.yml).

## Artifacts

| Artifact | Path |
|---|---|
| OpenAPI (derived, institution) | [openapi/nus-identity-openapi.yml](openapi/nus-identity-openapi.yml) |
| Pristine pre-refine copy | [openapi/_original/](openapi/_original/) |
| Identity federation | [identity-federation/nus-identity-federation.yml](identity-federation/nus-identity-federation.yml) |
| Domain standard conformance | [conformance/nus-conformance.yml](conformance/nus-conformance.yml) |
| Authentication | [authentication/nus-authentication.yml](authentication/nus-authentication.yml) |
| Scopes | [scopes/nus-scopes.yml](scopes/nus-scopes.yml) |
| Errors | [errors/nus-errors.yml](errors/nus-errors.yml) |
| Lifecycle | [lifecycle/nus-lifecycle.yml](lifecycle/nus-lifecycle.yml) |
| JSON Schema | [json-schema/](json-schema/) |
| Examples (verbatim live captures) | [examples/](examples/) |
| Vocabulary | [vocabulary/nus-vocabulary.yml](vocabulary/nus-vocabulary.yml) |
| Rules | [rules/nus-rules.yml](rules/nus-rules.yml) |
| JSON-LD | [json-ld/nus-context.jsonld](json-ld/nus-context.jsonld) |
| Agentic access | [agentic-access/nus-agentic-access.yml](agentic-access/nus-agentic-access.yml) |
| Domain security | [security/nus-domain-security.yml](security/nus-domain-security.yml) |
| Plans / Rate limits / FinOps | [plans/](plans/) · [rate-limits/](rate-limits/) · [finops/](finops/) |
| Review | [review.yml](review.yml) |

Every artifact carries `generated`, `method` (`searched` / `generated` / `derived` / `probed` /
`none`) and `source`. The OpenAPI in this repository is **derived** — NUS publishes no OpenAPI;
every path in it was read out of the university's own live OIDC discovery document.

## Corrections made on 2026-08-19

- Two NUSMods request collections were **removed**. They describe a student organisation's API, not
  the university's, and crediting them to NUS was an artifact-presence-is-not-provenance error. The
  relationship is retained as a `tenant` entry.
- `agentic-access/` was regenerated. The previous version was derived from the NUSMods OpenAPI and
  pointed at a source file that no longer exists; it now derives from the institution-operated
  identity contract.
- `security/nus-domain-security.yml` was rebuilt around TLS certificate **organization** fields,
  which settle operator attribution more reliably than any heuristic.

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-19

## Maintainers

- Kin Lane — kin@apievangelist.com
