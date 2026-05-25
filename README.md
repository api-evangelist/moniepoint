# Moniepoint (moniepoint)

Moniepoint is Africa's all-in-one financial platform for small and medium-sized businesses and individuals — Nigeria's largest merchant acquirer, with about 10 million business and individual accounts, $17B in monthly transaction volume, and 26M daily payments processed. Founded as TeamApt and rebranded under the Moniepoint name, the company became Africa's most valuable fintech unicorn after a 2024 raise led by Google, then expanded into Kenya and cross-border payments. The Monnify developer platform exposes the rails to third parties through a comprehensive REST API for authentication, collections, disbursements, sub-accounts and settlement, direct-debit mandates, invoices, bills payment, KYC verification, wallets, refunds, and signed webhooks; the separate Moniepoint POS API enables push payments to registered terminals.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/moniepoint/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Africa, Nigeria, Payments, Banking, Fintech, Acquiring, POS, Collections, Disbursements, Virtual Accounts, Direct Debit, Bills Payment, SMB, Working Capital, Unicorn

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## Platform At A Glance

| Metric | Value |
|---|---|
| Business & individual accounts | ~10 million |
| Monthly transaction volume | $17 billion |
| Daily payments processed | 26 million |
| Peak API throughput | 200M calls / minute |
| Primary market | Nigeria (largest merchant acquirer) |
| Secondary market | Kenya |
| Developer brand | Monnify |
| Production base URL | `https://api.monnify.com` |
| Sandbox base URL | `https://sandbox.monnify.com` |
| POS API base URL | `https://pos.moniepoint.com` |
| Auth | Basic `apiKey:secretKey` to `/api/v1/auth/login` then Bearer `accessToken` (1h TTL) |
| Response envelope | `{ requestSuccessful, responseMessage, responseCode, responseBody }` |
| Webhook signature | `monnify-signature` header = HMAC-SHA-512(clientSecret, stringifiedBody) |

## APIs

### Monnify Authentication API
Exchange Monnify API key + secret credentials (Basic auth) for a short-lived Bearer access token via `POST /api/v1/auth/login`. Cache the `accessToken` until expiry.

