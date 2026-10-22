---
name: westpac-review-payment-commitments
description: >-
  For an Accredited Data Recipient holding customer consent: list a Westpac
  customer's saved payees, direct-debit authorisations, scheduled payments and
  instalment plans via the CDR Banking APIs.
api: openapi/westpac-banking-payees-api-openapi.yml
operations:
  - listBankingPayees
  - getBankingPayeeDetail
  - listDirectDebitsBulk
  - listDirectDebits
  - listScheduledPaymentsBulk
  - listScheduledPayments
  - listInstalmentPlansBulk
  - listInstalmentPlans
---

# Review payment commitments (CDR, gated)

**Gated**, like all CDR consumer-data endpoints: you need an Accredited Data
Recipient consent token (OAuth 2.0 / OIDC FAPI) over mTLS, plus the `x-v` header.

1. `listBankingPayees` — `GET /banking/payees`; `getBankingPayeeDetail` for one `payeeId`.
2. `listDirectDebitsBulk` — `GET /banking/accounts/direct-debits`, or
   `listDirectDebits` for one `accountId`.
3. `listScheduledPaymentsBulk` — `GET /banking/payments/scheduled`, or
   `listScheduledPayments` for one account.
4. `listInstalmentPlansBulk` — `GET /banking/accounts/payments/plans`, or
   `listInstalmentPlans` for one account.

Specs: payees, direct-debits, and scheduled-payments contracts under `openapi/`.
The POST variants (`...SpecificAccounts`) are read queries that take a body of
account IDs. They do not change any data. Errors use the CDS `errors[]` envelope.
