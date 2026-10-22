---
name: westpac-review-account-activity
description: >-
  For an Accredited Data Recipient holding customer consent: list a Westpac
  customer's accounts, read balances, then list and inspect transactions via
  the CDR Banking APIs.
api: openapi/westpac-banking-accounts-api-openapi.yml
operations:
  - listBankingAccounts
  - getBankingAccountDetail
  - listBankingBalancesBulk
  - getBankingBalance
  - listBankingTransactions
  - getBankingTransactionDetail
---

# Review account activity (CDR, gated)

**Gated.** These are Consumer Data Right consumer-data endpoints. They can be
called only by an Accredited Data Recipient, using a customer consent token
(OAuth 2.0 / OIDC, FAPI profile) over mutual TLS. An arbitrary agent cannot call them.
Send `x-v`, plus the `x-fapi-*` headers the contract defines.

1. `listBankingAccounts` — `GET /banking/accounts` (filters `product-category`,
   `open-status`, `is-owned`; paginate with `page` / `page-size`).
2. `getBankingAccountDetail` — `GET /banking/accounts/{accountId}`.
3. `listBankingBalancesBulk` — `GET /banking/accounts/balances`, or
   `getBankingBalance` — `GET /banking/accounts/{accountId}/balance` for one account.
4. `listBankingTransactions` — `GET /banking/accounts/{accountId}/transactions`,
   then `getBankingTransactionDetail` for a single `transactionId`.

Specs: accounts, balances (`westpac-banking-account-balances-api-openapi.yml`),
transactions (`westpac-banking-account-transactions-api-openapi.yml`). Read-only;
errors use the CDS `errors[]` envelope.
