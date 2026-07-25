# CONSOL Energy (consol-energy)

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
