# Westpac Banking Corporation (westpac)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