**Human URL:** [https://developers.monnify.com/docs/getting-started/authentication](https://developers.monnify.com/docs/getting-started/authentication)

- [OpenAPI](openapi/monnify-authentication-api-openapi.yml)
- [Naftiko Capability — Login](capabilities/authentication-login.yaml)

### Monnify Collections API
Initialize one-time payment transactions, accept card payments with 3-D Secure / OTP, charge tokenized cards, complete bank-transfer payments, and look up transaction status.

**Human URL:** [https://developers.monnify.com/docs/collections](https://developers.monnify.com/docs/collections)

- [OpenAPI](openapi/monnify-collections-api-openapi.yml)
- [JSON Schema — Transaction](json-schema/monnify-transaction-schema.json)
- [JSON-LD](json-ld/moniepoint-context.jsonld)
- [Naftiko Capability — Transactions](capabilities/collections-transactions.yaml)
- [Naftiko Capability — Cards](capabilities/collections-cards.yaml)

### Monnify Reserved Accounts API
Provision permanent NUBAN virtual accounts (dedicated and invoice variants) for customers, with income-split routing, KYC updates (BVN / NIN), allowed-source restrictions, deallocation, transaction history, and per-account limit profiles. V2 endpoints under `/api/v2/bank-transfer/reserved-accounts/`.

**Human URL:** [https://developers.monnify.com/docs/collections/customer-reserved-account](https://developers.monnify.com/docs/collections/customer-reserved-account)

- [OpenAPI](openapi/monnify-reserved-accounts-api-openapi.yml)
- [JSON Schema — Reserved Account](json-schema/monnify-reserved-account-schema.json)
- [Naftiko Capability — Reserved Accounts](capabilities/reserved-accounts-accounts.yaml)
- [Naftiko Capability — Limit Profiles](capabilities/reserved-accounts-limits.yaml)

### Monnify Disbursements API
Initiate single and bulk NIP transfers with two-factor OTP authorization, wallet-balance lookup, transfer status, list/search, and resend-OTP. Since April 2026, the flow follows Name Inquiry → Disbursement Request and requires a verified beneficiary account name. `senderInformation` supported since October 2025.

**Human URL:** [https://developers.monnify.com/docs/disbursements](https://developers.monnify.com/docs/disbursements)

- [OpenAPI](openapi/monnify-disbursements-api-openapi.yml)
- [JSON Schema — Transfer](json-schema/monnify-transfer-schema.json)
- [Naftiko Capability — Single Transfers](capabilities/disbursements-single.yaml)
- [Naftiko Capability — Bulk Transfers](capabilities/disbursements-bulk.yaml)

### Monnify Sub-Accounts API
Create and manage settlement sub-accounts for marketplaces, franchises, and multi-tenant platforms. Settlement bank, split percentage, default flag, per-call income-split configuration.

**Human URL:** [https://developers.monnify.com/docs/sub-accounts](https://developers.monnify.com/docs/sub-accounts)

- [OpenAPI](openapi/monnify-sub-accounts-api-openapi.yml)
- [Naftiko Capability — Sub-Accounts](capabilities/sub-accounts-sub-accounts.yaml)

### Monnify Direct Debit API
Create, activate, and debit recurring NIBSS direct-debit mandates. Smart routing uses TeamApt as primary processor with NIBSS as fallback. `incomeSplit` supported on mandate-debit (April 2026).

**Human URL:** [https://developers.monnify.com/docs/direct-debit](https://developers.monnify.com/docs/direct-debit)

- [OpenAPI](openapi/monnify-direct-debit-api-openapi.yml)
- [Naftiko Capability — Mandates](capabilities/direct-debit-mandates.yaml)
- [Naftiko Capability — Debits](capabilities/direct-debit-debit.yaml)

### Monnify Invoices API
Create static and dynamic invoices that generate hosted payment pages and unique reserved accounts. Supports listing, status lookup, and cancellation.

**Human URL:** [https://developers.monnify.com/docs/invoices](https://developers.monnify.com/docs/invoices)

- [OpenAPI](openapi/monnify-invoices-api-openapi.yml)
- [Naftiko Capability — Invoices](capabilities/invoices-invoices.yaml)

### Monnify Bills Payment API
Unified Biller Service for airtime, data, electricity, cable TV, betting, and education. List categories, billers, biller items; validate customer; process bill; check status.

**Human URL:** [https://developers.monnify.com/docs/bills-payment](https://developers.monnify.com/docs/bills-payment)

- [OpenAPI](openapi/monnify-bills-payment-api-openapi.yml)
- [Naftiko Capability — Bills](capabilities/bills-payment-bills.yaml)

### Monnify Verification API
Validate Nigerian bank account numbers (Name Inquiry), match BVN to bank account, and verify NIN. Critical for KYC, disbursement beneficiary checks, and fraud prevention.

**Human URL:** [https://developers.monnify.com/docs/verification](https://developers.monnify.com/docs/verification)

- [OpenAPI](openapi/monnify-verification-api-openapi.yml)
- [Naftiko Capability — Verification](capabilities/verification-verifications.yaml)

### Monnify Wallets API
Create wallets and sub-wallets, query main and disbursement balances, list transactions, and pull statements.

**Human URL:** [https://developers.monnify.com/docs/wallets](https://developers.monnify.com/docs/wallets)

- [OpenAPI](openapi/monnify-wallets-api-openapi.yml)
- [Naftiko Capability — Wallets](capabilities/wallets-wallets.yaml)

### Monnify Refunds API
Initiate full or partial refunds against a successful collection, list refunds, and look up refund status. Emits `successful_refund` / `failed_refund` webhooks.

**Human URL:** [https://developers.monnify.com/docs/refunds](https://developers.monnify.com/docs/refunds)

- [OpenAPI](openapi/monnify-refunds-api-openapi.yml)
- [Naftiko Capability — Refunds](capabilities/refunds-refunds.yaml)

### Monnify Settlements API
Retrieve settlement information for collected funds — settlement batches per merchant or sub-account, settlement transactions, and settlement bank details.

**Human URL:** [https://developers.monnify.com/docs/settlements](https://developers.monnify.com/docs/settlements)

- [OpenAPI](openapi/monnify-settlements-api-openapi.yml)
- [Naftiko Capability — Settlements](capabilities/settlements-settlements.yaml)

### Monnify Webhooks
Asynchronous notifications for nine event categories — successful collection, successful / failed / reversed disbursement, successful / failed refund, settlement completion, mandate status change, wallet activity, and `low_balance_alert` (added September 2025). HMAC-SHA-512 signature in the `monnify-signature` header.

**Human URL:** [https://developers.monnify.com/docs/webhooks](https://developers.monnify.com/docs/webhooks)

- [JSON Schema — Webhook](json-schema/monnify-webhook-schema.json)

### Moniepoint POS Push Payment API
Push payment-request flow for Moniepoint POS terminals. ISV partners send an authenticated push to a registered terminal serial number; the merchant taps to accept and the terminal completes a card or transfer collection routed through Moniepoint's acquiring rails.

**Human URL:** [https://docs.pos.moniepoint.com](https://docs.pos.moniepoint.com)

- [OpenAPI](openapi/moniepoint-pos-api-openapi.yml)
- [Naftiko Capability — Push Payment](capabilities/pos-push-payment.yaml)

## Common Properties

- [Portal — moniepoint.com](https://moniepoint.com)
- [Portal — Monnify Developer Portal](https://developers.monnify.com)
- [Documentation — Monnify API Reference](https://developers.monnify.com/api)
- [Documentation — Moniepoint POS API](https://docs.pos.moniepoint.com)
- [Documentation — Monnify Confluence Archive](https://teamapt.atlassian.net/wiki/spaces/MON/pages)
- [Documentation — POS Developer Support (Confluence)](https://teamapt.atlassian.net/wiki/spaces/EI/pages)
- [GettingStarted](https://developers.monnify.com/docs/getting-started)
- [ChangeLog](https://developers.monnify.com/docs/change-logs)
- [Blog — Monnify Developer Blog](https://developers.monnify.com/blog)
- [Blog — Moniepoint Engineering](https://engineering.moniepoint.com)
- [Blog — moniepoint.com/blog](https://moniepoint.com/blog)
- [Press](https://moniepoint.com/press)
- [Support](https://support.moniepoint.com)
- [Training — Learning Centre](https://learning.moniepoint.com)
- [TrustCenter](https://trust.moniepoint.com)
- [PrivacyPolicy](https://moniepoint.com/ng/privacy-policy)
- [TermsOfService](https://moniepoint.com/ng/terms-of-service)
- [SignUp — Monnify](https://app.monnify.com/create-account)
- [SignUp — Moniepoint Business](https://app.moniepoint.com/signup)
- [Sandbox — sandbox.monnify.com](https://sandbox.monnify.com)
- [GitHubOrganization](https://github.com/Moniepoint)
- [LinkedIn](https://www.linkedin.com/company/moniepoint)
- [Twitter](https://twitter.com/moniepointNG)
- [Careers](https://moniepoint.com/careers)
- [Webhooks](https://developers.monnify.com/docs/webhooks)
- [Errors](https://developers.monnify.com/docs/getting-started/errors)
- [Authentication](https://developers.monnify.com/docs/getting-started/authentication)
- [RateLimits](https://developers.monnify.com/docs/rate-limits)
- [Versioning](https://developers.monnify.com/docs/getting-started/versioning)
- [SDK — dart-flow](https://github.com/Moniepoint/dart-flow)
- [SDK — MonnifyEase (community)](https://github.com/cla-bit/MonnifyEase)
- [SDK — Laravel Monnify (community)](https://github.com/abdsalam/laravel-monnify)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Monnify Authentication API](openapi/monnify-authentication-api-openapi.yml)
- [Monnify Collections API](openapi/monnify-collections-api-openapi.yml)
- [Monnify Reserved Accounts API](openapi/monnify-reserved-accounts-api-openapi.yml)
- [Monnify Disbursements API](openapi/monnify-disbursements-api-openapi.yml)
- [Monnify Sub-Accounts API](openapi/monnify-sub-accounts-api-openapi.yml)
- [Monnify Direct Debit API](openapi/monnify-direct-debit-api-openapi.yml)
- [Monnify Invoices API](openapi/monnify-invoices-api-openapi.yml)
- [Monnify Bills Payment API](openapi/monnify-bills-payment-api-openapi.yml)
- [Monnify Verification API](openapi/monnify-verification-api-openapi.yml)
- [Monnify Wallets API](openapi/monnify-wallets-api-openapi.yml)
- [Monnify Refunds API](openapi/monnify-refunds-api-openapi.yml)
- [Monnify Settlements API](openapi/monnify-settlements-api-openapi.yml)
- [Moniepoint POS Push Payment API](openapi/moniepoint-pos-api-openapi.yml)

### JSON Schema

- [Monnify Transaction](json-schema/monnify-transaction-schema.json)
- [Monnify Reserved Account](json-schema/monnify-reserved-account-schema.json)
- [Monnify Transfer](json-schema/monnify-transfer-schema.json)
- [Monnify Webhook](json-schema/monnify-webhook-schema.json)

### JSON-LD

- [Moniepoint Context](json-ld/moniepoint-context.jsonld)

### Capabilities (Naftiko)

- [Authentication — Login](capabilities/authentication-login.yaml)
- [Collections — Transactions](capabilities/collections-transactions.yaml)
- [Collections — Cards](capabilities/collections-cards.yaml)
- [Reserved Accounts — Accounts](capabilities/reserved-accounts-accounts.yaml)
- [Reserved Accounts — Limit Profiles](capabilities/reserved-accounts-limits.yaml)
- [Disbursements — Single Transfers](capabilities/disbursements-single.yaml)
- [Disbursements — Bulk Transfers](capabilities/disbursements-bulk.yaml)
- [Sub-Accounts](capabilities/sub-accounts-sub-accounts.yaml)
- [Direct Debit — Mandates](capabilities/direct-debit-mandates.yaml)
- [Direct Debit — Debits](capabilities/direct-debit-debit.yaml)
- [Invoices](capabilities/invoices-invoices.yaml)
- [Bills Payment](capabilities/bills-payment-bills.yaml)
- [Verification](capabilities/verification-verifications.yaml)
- [Wallets](capabilities/wallets-wallets.yaml)
- [Refunds](capabilities/refunds-refunds.yaml)
- [Settlements](capabilities/settlements-settlements.yaml)
- [POS — Push Payment](capabilities/pos-push-payment.yaml)

### Examples

- [Initialize Transaction](examples/monnify-initialize-transaction-example.json)
- [Reserve A Customer Account (V2)](examples/monnify-reserve-account-example.json)
- [Initiate Single Transfer](examples/monnify-single-transfer-example.json)
- [Successful Collection Webhook](examples/monnify-webhook-successful-collection-example.json)
- [POS Push Payment Request](examples/moniepoint-push-payment-example.json)

### Commercial artifacts

- [Plans / Pricing](plans/moniepoint-plans-pricing.yml)
- [Rate Limits](rate-limits/moniepoint-rate-limits.yml)
- [FinOps Definition](finops/moniepoint-finops.yml)

### Governance

- [Spectral Rules](rules/moniepoint-rules.yml)
- [Vocabulary](vocabulary/moniepoint-vocabulary.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
