# sell-unused-tokens (archived)

This repository has moved to [tokensto.cash](https://tokensto.cash/skills/sell-unused-tokens). It is retained as a migration pointer for existing links and installations; it is no longer the source of truth.

The canonical skill now ships with a secret-safe local CLI and a narrow listing-only API. Browser automation is no longer the normal workflow. Provider keys and one-time pairing codes are entered only through hidden terminal prompts, not chat or command arguments.

## Install the current skill

```bash
npm exec --package=skills@1.5.23 -- skills add https://tokensto.cash -g -y
```

This discovers the complete bundle from `https://tokensto.cash/.well-known/agent-skills/index.json`.

## Existing installations

If an agent loaded this repository as a skill, stop and replace it with the command above. Do not copy this repository into an agent skills directory and do not follow its former browser-driven listing procedure.

The current instructions, CLI, references, and security boundary are published by tokensto.cash:

- [Skill page](https://tokensto.cash/skills/sell-unused-tokens)
- [Raw skill](https://tokensto.cash/skills/sell-unused-tokens/SKILL.md)
- [Discovery manifest](https://tokensto.cash/.well-known/agent-skills/index.json)

Operator: [Galleon Labs](https://galleonlabs.io). Support: gm@galleonlabs.io.
