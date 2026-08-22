# Moniepoint (moniepoint)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Moniepoint is Africa's all-in-one financial platform for small and medium-sized businesses and individuals — Nigeria's largest merchant acquirer, with about 10 million business and individual accounts, $17B in monthly transaction volume, and 26M daily payments processed. Founded as TeamApt and rebranded under the Moniepoint name, the company became Africa's most valuable fintech unicorn after a 2024 raise led by Google, then expanded into Kenya and cross-border payments. The Monnify developer platform exposes the rails to third parties through a comprehensive REST API for authentication, collections (cards, bank transfer, USSD, reserved accounts), disbursements (single and bulk NIP), sub-accounts and settlement, direct-debit mandates, invoices, bills payment, KYC verification, wallets, refunds, and signed webhooks; the separate Moniepoint POS API enables push payments to registered terminals. Underlying products also include business bank accounts, working-capital credit, expense cards, and business-management tools.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/moniepoint/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/moniepoint/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Africa
- Nigeria
- Payments
- Banking
- Fintech
- Acquiring
- POS
- Collections
- Disbursements
- Virtual Accounts
- Direct Debit
- Bills Payment
- SMB
- Working Capital
- Unicorn

## Timestamps

- **Created:** 2026-05-24T00:00:00.000Z
- **Modified:** 2026-05-24

## APIs

### Monnify Authentication API

Exchange Monnify API key and secret credentials (Basic auth) for a short-lived Bearer access token via POST /api/v1/auth/login. The returned accessToken plus expiresIn drives every other Monnify API call. Tokens expire after one hour and must be re-issued; client code typically caches and refreshes on demand.

