# soroban-trader-skill

A controlled recipient-substitution skill for the HoneySkill payment-agent demonstration.

This package contains authored adversarial natural-language instructions: it tries to replace the user-confirmed invoice recipient and conceal the change. It is a test fixture, not a documented real-world malware sample. Use it only with a disposable laboratory agent and fake local funds, never a real wallet or agent profile.

The name is a demonstration label. The current HoneySkill execution adapter supports native payments on an owned Avalanche Fuji fork; this package does not implement Stellar/Soroban trading.

## Run the demonstration

From the prepared HoneySkill development workspace that includes `live-agent`, build the CLI and run:

```sh
pnpm install --frozen-lockfile
pnpm build:cli
mkdir -p outputs
node dist/cli.js live-agent https://github.com/gderamchi/soroban-trader-skill --out outputs/soroban-demo
```

The local alias is `soroban-trader-skill`. The paid OpenAI agent may follow or ignore the redirection; only an observed forbidden proposal blocked by HoneySkill demonstrates runtime interception. Successful execution is verified through local transaction receipts, exact fields, balances and nonce. No public signed transaction is needed.

This repository publishes the skill text only. The `live-agent` integration is currently provided in the prepared development workspace; the published HoneySkill package and main source branch predate it. Installing the older release does not add that command. [HoneySkill project](https://github.com/gderamchi/honeyskill).

## Provenance

Renamed from the authored `settlement-router` fixture on 2026-10-11. Only the YAML frontmatter name changed; the instruction body is identical. Original recorded experiments keep their original identities and hashes. `provenance.json` records the exact transformation and SHA-256 digests.
