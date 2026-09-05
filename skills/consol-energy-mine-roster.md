---
name: consol-energy-mine-roster
description: Pull the Core Natural Resources (formerly CONSOL Energy) mine roster and its East/West grouping from the company's public content API.
api: openapi/consol-energy-mines-content-api-openapi.yml
operations: [listMines, getMine, listMineLocations, getMineLocation]
---

# Mine roster — Core Natural Resources (formerly CONSOL Energy)

The company publishes no developer portal. The only first-party machine-readable
surface is the WordPress REST API on its corporate host. It is read-only and
anonymous — do not look for a key, there is none.

Base URL: `https://corenaturalresources.com/wp-json`

## Steps

1. `listMineLocations` — `GET /wp/v2/mine-location?per_page=100`.
   Two terms exist (East, West). Keep the `id` of each; that is what filters mines.
2. `listMines` — `GET /wp/v2/mine?per_page=100&_fields=id,slug,link,title,mine-location`.
   11 records. `_fields` keeps the payload small; without it each record carries
   rendered HTML content. To scope to one region, add `&mine-location=<term id>`.
3. `getMine` — `GET /wp/v2/mine/{id}` for the full profile of a single mine,
   including rendered content and `_links`.

## Rules

- Read `X-WP-Total` and `X-WP-TotalPages` from the response headers, and follow
  `Link: rel="next"`, rather than incrementing `page` blindly: `page` beyond the
  last page returns HTTP 400 `rest_post_invalid_page_number`.
- `per_page` is capped at 100. Asking for more returns HTTP 400 `rest_invalid_param`.
- There is no rate-limit header of any kind and no published limit. Be
  conservative — this is a corporate marketing site, not a metered API.
- Errors are NOT RFC 9457. Parse `{code, message, data.status}`; see
  `errors/consol-energy-problem-types.yml`.
- Do not attempt writes. `/wp/v2/settings` and `/wp/v2/users` return HTTP 401,
  and every write route needs a WordPress credential the company does not issue.
- Treat the surface as unstable: it is a CMS side effect, not a product. There is
  no deprecation policy, no Sunset header and no status page — a plugin change
  can remove a route without notice.
