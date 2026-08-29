# Security

This repository is a procedure skill. The workflow is browser and prose only: no file here runs as part of the skill, and nothing in this repository reads, stores, or transmits a credential.

## What the install copies

Installing copies the repository folder, so the maintainer's CI check `scripts/validate.sh` lands in your skills directory next to `SKILL.md`. The skill never invokes it and you never need to run it. It takes no input, touches no credential, and only checks installability, link health, payload disclosure, and the installer pin against public URLs, the repository's own tracked files, and the npm registry. It is the only executable this package ships.

`scripts/payload-executables.txt` declares that set, and the `validate` workflow fails if an undeclared executable appears or if this file stops naming one. It runs on every pull request and every push to `main`, so drift in the claim above surfaces as a failed check on the commit that caused it. `main` carries no branch protection, so the check reports drift rather than blocking it: read the check before you trust the claim.

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
