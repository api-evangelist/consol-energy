# CONSOL Energy (consol-energy)

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

CONSOL Energy was a Pittsburgh-based coal mining company that produced high-quality bituminous coal from underground mines for sale to electric utilities, steelmakers, and industrial customers. In January 2025 CONSOL Energy merged with Arch Resources to form Core Natural Resources, Inc. (NYSE: CNR), and consolenergy.com now 301-redirects to corenaturalresources.com.

The company publishes no developer portal, no API documentation, no SDKs and no GitHub organization. It does, however, run its corporate site on WordPress and serve the standard **WordPress REST API anonymously at `https://corenaturalresources.com/wp-json/`** — a real, machine-readable, unauthenticated read surface over company content. That surface carries custom post types the company defined for its own business: **11 mines** (Bailey, Enlow Fork and Harvey from the legacy CONSOL fleet; Black Thunder, West Elk, Leer, Leer South, Beckley, Itmann, Mountain Laurel and Coal Creek), grouped East/West by a `mine-location` taxonomy; **16 leadership and board profiles**; **40 news releases** in 9 series; 22 corporate pages; and a **173-item media library** holding the supplier terms and conditions, the Supplier Code of Conduct and the sustainability and safety PDFs as addressable files.

Every endpoint catalogued here was called anonymously on **2026-09-05** and returned HTTP 200. Write methods and the administrative namespaces exist on the host but are authenticated — `/wp/v2/users` and `/wp/v2/settings` both returned HTTP 401 — and are deliberately not catalogued. The OpenAPI documents in `openapi/` are **derived by API Evangelist** from the route discovery document the host itself serves (saved verbatim as `openapi/consol-energy-content-wp-routes-original.json`); the company publishes no OpenAPI.

This corrects the 2026-07-25 note on this profile, which said the company had "no documented endpoints and no XML feeds." Endpoints are still undocumented — but they are served, and so are `/feed` (RSS 2.0) and `/sitemap.xml`.

Machine-readable **financial** data remains third-party, via the SEC's own EDGAR APIs.

**Related profile:** [arch-coal](https://github.com/api-evangelist/arch-coal) — the other half of the merger. It shares this successor domain, and therefore this same content surface.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/consol-energy/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Producing
- **Access:** 1st-Party
- **Classification:** Company

## Tags

- Bituminous Coal, Coal Mining, Core Natural Resources, Energy, Investor Relations, Mining, Suppliers, Sustainability, Fortune 1000

## Timestamps

- **Created:** 2026-03-23
- **Modified:** 2026-09-05

## APIs

### Core Natural Resources Mines Content API

The `mine` custom post type plus the `mine-location` taxonomy. `GET /wp/v2/mine` returned HTTP 200 with `X-WP-Total: 11`.

- Base URL: `https://corenaturalresources.com/wp-json`
- [Operations page](https://corenaturalresources.com/core-operations/)
- Spec: `openapi/consol-energy-mines-content-api-openapi.yml`

### Core Natural Resources Leadership Content API

The `leader` custom post type plus `leader-category`. `GET /wp/v2/leader` returned HTTP 200 with `X-WP-Total: 16`.

- [Leadership page](https://corenaturalresources.com/about-core/core-leadership/)
- Spec: `openapi/consol-energy-leadership-content-api-openapi.yml`

### Core Natural Resources News Content API

The `article` custom post type plus the `news-series-title` taxonomy. `GET /wp/v2/article` returned HTTP 200 with `X-WP-Total: 40`; the core `posts` collection is registered but empty.

- [News & media](https://corenaturalresources.com/news-media/)
- Spec: `openapi/consol-energy-news-content-api-openapi.yml`

### Core Natural Resources Site Content API

Corporate pages (22) and the media library (173), where the published supplier and sustainability PDFs live.

- Spec: `openapi/consol-energy-site-content-api-openapi.yml`

### Core Natural Resources Discovery API

Registered types and taxonomies, post statuses, cross-type search (89 items) and oEmbed 1.0 — the surface that makes the rest discoverable without documentation.

- Spec: `openapi/consol-energy-discovery-api-openapi.yml`

### SEC EDGAR Filings (Core Natural Resources, CIK 1710366)

Third-party government API — filing history as JSON. CIK 0001710366 is the CONSOL Energy Inc. registrant, renamed Core Natural Resources in January 2025, so it covers CONSOL's filing history as well as the merged company's.

- [EDGAR APIs documentation](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)
- [https://data.sec.gov/submissions/CIK0001710366.json](https://data.sec.gov/submissions/CIK0001710366.json)

**Evidence, verified 2026-07-25, re-probed 2026-09-05.** The documentation page describes RESTful JSON APIs on `data.sec.gov`, no authentication required, with a declared User-Agent and a 10-requests-per-second fair-access ceiling. It returns HTTP 403 to a generic browser User-Agent and HTTP 200 to a declared one. Calling the endpoint returned HTTP 200 with JSON naming "Core Natural Resources, Inc.", ticker CNR, and the former name "CONSOL Energy Inc." through 2025-01-10.

## What the company does not publish

Probed 2026-09-05, all returning HTTP 404 on both `corenaturalresources.com` and `consolenergy.com`: every `/.well-known/` path in the pipeline's list (security.txt, openid-configuration, oauth-authorization-server, oauth-protected-resource, api-catalog, ai-plugin.json, apis.json, agent-card.json, agent.json, aauth-resource.json), plus `/apis.json`, `/apis.yml`, `/llms.txt` and `/AGENTS.md`. A negative-control path confirmed the hosts are not answering 200 to everything. There is no status page, no changelog, no security or disclosure page, no trust center, no MCP server, no A2A agent card, no SDK in any registry, no GitHub organization, and no pricing or plans of any kind. Those absences are recorded as data, not guessed.

## Common Properties

- [Website](https://corenaturalresources.com/)
- [Legacy Website](https://consolenergy.com) (301 to the successor domain; the previously listed `www.consol-energy.com` no longer resolves and was removed)
- [Suppliers](https://corenaturalresources.com/suppliers/)
- [Investor Relations](https://corenaturalresources.com/investors/)
- [Newsroom](https://corenaturalresources.com/news-media/)
- [Sustainability](https://corenaturalresources.com/sustainability/)
- [Careers](https://corenaturalresources.com/careers/)
- [Contact](https://corenaturalresources.com/contact-us/)
- [Privacy Policy](https://corenaturalresources.com/privacy-policy/)
- [Terms and Conditions](https://corenaturalresources.com/arch-terms-and-conditions/)
- [LinkedIn](https://www.linkedin.com/company/consol-energy)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
