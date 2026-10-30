# Moniepoint

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

**Areas:** Africa · Nigeria · Payments · Banking · Fintech · Acquiring · Point-of-Sale · Collection · Disbursements · Virtual Accounts · Direct Debit · Bills Payment

## Moniepoint on APIs.io

Everything profiled for Moniepoint is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/moniepoint/](https://apis.io/providers/moniepoint/)** — or go straight to one of the APIs or properties below.

### APIs (19)

- [Monnify Webhooks](https://apis.io/apis/moniepoint/monnify-webhooks/) — Asynchronous server-to-server notifications for nine event categories — successful collection, successful / failed / reversed disbursement, successful /…
- [Moniepoint Authentication API](https://apis.io/apis/moniepoint/moniepoint-authentication-api/) — Obtain a Bearer access token for the Monnify API.
- [Moniepoint Banks API](https://apis.io/apis/moniepoint/moniepoint-banks-api/) — NIP bank directory and account validation.
- [Moniepoint Bills Payment API](https://apis.io/apis/moniepoint/moniepoint-bills-payment-api/) — Bill categories, billers, validation, processing, and status.
- [Moniepoint Bulk Transfers API](https://apis.io/apis/moniepoint/moniepoint-bulk-transfers-api/) — Initiate and query bulk transfer batches.
- [Moniepoint Debits API](https://apis.io/apis/moniepoint/moniepoint-debits-api/) — Initiate debits against an active mandate.
- [Moniepoint Invoices API](https://apis.io/apis/moniepoint/moniepoint-invoices-api/) — Create, list, and manage invoices.
- [Moniepoint Limit Profiles API](https://apis.io/apis/moniepoint/moniepoint-limit-profiles-api/) — Per-account transaction limit profiles.
- [Moniepoint Mandates API](https://apis.io/apis/moniepoint/moniepoint-mandates-api/) — Create and manage direct-debit mandates.
- [Moniepoint Push Payments API](https://apis.io/apis/moniepoint/moniepoint-push-payments-api/) — Initiate push payments to a registered POS terminal.
- [Moniepoint Refunds API](https://apis.io/apis/moniepoint/moniepoint-refunds-api/) — Initiate and query refunds.
- [Moniepoint Reserved Accounts API](https://apis.io/apis/moniepoint/moniepoint-reserved-accounts-api/) — Manage dedicated and invoice reserved NUBAN accounts.
- [Moniepoint Settlements API](https://apis.io/apis/moniepoint/moniepoint-settlements-api/) — Settlement batches and transactions reporting.
- [Moniepoint Single Transfers API](https://apis.io/apis/moniepoint/moniepoint-single-transfers-api/) — Initiate, authorize, and query single transfers.
- [Moniepoint Transactions API](https://apis.io/apis/moniepoint/moniepoint-transactions-api/) — Initialize, charge, query, and list collection transactions.
- [Moniepoint Verification API](https://apis.io/apis/moniepoint/moniepoint-verification-api/) — Identity, BVN, NIN, and account verification.
- [Moniepoint Wallet API](https://apis.io/apis/moniepoint/moniepoint-wallet-api/) — Disbursement wallet balance and metadata.
- [Moniepoint Wallets API](https://apis.io/apis/moniepoint/moniepoint-wallets-api/) — Manage wallets and sub-wallets.
- [Moniepoint Subaccounts API](https://apis.io/apis/moniepoint/moniepoint-subaccounts-api/) — Manage settlement sub-accounts.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (13)

Multi-step workflows that chain operations into a business task.

- [Moniepoint Bulk Disbursement](https://apis.io/arazzos/moniepoint/moniepoint-bulk-disbursement-workflow/)
- [Moniepoint Card Charge With OTP](https://apis.io/arazzos/moniepoint/moniepoint-card-charge-otp-workflow/)
- [Moniepoint Collect Via Bank Transfer](https://apis.io/arazzos/moniepoint/moniepoint-collect-bank-transfer-workflow/)
- [Moniepoint KYC Verified Virtual Account](https://apis.io/arazzos/moniepoint/moniepoint-kyc-reserve-account-workflow/)
- [Moniepoint Pay A Bill](https://apis.io/arazzos/moniepoint/moniepoint-pay-bill-workflow/)
- [Moniepoint POS Push Payment](https://apis.io/arazzos/moniepoint/moniepoint-pos-push-payment-workflow/)
- [Moniepoint Recurring Mandate Debit](https://apis.io/arazzos/moniepoint/moniepoint-recurring-mandate-debit-workflow/)
- [Moniepoint Refund A Collected Payment](https://apis.io/arazzos/moniepoint/moniepoint-refund-collected-payment-workflow/)
- [Moniepoint Reserve Virtual Account](https://apis.io/arazzos/moniepoint/moniepoint-reserve-virtual-account-workflow/)
- [Moniepoint Single Transfer With OTP](https://apis.io/arazzos/moniepoint/moniepoint-single-transfer-otp-workflow/)
- [Moniepoint Verify And Disburse](https://apis.io/arazzos/moniepoint/moniepoint-verify-and-disburse-workflow/)
- [Moniepoint Virtual Account With Limit Profile](https://apis.io/arazzos/moniepoint/moniepoint-virtual-account-with-limit-workflow/)
- [Moniepoint Create Wallet And Check Balance](https://apis.io/arazzos/moniepoint/moniepoint-wallet-balance-check-workflow/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Moniepoint Agentic Access](https://apis.io/agentic-access/moniepoint/moniepoint-agentic-access/)

#### JSON Schema (4)

The data models the API reads and writes.

- [Monnify Reserved Account](https://apis.io/schemas/moniepoint/monnify-reserved-account/)
- [Monnify Transaction](https://apis.io/schemas/moniepoint/monnify-transaction/)
- [Monnify Transfer](https://apis.io/schemas/moniepoint/monnify-transfer/)
- [Monnify Webhook Notification](https://apis.io/schemas/moniepoint/monnify-webhook/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Moniepoint Context](https://apis.io/jsonld/moniepoint/moniepoint-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Moniepoint Vocabulary](https://apis.io/vocabularies/moniepoint/moniepoint-vocabulary/)

#### Examples (5)

Example requests and responses.

- [Moniepoint Push Payment Example](https://apis.io/examples/moniepoint/moniepoint-push-payment-example/)
- [Monnify Initialize Transaction Example](https://apis.io/examples/moniepoint/monnify-initialize-transaction-example/)
- [Monnify Reserve Account Example](https://apis.io/examples/moniepoint/monnify-reserve-account-example/)
- [Monnify Single Transfer Example](https://apis.io/examples/moniepoint/monnify-single-transfer-example/)
- [Monnify Webhook Successful Collection Example](https://apis.io/examples/moniepoint/monnify-webhook-successful-collection-example/)

#### Collections (44)

Postman and Open Collection request collections.

- [Moniepoint POS Push Payment Authentication API](https://apis.io/collections/moniepoint/open-moniepoint-authentication-api/)
- [Moniepoint POS Push Payment Authentication Banks API](https://apis.io/collections/moniepoint/open-moniepoint-banks-api/)
- [Moniepoint POS Push Payment Authentication Bills Payment API](https://apis.io/collections/moniepoint/open-moniepoint-bills-payment-api/)
- [Moniepoint POS Push Payment Authentication Bulk Transfers API](https://apis.io/collections/moniepoint/open-moniepoint-bulk-transfers-api/)
- [Moniepoint POS Push Payment Authentication Debits API](https://apis.io/collections/moniepoint/open-moniepoint-debits-api/)
- [Moniepoint POS Push Payment Authentication Invoices API](https://apis.io/collections/moniepoint/open-moniepoint-invoices-api/)
- [Moniepoint POS Push Payment Authentication Limit Profiles API](https://apis.io/collections/moniepoint/open-moniepoint-limit-profiles-api/)
- [Moniepoint POS Push Payment Authentication Mandates API](https://apis.io/collections/moniepoint/open-moniepoint-mandates-api/)
- [Moniepoint POS Push Payment API](https://apis.io/collections/moniepoint/open-moniepoint-pos-api/)
- [Moniepoint POS Push Payment Authentication Push Payments API](https://apis.io/collections/moniepoint/open-moniepoint-push-payments-api/)
- [Moniepoint POS Push Payment Authentication Refunds API](https://apis.io/collections/moniepoint/open-moniepoint-refunds-api/)
- [Moniepoint POS Push Payment Authentication Reserved Accounts API](https://apis.io/collections/moniepoint/open-moniepoint-reserved-accounts-api/)
- [Moniepoint POS Push Payment Authentication Settlements API](https://apis.io/collections/moniepoint/open-moniepoint-settlements-api/)
- [Moniepoint POS Push Payment Authentication Single Transfers API](https://apis.io/collections/moniepoint/open-moniepoint-single-transfers-api/)
- [Moniepoint POS Push Payment Authentication Sub-Accounts API](https://apis.io/collections/moniepoint/open-moniepoint-sub-accounts-api/)
- [Moniepoint POS Push Payment Authentication Transactions API](https://apis.io/collections/moniepoint/open-moniepoint-transactions-api/)
- [Moniepoint POS Push Payment Authentication Verification API](https://apis.io/collections/moniepoint/open-moniepoint-verification-api/)
- [Moniepoint POS Push Payment Authentication Wallet API](https://apis.io/collections/moniepoint/open-moniepoint-wallet-api/)
- [Moniepoint POS Push Payment Authentication Wallets API](https://apis.io/collections/moniepoint/open-moniepoint-wallets-api/)
- [Monnify Authentication API](https://apis.io/collections/moniepoint/open-monnify-authentication-api/)
- [Monnify Bills Payment API](https://apis.io/collections/moniepoint/open-monnify-bills-payment-api/)
- [Monnify Collections API](https://apis.io/collections/moniepoint/open-monnify-collections-api/)
- [Monnify Direct Debit API](https://apis.io/collections/moniepoint/open-monnify-direct-debit-api/)
- [Monnify Disbursements API](https://apis.io/collections/moniepoint/open-monnify-disbursements-api/)
- [Monnify Invoices API](https://apis.io/collections/moniepoint/open-monnify-invoices-api/)
- …and 19 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Moniepoint — jsonschema rules](https://apis.io/rules/moniepoint/moniepoint-jsonschema-spectral-rules/)
- [Moniepoint API Rules](https://apis.io/rules/moniepoint/moniepoint-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Moniepoint Authentication](https://apis.io/security/moniepoint/moniepoint-authentication/)
- [Moniepoint Domain Security](https://apis.io/security/moniepoint/moniepoint-domain-security/)
- [Moniepoint Trust Center](https://apis.io/security/moniepoint/moniepoint-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Moniepoint Plans Pricing](https://apis.io/plans/moniepoint/moniepoint-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Moniepoint Rate Limits](https://apis.io/rate-limits/moniepoint/moniepoint-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Moniepoint Finops](https://apis.io/finops/moniepoint/moniepoint-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Documentation](https://developers.monnify.com/api)
- [Getting started](https://developers.monnify.com/docs/getting-started)
- [Support](https://support.moniepoint.com)
- [Changelog](https://developers.monnify.com/docs/change-logs)
- [Blog](https://developers.monnify.com/blog)
- [Trust centre](https://trust.moniepoint.com)
- [Terms of service](https://moniepoint.com/ng/terms-of-service)
- [Privacy policy](https://moniepoint.com/ng/privacy-policy)
- [GitHub](https://github.com/Moniepoint)

## API Evangelist rating

**Unrated** — no public website could be reached for this company, so there was almost nothing to measure and nothing a reader could check.

This is not a score of zero. No rating is published for this company. If that is wrong because something public exists that we missed, say so on this repository or email [info@apievangelist.com](mailto:info@apievangelist.com) and it will be re-run — free, and no justification needed.

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Moniepoint: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/moniepoint/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