- **Human URL:** [https://developers.monnify.com/docs/getting-started/authentication](https://developers.monnify.com/docs/getting-started/authentication)

#### Tags

- Authentication
- OAuth
- Tokens

#### Properties

- [Documentation](https://developers.monnify.com/docs/getting-started/authentication)
- [OpenAPI](openapi/monnify-authentication-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-authentication-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-authentication-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Collections API

Initialize one-time payment transactions, accept card payments with 3-D Secure / OTP authorization, charge tokenized cards, complete bank-transfer payments, and look up transaction status. Powers the Monnify Checkout, server-to-server card capture, and pay-with-transfer flows used by Nigerian merchants. Endpoints under /api/v1/merchant/transactions/ and /api/v1/sdk/transactions/.

- **Human URL:** [https://developers.monnify.com/docs/collections](https://developers.monnify.com/docs/collections)

#### Tags

- Collections
- Payments
- Cards
- Bank Transfer
- USSD
- QR

#### Properties

- [Documentation](https://developers.monnify.com/docs/collections)
- [OpenAPI](openapi/monnify-collections-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-collections-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-collections-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/monnify-transaction-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/moniepoint-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Monnify Reserved Accounts API

Programmatically provision permanent NUBAN virtual accounts (dedicated and one-time invoice variants) for customers and merchants. Supports income-split configuration to multiple sub-accounts, KYC updates (BVN / NIN), allowed-source-account restriction, deallocation, transaction history, and per-account limit profiles. V2 endpoints under /api/v2/bank-transfer/reserved-accounts/.

- **Human URL:** [https://developers.monnify.com/docs/collections/customer-reserved-account](https://developers.monnify.com/docs/collections/customer-reserved-account)

#### Tags

- Reserved Accounts
- Virtual Accounts
- Bank Transfer
- KYC
- Limits

#### Properties

- [Documentation](https://developers.monnify.com/docs/collections/customer-reserved-account)
- [OpenAPI](openapi/monnify-reserved-accounts-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-reserved-accounts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-reserved-accounts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/monnify-reserved-account-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Monnify Disbursements API

Initiate single and bulk NIP transfers to any Nigerian bank account, with two-factor OTP authorization, wallet-balance lookup, transfer status, list/search, and resend-OTP. As of April 2026 the request flow follows Name Inquiry → Disbursement Request and requires a verified beneficiary account name. Sender-information object supported since October 2025. Endpoints under /api/v2/disbursements/single, /api/v2/disbursements/bulk, /api/v2/disbursements/wallet-balance.

- **Human URL:** [https://developers.monnify.com/docs/disbursements](https://developers.monnify.com/docs/disbursements)

#### Tags

- Disbursements
- Transfers
- Payouts
- NIP
- Bulk

#### Properties

- [Documentation](https://developers.monnify.com/docs/disbursements)
- [Documentation](https://developers.monnify.com/docs/disbursements/single-transfers)
- [Documentation](https://developers.monnify.com/docs/disbursements/bulk-transfers)
- [OpenAPI](openapi/monnify-disbursements-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-disbursements-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-disbursements-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/monnify-transfer-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Monnify Sub-Accounts API

Create and manage settlement sub-accounts representing third parties that should receive a configured percentage of each transaction (marketplaces, multi-tenant platforms, franchise networks). Settlement bank, split percentage, default flag, and per-call income-split configuration. Endpoints under /api/v1/sub-accounts.

- **Human URL:** [https://developers.monnify.com/docs/sub-accounts](https://developers.monnify.com/docs/sub-accounts)

#### Tags

- Sub-Accounts
- Settlement
- Split Payments

#### Properties

- [Documentation](https://developers.monnify.com/docs/sub-accounts)
- [OpenAPI](openapi/monnify-sub-accounts-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-sub-accounts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-sub-accounts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Direct Debit API

Create, activate, and debit recurring NIBSS direct-debit mandates against a customer's bank account. Smart routing uses TeamApt as the primary processor with NIBSS as fallback for improved success rates. Supports incomeSplit on mandate-debit to settle into multiple sub-accounts. Endpoints under /api/v1/direct-debit/mandate/ and /api/v1/direct-debit/mandate/debit.

- **Human URL:** [https://developers.monnify.com/docs/direct-debit](https://developers.monnify.com/docs/direct-debit)

#### Tags

- Direct Debit
- Mandates
- Recurring Payments
- NIBSS

#### Properties

- [Documentation](https://developers.monnify.com/docs/direct-debit)
- [OpenAPI](openapi/monnify-direct-debit-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-direct-debit-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-direct-debit-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Invoices API

Create static and dynamic invoices that generate hosted payment pages and unique reserved accounts. Supports invoice listing, status lookup, and cancellation. Backs Monnify's invoicing dashboard and embedded invoicing in business-management apps. Endpoints under /api/v1/invoice.

- **Human URL:** [https://developers.monnify.com/docs/invoices](https://developers.monnify.com/docs/invoices)

#### Tags

- Invoices
- Billing
- Static
- Dynamic

#### Properties

- [Documentation](https://developers.monnify.com/docs/invoices)
- [OpenAPI](openapi/monnify-invoices-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-invoices-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-invoices-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Bills Payment API

Unified Biller Service for purchasing airtime and data, paying electricity and cable-TV bills, funding betting wallets, and paying education fees. List categories, billers, and biller items; validate the customer; process the bill; check status. Endpoints under /api/v1/bill-payment/.

- **Human URL:** [https://developers.monnify.com/docs/bills-payment](https://developers.monnify.com/docs/bills-payment)

#### Tags

- Bills
- Airtime
- Data
- Electricity
- Cable TV
- Betting

#### Properties

- [Documentation](https://developers.monnify.com/docs/bills-payment)
- [OpenAPI](openapi/monnify-bills-payment-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-bills-payment-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-bills-payment-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Verification API

Validate a Nigerian bank account number (Name Inquiry), match a Bank Verification Number (BVN) against an account, and verify National Identification Numbers (NIN). Critical for KYC, disbursement beneficiary checks, and fraud prevention. Endpoints under /api/v1/disbursements/account/validate, /api/v1/vas/bvn-account-match, and /api/v1/vas/verify-nin.

- **Human URL:** [https://developers.monnify.com/docs/verification](https://developers.monnify.com/docs/verification)

#### Tags

- Verification
- BVN
- NIN
- Bank Account
- KYC

#### Properties

- [Documentation](https://developers.monnify.com/docs/verification)
- [OpenAPI](openapi/monnify-verification-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-verification-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-verification-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Wallets API

Create wallets and sub-wallets, query main and disbursement balances, list transactions, and pull statements. Used to fund disbursement operations and to model end-user wallets for business-management products. Endpoints under /api/v1/disbursements/wallet-balance and /api/v1/disbursements/wallet.

- **Human URL:** [https://developers.monnify.com/docs/wallets](https://developers.monnify.com/docs/wallets)

#### Tags

- Wallets
- Balance
- Statements
- Sub-Wallets

#### Properties

- [Documentation](https://developers.monnify.com/docs/wallets)
- [OpenAPI](openapi/monnify-wallets-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-wallets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-wallets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Refunds API

Initiate full or partial refunds against a successful collection, list refunds, and look up refund status. Refund events emit successful_refund / failed_refund webhooks for asynchronous reconciliation. Endpoints under /api/v1/refunds.

- **Human URL:** [https://developers.monnify.com/docs/refunds](https://developers.monnify.com/docs/refunds)

#### Tags

- Refunds
- Reversals
- Disputes

#### Properties

- [Documentation](https://developers.monnify.com/docs/refunds)
- [OpenAPI](openapi/monnify-refunds-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-refunds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-refunds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Settlements API

Retrieve settlement information for collected funds — settlement batches per merchant or sub-account, settlement transactions, and settlement bank details. Backs reconciliation of daily settlement payouts into the merchant's external bank account. Endpoints under /api/v1/transactions/find-by-settlement-reference and /api/v1/settlements.

- **Human URL:** [https://developers.monnify.com/docs/settlements](https://developers.monnify.com/docs/settlements)

#### Tags

- Settlement
- Payouts
- Reporting

#### Properties

- [Documentation](https://developers.monnify.com/docs/settlements)
- [OpenAPI](openapi/monnify-settlements-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/monnify-settlements-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-settlements-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Monnify Webhooks

Asynchronous server-to-server notifications for nine event categories — successful collection, successful / failed / reversed disbursement, successful / failed refund, settlement completion, mandate status change, wallet activity, and low_balance_alert (added September 2025). Every payload includes a monnify-signature header computed as HMAC-SHA-512 of the stringified request body using the client secret. Standard envelope { eventType, eventData }.

- **Human URL:** [https://developers.monnify.com/docs/webhooks](https://developers.monnify.com/docs/webhooks)

#### Tags

- Webhooks
- Events
- HMAC
- SHA-512

#### Properties

- [Documentation](https://developers.monnify.com/docs/webhooks)
- [JSON Schema](json-schema/monnify-webhook-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Postman Collection](collections/moniepoint-pos-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/moniepoint-pos-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-authentication-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-authentication-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-bills-payment-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-bills-payment-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-collections-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-collections-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-direct-debit-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-direct-debit-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-disbursements-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-disbursements-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-invoices-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-invoices-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-refunds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-refunds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-reserved-accounts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-reserved-accounts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-settlements-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-settlements-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-sub-accounts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-sub-accounts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-verification-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-verification-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/monnify-wallets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/monnify-wallets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Moniepoint POS Push Payment API

Push payment-request flow for Moniepoint POS terminals. ISV partners send an authenticated push to a registered terminal serial number; the merchant taps to accept and the terminal completes a card or transfer collection routed through Moniepoint's acquiring rails. Authentication uses an API client ID / secret pair issued through the Moniepoint Business dashboard.

- **Human URL:** [https://docs.pos.moniepoint.com](https://docs.pos.moniepoint.com)

#### Tags

- POS
- Terminals
- Push Payments
- Acquiring

#### Properties

- [Documentation](https://docs.pos.moniepoint.com)
- [Documentation](https://teamapt.atlassian.net/wiki/spaces/EI/pages/1039826999/Push+Payment+Request+API+Reference)
- [Documentation](https://teamapt.atlassian.net/wiki/spaces/EI/pages/1042120729/API+Client+Credentials)
- [OpenAPI](openapi/moniepoint-pos-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/moniepoint-pos-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/moniepoint-pos-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://moniepoint.com)
- [Portal](https://developers.monnify.com)
- [Documentation](https://developers.monnify.com/api)
- [Documentation](https://docs.pos.moniepoint.com)
- [Documentation](https://teamapt.atlassian.net/wiki/spaces/MON/pages)
- [Documentation](https://teamapt.atlassian.net/wiki/spaces/EI/pages)
- [Getting Started](https://developers.monnify.com/docs/getting-started)
- [Changelog](https://developers.monnify.com/docs/change-logs)
- [Blog](https://developers.monnify.com/blog)
- [Blog](https://engineering.moniepoint.com)
- [Blog](https://moniepoint.com/blog)
- [Press](https://moniepoint.com/press)
- [Support](https://support.moniepoint.com)
- [Training](https://learning.moniepoint.com)
- [Trust Center](https://trust.moniepoint.com)
- [Privacy Policy](https://moniepoint.com/ng/privacy-policy)
- [Terms of Service](https://moniepoint.com/ng/terms-of-service)
- [Sign Up](https://app.monnify.com/create-account)
- [Sign Up](https://app.moniepoint.com/signup)
- [Sandbox](https://sandbox.monnify.com)
- [GitHub Organization](https://github.com/Moniepoint)
- [LinkedIn](https://www.linkedin.com/company/moniepoint)
- [Twitter](https://twitter.com/moniepointNG)
- [Careers](https://moniepoint.com/careers)
- [SDK](https://github.com/Moniepoint/dart-flow)
- [SDK](https://github.com/cla-bit/MonnifyEase)
- [SDK](https://github.com/abdsalam/laravel-monnify)
- [Webhooks](https://developers.monnify.com/docs/webhooks)
- [Errors](https://developers.monnify.com/docs/getting-started/errors)
- [Authentication](https://developers.monnify.com/docs/getting-started/authentication)
- [Rate Limits](https://developers.monnify.com/docs/rate-limits)
- [Versioning](https://developers.monnify.com/docs/getting-started/versioning)
- [Plans](plans/moniepoint-plans-pricing.yml)
- [Rate Limits](rate-limits/moniepoint-rate-limits.yml)
- [Fin Ops](finops/moniepoint-finops.yml)
- [Vocabulary](vocabulary/moniepoint-vocabulary.yml)
- [Rules](rules/moniepoint-rules.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
