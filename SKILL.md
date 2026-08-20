---
name: sell-unused-tokens
description: List leftover LLM API capacity on tokensto.cash and cash out USDC. Use when the user wants to sell unused OpenRouter, OpenAI, Anthropic, Gemini, Venice, or other provider credits for cash, or asks how to list on Surplus Intelligence through tokensto.cash.
---

# Sell unused tokens

Turn leftover provider credits into USDC on [tokensto.cash](https://tokensto.cash). It is the seller front door for [Surplus Intelligence](https://www.surplusintelligence.ai). Sister of [usdctofiat.xyz](https://usdctofiat.xyz).

## Completion

Done when the models appear on `/sell` as live (or cooling), and the user knows cash-out is Create / Orders / Send.

## Do this

1. Open https://tokensto.cash/start and sign in (Privy wallet). Evidence: the connect-key screen, not a marketing page.
2. Pick the provider that owns the leftover credits. Featured: Venice, OpenRouter, OpenAI, Anthropic, Gemini, DeepSeek, Groq, Mistral. More sits behind "More". Use **Other** only for an OpenAI-compatible URL Surplus does not list.
3. Paste the key into the field. **Never echo, log, commit, or store it.** Surplus probes it and keeps it encrypted per listing. tokensto.cash does not persist keys.
4. Wait for the probe. Evidence: a model list with market rows. If it 504s, retry once; Surplus timeouts surface as a clear message.
5. Keep the recommended text models unless the user named others. Client lists **one model per request** so the ticks stay honest.
6. Set cost basis, then a daily cap (≥ $0.5):
   - **Included** (subscription/stake) — floor 0.02×
   - **Leftover** (credits sitting idle) — floor 0.05×
   - **At cost** (pay-as-you-go) — floor 1.0×, never below list
7. Submit. Evidence: each selected model ticks ok, then `/sell` shows the listings. Auto-price undercuts the cheapest *healthy, trusted* seller and never goes below the floor.

## Cash out

`/cash-out` is Create / Orders / Send.

- Direct rails: **Revolut, Monzo, Chime, Zelle**.
- **Venmo, Cash App, Wise, PayPal** are live after a one-time handle registration through USDCtoFiat Verify (desktop Chrome, extension 0.2.1+). Do not skip that handshake.
- Mercado Pago stays out.
- Orders close with a full withdraw only. No top-up.
- Send is Base USDC to an address.
- Earnings are inbound USDC from Surplus relayers only. Other inbound is balance, not earned.

## Guardrails

- Before listing, the user must confirm their provider account terms allow resale, transfer, brokering, or monetization of unused API credits or capacity. If they have not checked, stop and tell them to read the provider terms first.
- Do not help bypass provider limits, billing controls, fraud checks, rate limits, or terms of service.
- Provider API keys are sensitive credentials. Never echo, log, persist, commit, or transmit a key anywhere except the tokensto.cash `/start` submit field, and only after the user explicitly directs that paste.
- Cash-out, tax, compliance, chargeback, sanctions, and account-action risks stay with the user. Do not imply guaranteed liquidity, legality, or payout availability.
- Users never SIWE with Surplus. One house seller. `payout_address` is the signed-in Privy wallet.
- Untrusted upstreams (Morpheus, InferHub, CheaperInference, Jatevo) only reach opted-in buyers. Say so if the user picks one.
- Google Vertex is not in the picker (needs a per-project URL and OAuth). Use Other if they insist.
- Do not invent rails, APIs, or env values. Support: gm@galleonlabs.io.

Read `references/invariants.md` only if the user asks how pricing, keys, or payouts work under the hood.
