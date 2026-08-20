# Security

This repository is a procedure skill. It contains no scripts, no binaries, and no code that transmits credentials.

## Provider keys

- The agent must never echo, log, persist, commit, or transmit a provider API key except into the tokensto.cash `/start` field, and only after the user explicitly directs that paste.
- tokensto.cash does not persist keys. Surplus probes the key and stores it encrypted per listing.
- Do not open GitHub issues, pull requests, or support mail that contain a key. Rotate any key that lands in a log or chat.

## What this skill will not do

- Bypass provider limits, billing controls, fraud checks, rate limits, or terms of service.
- Open a Surplus seller account or SIWE as the user.
- Imply guaranteed liquidity, legality, or payout availability.

## Reporting

gm@galleonlabs.io
