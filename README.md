# Westpac Banking Corporation (westpac)

Westpac Banking Corporation is Australia's oldest bank and company, founded in 1817 as the Bank of New South Wales, and is one of the country's "Big Four" banks. Headquartered in Sydney, it is a publicly listed company on the Australian Securities Exchange (ASX:WBC) — not a customer-owned mutual — and operates a multi-brand group that includes St.George, BankSA, Bank of Melbourne, and RAMS. As an authorised deposit-taking institution (ADI), Westpac is a designated data holder under Australia's Consumer Data Right (CDR / Open Banking) and exposes a public, unauthenticated Product Reference Data (PRD) API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/westpac/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/westpac/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Product Reference Data
- ADI

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Westpac Banking Corporation CDR Product Reference Data API

Public, unauthenticated Product Reference Data (PRD) API exposing Westpac's banking product catalogue (rates, fees, features, eligibility) under Australia's Consumer Data Right. Confirmed live returning HTTP 200 with a `data.products` array — 64 total product records across Westpac Group brands — served at supported version `x-v: 5`. No security or other headers are required to call this API. Conforms to the DSB Consumer Data Standards Get Products / Get Product Detail contract.

- **Human URL:** [https://www.westpac.com.au/about-westpac/innovation/open-banking/product-api/](https://www.westpac.com.au/about-westpac/innovation/open-banking/product-api/)
- **Base URL:** `https://digital-api.westpac.com.au/cds-au/v1/banking/products`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Australia

#### Properties

- [Documentation](https://www.westpac.com.au/about-westpac/innovation/open-banking/product-api/)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/) — Consumer Data Standards (DSB)
- [OpenAPI](openapi/westpac-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.westpac.com.au/)
- [Developer Portal](https://www.westpac.com.au/about-westpac/innovation/open-banking/)
- [Documentation](https://www.westpac.com.au/about-westpac/innovation/open-banking/product-api/)
- [GitHub Organization](https://github.com/westpac)
- [LinkedIn](https://www.linkedin.com/company/westpac)
- [Privacy Policy](https://www.westpac.com.au/privacy/privacy-statement/)
- [Terms of Service (CDR Policy)](https://www.westpac.com.au/content/dam/public/wbc/documents/pdf/aw/WBC_CDR_Policy.pdf)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
