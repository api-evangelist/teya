---
name: Offer Dynamic Currency Conversion at checkout
description: Create a Teya FX DCC offer so a cardholder can pay in their home currency.
api: openapi/teya-fx-openapi.yaml
operations: [dccOffer]
---

# Offer Dynamic Currency Conversion (DCC)

Use this flow to let a foreign cardholder choose to pay in their home currency at the point of sale.

## Auth
- OAuth 2.0 bearer token from `https://id.teya.com/oauth/v2/oauth-token`, application granted
  the `fx/dcc/create` scope. Base `https://api.teya.com` (`https://api.teya.xyz` dev).

## Steps
1. **Create an offer** — `POST /fx/v1/dcc/offers` (`dccOffer`) with `store_id`, the card's
   `card_first9` (BIN, 6-9 digits — no full PAN), `base_amount` (minor units), `base_currency`,
   and `cardholder_currency`.
2. Read the response `quote_id`, `exchange_rate`, `markup`, and `cardholder_amount`.
3. Present both options to the cardholder (original vs converted). If they accept DCC, process
   the payment with the `quote_id` via the Payments/Online Payments API.

## Rules
- Only the BIN is used — never send the full card number.
- Amounts are minor-unit integers; currencies ISO-4217; exchange rates have 6 decimals.
- The cardholder must consent to DCC before conversion is applied.
