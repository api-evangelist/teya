---
name: Create and manage a Teya PayByLink payment link
description: Generate a shareable Teya payment link, fetch its status, and update it.
api: openapi/teya-online-payments-openapi.yaml
operations: [createPaymentLinkV2, getPaymentLink, updatePaymentLink]
---

# Create and manage a Teya PayByLink payment link

Use this flow to bill a customer with a shareable link (email, SMS, chat) instead of a checkout page.

## Auth
- OAuth 2.0 bearer token from `https://id.teya.com/oauth/v2/oauth-token`. Base `https://api.teya.com`.

## Steps
1. **Create the link** — `POST /v2/payment-links` (`createPaymentLinkV2`).
   - Body: `amount` (minor units), ISO-4217 `currency`, customer + optional delivery info,
     line items. Include an `Idempotency-Key` header.
   - Response returns a `payment_link_id` and the shareable URL.
2. **Check status** — `GET /v1/payment-links/{payment_link_id}` (`getPaymentLink`).
3. **Update** — `PATCH /v2/payment-links/{payment_link_id}` (`updatePaymentLink`) to change
   amount/details or expire the link before it is paid.

## Rules
- Amounts in minor units; ISO-4217 currency.
- Idempotency-Key prevents duplicate links on retry.
- On errors, read the `code`/`message`/`invalid_params` envelope (`errors/teya-problem-types.yml`).
