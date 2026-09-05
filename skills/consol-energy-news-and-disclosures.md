---
name: consol-energy-news-and-disclosures
description: Retrieve Core Natural Resources (formerly CONSOL Energy) news releases, article series, corporate pages and published PDF disclosures from the company's public content API.
api: openapi/consol-energy-news-content-api-openapi.yml
operations: [listArticles, getArticle, listNewsSeriesTitles, listPages, listMedia, searchContent]
---

# News releases and published disclosures — Core Natural Resources

Base URL: `https://corenaturalresources.com/wp-json`. Anonymous, read-only.

## Steps

1. `listNewsSeriesTitles` — `GET /wp/v2/news-series-title?per_page=100` to see how
   the company groups its 40 articles into 9 series.
2. `listArticles` — `GET /wp/v2/article?per_page=100&_fields=id,date,slug,link,title,news-series-title`.
   Narrow by date with `?after=2026-01-01T00:00:00` (ISO 8601), by series with
   `?news-series-title=<term id>`, or sort with `?orderby=date&order=desc`.
3. `getArticle` — `GET /wp/v2/article/{id}` for the rendered body of one release.
4. `listPages` — `GET /wp/v2/pages?per_page=100&_fields=id,slug,link,title` for the
   22 corporate pages (investors, suppliers, sustainability, careers, contact).
5. `listMedia` — `GET /wp/v2/media?per_page=100&_fields=id,date,slug,source_url,title,mime_type`
   for the 173-item library. This is where the supplier terms and conditions,
   the Supplier Code of Conduct, and the sustainability and safety PDFs live as
   addressable files; filter client-side on `mime_type == "application/pdf"`.
6. `searchContent` — `GET /wp/v2/search?search=<terms>&subtype=article,page,mine,leader`
   when you do not know which type holds the thing you want.

## Rules

- Same pagination, error and stability rules as `consol-energy-mine-roster`.
- `/wp/v2/posts` is registered but empty (`X-WP-Total: 0`) — editorial content is
  in the `article` type. Do not conclude the site has no news from an empty
  `posts` collection.
- Financial data is NOT here. Filings for this registrant come from the SEC's own
  EDGAR APIs — `https://data.sec.gov/submissions/CIK0001710366.json` — which
  require a declared `User-Agent` and cap at 10 requests/second.
- Nothing on this host is a regulatory disclosure of record. Cite the PDF or the
  SEC filing, not the JSON representation.
