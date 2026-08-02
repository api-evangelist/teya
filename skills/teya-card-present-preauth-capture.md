---
name: Take a card-present pre-authorization and capture it
description: Reserve funds on a physical card via the Teya Payments Gateway, then capture the final amount.
api: openapi/teya-payments-openapi.yaml
operations: [cardTransactions_2, captureRequest, cardTransactions]
---

# Card-present pre-authorization and capture

Use this flow for hotel/rental/tab scenarios: reserve funds at check-in, capture the final amount at checkout.

## Auth
- OAuth 2.0 bearer token from `https://id.teya.com/oauth/v2/oauth-token`. Base `https://api.teya.com`.
- Card data is sent **encrypted** (`encrypted_track` + `encryption_key_id` + `encryption_ksn`);
  never send a clear PAN.

## Steps
1. **Pre-authorize** — `POST /v1/transactions/card-present` (`cardTransactions_2`) with
   `type: PRE_AUTHORISATION`, `amounts.amount` (minor units), `amounts.currency`, `terminal_id`,
   `entry_mode`, `verification_method`, and encrypted track data.
   Send an `Idempotency-Key`. The response returns the transaction `id`.
2. **Capture** — `POST /v1/transactions/{id}/capture` (`captureRequest`) with the final
   `amount` (≤ pre-auth) and a fresh `Idempotency-Key`.
3. **Refund if needed** — `POST /v3/refunds` (`cardTransactions`) with `transaction_id`,
   `terminal_id`, and `amount` for full or partial refunds.

## Rules
- Amounts are minor-unit integers; currencies ISO-4217; timestamps ISO-8601.
- Transaction types: AUTHORISATION, CAPTURE, REFUND, REVERSAL.
- Each write needs a unique `Idempotency-Key`; reuse with a different body returns `409`.
- Handle declines (`460`), `424` dependency failures, and `429` rate limits;
  see `errors/teya-problem-types.yml`. Test with sandbox cards (`sandbox/teya-sandbox.yml`).
