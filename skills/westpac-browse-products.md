---
name: Browse Westpac banking products
description: >-
  List and inspect Westpac's openly offered banking products via the public,
  unauthenticated CDR Product Reference Data API — filter the catalogue, page
  through results, then pull full fee and rate detail for a chosen product.
api: openapi/westpac-cds-banking-products-openapi.yml
operations:
  - listProducts
  - getProductDetail
---

# Browse Westpac banking products

This skill uses Westpac's public **Consumer Data Right Product Reference Data**
API. It is **unauthenticated** — no API key, token, or OAuth. The only required
header is the CDS version header.

Base URL: `https://digital-api.westpac.com.au/cds-au/v1`

## Rules

- Always send the header **`x-v: 5`**. Westpac serves versions 4 and 5; older
  versions (e.g. `3`) return HTTP `406` `UnsupportedVersion`.
- These are safe, read-only `GET` calls. There is no idempotency key and no
  state change.
- Errors come back as a CDS `errors[]` array (`{code, title, detail}`), not
  RFC 9457 problem+json.

## Steps

1. **List products** — call `listProducts`:
   `GET /banking/products` with `x-v: 5`.
   Optional filters: `effective` (`CURRENT`|`FUTURE`|`ALL`), `updated-since`,
   `brand`, `product-category` (e.g. `RESIDENTIAL_MORTGAGES`,
   `TRANS_AND_SAVINGS_ACCOUNTS`, `CRED_AND_CHRG_CARDS`, `TERM_DEPOSITS`).
   Paginate with `page` and `page-size` (default 25). Read `meta.totalRecords`
   and `meta.totalPages` to know how far to page. Each item carries a
   `productId`.

2. **Get product detail** — for a `productId` of interest, call
   `getProductDetail`: `GET /banking/products/{productId}` with `x-v: 5`.
   The `data` object adds `fees`, `depositRates`, `lendingRates` (with tiered
   `tiers`), `features`, `constraints`, `eligibility`, and `bundles`.

3. **Interpret rates and fees** — lending/deposit rates carry a
   `rate` (RateString) plus `lendingRateType`/`depositRateType`; fees carry
   `feeType` and one of `amount`/`balanceRate`/`transactionRate`/`accruedRate`.
   Currency defaults to `AUD` when absent.

## Notes

- The catalogue spans Westpac Group brands; use the `brand` filter or the
  `brand`/`brandName` fields on each product to separate them.
- Consumer/account data beyond this product catalogue is **not** available here —
  it requires CDR Accredited Data Recipient accreditation and the consent flow.
