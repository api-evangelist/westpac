---
name: westpac-browse-products
description: >-
  List and inspect Westpac's openly offered banking products via the public,
  unauthenticated CDR Product Reference Data API: filter the catalogue, page
  through results, then pull full fee, rate and eligibility detail for one product.
api: openapi/westpac-banking-products-api-openapi.yml
operations:
  - listBankingProducts
  - getBankingProductDetail
---

# Browse Westpac banking products

Base URL: `https://digital-api.westpac.com.au/cds-au/v1`. No API key or OAuth;
the only required header is `x-v` (endpoint version, optional `x-min-v`). An
unsupported version returns `406 Not Acceptable`.

1. `listBankingProducts` — `GET /banking/products`. Filter with `effective`,
   `updated-since`, `brand`, `product-category`; page with `page` / `page-size`
   and follow `links.next` until absent (`meta.totalPages`).
2. `getBankingProductDetail` — `GET /banking/products/{productId}` for a
   `productId` from step 1: fees, deposit/lending rates, features, constraints,
   eligibility.

Rules: read-only GETs, so no idempotency keys. Errors use the Consumer Data
Standards `errors[]` envelope (`code`, `title`, `detail`), not problem+json.
