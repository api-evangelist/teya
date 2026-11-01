# Teya

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

Teya (formerly SaltPay) is a European payments and business-services provider serving local businesses with card machines, online and in-person card acquiring, a business account, and flexible business funding. Its developer platform exposes REST APIs for the full card-payment lifecycle: Online Payments (Hosted Checkout, PayByLink, e-commerce transactions, captures, refunds, digital receipts, tokens), a Payments Gateway (card-present, MOTO, refunds, captures, reversals), POSLink for cloud terminal control (payment requests, tabs, stores, terminals, ePOS registration, receipt printing), and a Teya FX API for Dynamic Currency Conversion, plus a SOAP-based Settlement API for payout reporting. Authentication is OAuth 2.0 (authorization code and client credentials) against id.teya.com, write operations support Idempotency-Key, and first-party SDKs cover web (Teya Blocks) and Android/iOS point-of-sale.

**Areas:** Company · Payments · Payment Processing · Card Acquiring · Online Payments · Point-of-Sale · E-Commerce · Fintech · Merchant Services · Europe

## Teya on APIs.io

Everything profiled for Teya is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/teya/](https://apis.io/providers/teya/)** — or go straight to one of the APIs or properties below.

### APIs (15)

- [Teya Captures API](https://apis.io/apis/teya/teya-captures-api/) — Operations related to capturing pre-authorised transactions.
- [Teya DCC API](https://apis.io/apis/teya/teya-dcc-api/) — Operations related to dynamic currency conversion
- [Teya ePOS Registration API](https://apis.io/apis/teya/teya-epos-registration-api/) — The ePOS Registration API from Teya — 1 operation(s) for epos registration.
- [Teya Hosted Checkout API](https://apis.io/apis/teya/teya-hosted-checkout-api/) — APIs exposed for session management
- [Teya '@internal' API](https://apis.io/apis/teya/teya-internal-api/) — The '@internal' API from Teya — 2 operation(s) for '@internal'.
- [Teya Pay at Table API](https://apis.io/apis/teya/teya-pay-at-table-api/) — The Pay at Table API from Teya — 9 operation(s) for pay at table.
- [Teya Payment Requests API](https://apis.io/apis/teya/teya-payment-requests-api/) — The Payment Requests API from Teya — 4 operation(s) for payment requests.
- [Teya Print Receipts (ePOS) API](https://apis.io/apis/teya/teya-print-receipts-epos-api/) — Create a receipt print job and fetch its status/events
- [Teya '@public' API](https://apis.io/apis/teya/teya-public-api/) — The '@public' API from Teya — 4 operation(s) for '@public'.
- [Teya Refunds API](https://apis.io/apis/teya/teya-refunds-api/) — The Refunds API from Teya — 2 operation(s) for refunds.
- [Teya Stores API](https://apis.io/apis/teya/teya-stores-api/) — The Stores API from Teya — 3 operation(s) for stores.
- [Teya Terminals API](https://apis.io/apis/teya/teya-terminals-api/) — The Terminals API from Teya — 1 operation(s) for terminals.
- [Teya Tokens API](https://apis.io/apis/teya/teya-tokens-api/) — Token management for saved payment methods
- [Teya Transactions API](https://apis.io/apis/teya/teya-transactions-api/) — Transactions
- [Teya Pay by Link API](https://apis.io/apis/teya/teya-pay-by-link-api/) — APIs exposed for pay by link customers

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [teya](https://apis.io/servers/teya/teya/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Teya Agentic Access](https://apis.io/agentic-access/teya/teya-agentic-access/)

#### Collections (16)

Postman and Open Collection request collections.

- [Teya FX Captures API](https://apis.io/collections/teya/open-teya-captures-api/)
- [Teya FX Captures DCC API](https://apis.io/collections/teya/open-teya-dcc-api/)
- [Teya FX Captures ePOS Registration API](https://apis.io/collections/teya/open-teya-epos-registration-api/)
- [Teya FX Captures Hosted Checkout API](https://apis.io/collections/teya/open-teya-hosted-checkout-api/)
- [Teya FX Captures '@internal' API](https://apis.io/collections/teya/open-teya-internal-api/)
- [Teya FX Captures Pay at Table API](https://apis.io/collections/teya/open-teya-pay-at-table-api/)
- [Teya FX Captures PayByLink API](https://apis.io/collections/teya/open-teya-paybylink-api/)
- [Teya FX Captures Payment Requests API](https://apis.io/collections/teya/open-teya-payment-requests-api/)
- [Teya FX Captures Print Receipts (ePOS) API](https://apis.io/collections/teya/open-teya-print-receipts-epos-api/)
- [Teya FX Captures '@public' API](https://apis.io/collections/teya/open-teya-public-api/)
- [Teya FX Captures Refunds API](https://apis.io/collections/teya/open-teya-refunds-api/)
- [Teya FX Captures Reversals API](https://apis.io/collections/teya/open-teya-reversals-api/)
- [Teya FX Captures Stores API](https://apis.io/collections/teya/open-teya-stores-api/)
- [Teya FX Captures Terminals API](https://apis.io/collections/teya/open-teya-terminals-api/)
- [Teya FX Captures Tokens API](https://apis.io/collections/teya/open-teya-tokens-api/)
- [Teya FX Captures Transactions API](https://apis.io/collections/teya/open-teya-transactions-api/)

#### Overlays (4)

OpenAPI overlays, including conversational phrasing for each operation.

- [Teya Fx Overlay](https://apis.io/overlays/teya/teya-fx-overlay/)
- [Teya Online Payments Overlay](https://apis.io/overlays/teya/teya-online-payments-overlay/)
- [Teya Payments Overlay](https://apis.io/overlays/teya/teya-payments-overlay/)
- [Teya Poslink Overlay](https://apis.io/overlays/teya/teya-poslink-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Teya Authentication](https://apis.io/security/teya/teya-authentication/)
- [Teya Domain Security](https://apis.io/security/teya/teya-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Teya Scopes](https://apis.io/scopes/teya/teya-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.teya.com/)
- [Documentation](https://docs.teya.com/apis/overview)
- [Getting started](https://docs.teya.com/apis/developer-portal/configure-application)
- [API reference](https://docs.teya.com/apis/overview)
- [Pricing](https://www.teya.com/pricing)
- [Sign up](https://www.teya.com/sign-up)
- [Support](https://help.teya.com/)
- [Blog](https://www.teya.com/blog)
- [Terms of service](https://www.teya.com/legal/general-terms)
- [Privacy policy](https://teya.com/legal/privacy-policy)
- [GitHub](https://github.com/saltpay)

## API Evangelist rating

**Kin Score 42.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 49.5 |
| Contract governance | 4.5 |
| Operational transparency | 2.6 |
| Developer ergonomics | 35.1 |
| Access clarity | 44.7 |

**Agent readiness 43.4** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 38.4** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/teya/](https://apis.io/providers/teya/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Teya: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/teya/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
