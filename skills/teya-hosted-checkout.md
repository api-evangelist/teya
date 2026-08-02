---
name: Accept an online payment with Teya Hosted Checkout
description: Create a Teya hosted checkout session, redirect the shopper, and confirm the result.
api: openapi/teya-online-payments-openapi.yaml
operations: [createSessionV2, getSessionInfoV2]
---

# Accept an online payment with Teya Hosted Checkout

Use this flow to take an e-commerce payment without handling card data yourself.

## Auth
- Get an OAuth 2.0 token from `https://id.teya.com/oauth/v2/oauth-token`
  (`https://id.teya.xyz/...` in development). Use client-credentials for server-to-server.
- Send `Authorization: Bearer <token>` on every call. Base URL `https://api.teya.com`.

## Steps
1. **Create a session** — `POST /v2/checkout/sessions` (`createSessionV2`).
   - Body: amount in **minor units** (`5000` = EUR 50.00), ISO-4217 `currency`, line items,
     and return URLs.
   - Send a unique `Idempotency-Key` header so a retry never double-charges.
   - The response returns a `session_id` and a hosted payment URL.
2. **Redirect** the shopper to the hosted payment URL and let them pay on Teya's page.
3. **Confirm** — `GET /v2/checkout/sessions/{session_id}` (`getSessionInfoV2`) to read the
   final status once the shopper returns.

## Rules
- Amounts are integers in minor units; currencies are ISO-4217.
- Reusing an `Idempotency-Key` with a different body returns `409 Conflict`.
- Handle `401` (refresh token), `429` (back off), and the custom error envelope
  (`code`/`message`/`invalid_params`) — see `errors/teya-problem-types.yml`.
- Test with the sandbox cards in `sandbox/teya-sandbox.yml` (dev environment only).
