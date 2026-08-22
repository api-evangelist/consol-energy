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

CONSOL Energy was a Pittsburgh-based coal mining company that produced high-quality bituminous coal from underground mines for sale to electric utilities, steelmakers, and industrial customers. In 2025 CONSOL Energy merged with Arch Resources to form Core Natural Resources, and the consolenergy.com domain now redirects to corenaturalresources.com. The combined company does not publish public developer APIs; its external digital surface is organized around an investor relations site, a suppliers page (with downloadable terms, conditions, and a Supplier Code of Conduct), and corporate sustainability/safety disclosures — all HTML and PDF, with no documented endpoints and no XML feeds (probed 2026-07-25).

**Related profile:** [arch-coal](https://github.com/api-evangelist/arch-coal) — the other half of the merger.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/consol-energy/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party
- **Classification:** Company

## Tags

- Bituminous Coal, Coal Mining, Core Natural Resources, Energy, Investor Relations, Mining, Suppliers, Sustainability

## Timestamps

- **Created:** 2026-03-23
- **Modified:** 2026-04-28

## APIs

The suppliers and investor relations pages were previously listed here as APIs. They are corporate web pages — no documented endpoints, no machine-readable feeds — so they now appear under Common Properties as website surfaces instead.

### SEC EDGAR Filings (Core Natural Resources, CIK 1710366)

Third-party government API — filing history as JSON. CIK 0001710366 is the CONSOL Energy Inc. registrant, renamed Core Natural Resources in January 2025, so it covers CONSOL's filing history as well as the merged company's.

- [EDGAR APIs documentation](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)
- [https://data.sec.gov/submissions/CIK0001710366.json](https://data.sec.gov/submissions/CIK0001710366.json)

**Evidence, verified 2026-07-25.** The documentation page describes RESTful JSON APIs on `data.sec.gov` — `https://data.sec.gov/submissions/CIK##########.json` plus the XBRL `companyconcept`, `companyfacts`, and `frames` APIs, no authentication required, with a declared User-Agent and a 10-requests-per-second fair-access ceiling. Calling the endpoint returned HTTP 200 with JSON naming "Core Natural Resources, Inc.", ticker CNR, and the former name "CONSOL Energy Inc." through 2025-01-10.

## Common Properties

- [Website](https://corenaturalresources.com/)
- [Legacy Website](https://www.consol-energy.com)
- [Suppliers](https://corenaturalresources.com/suppliers/)
- [Investors](https://corenaturalresources.com/investors/)
- [News & Media](https://corenaturalresources.com/news-media/)
- [Sustainability](https://corenaturalresources.com/sustainability/)
- [Careers](https://corenaturalresources.com/careers/)
- [Contact](https://corenaturalresources.com/contact-us/)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
