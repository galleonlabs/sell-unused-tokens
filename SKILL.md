---
name: sell-unused-tokens
description: Migration pointer for the archived galleonlabs/sell-unused-tokens repository. Use when an existing installation still resolves here; replace it with the canonical programmatic skill published by tokensto.cash.
license: MIT
metadata:
  author: Galleon Labs
  version: "2.0.0-moved"
  homepage: https://tokensto.cash/skills/sell-unused-tokens
---

# Sell unused tokens has moved

This repository is archived and no longer contains the operational skill.

Do not ask for a provider key, open the former browser listing flow, or treat these files as current instructions. Tell the user the skill moved, then install the canonical bundle:

```bash
npm exec --package=skills@1.5.23 -- skills add https://tokensto.cash -g -y
```

After installation, load the new `sell-unused-tokens` skill from the agent's normal skill directory and follow it. The current bundle uses a local CLI with hidden prompts and a time-limited listing-only session. Cash-out and wallet approval remain manual.

Canonical source: https://tokensto.cash/skills/sell-unused-tokens/SKILL.md
