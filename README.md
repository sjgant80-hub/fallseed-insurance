# FallSeed Insurance Broker

> **A Progressive Web App (PWA) seed for UK Insurance firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-insurance/

## What this is

`fallseed-insurance` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Insurance wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

Insurance broking · intermediary (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`fallinsurance`](https://sjgant80-hub.github.io/fallinsurance/) | Policyholder register · risk register · quotes · renewals · D&N records · IDD docs · CASS 5 ledgers · 12-pt compliance |
| onboard | [`fallinsuranceonboard`](https://sjgant80-hub.github.io/fallinsuranceonboard/) | Client onboarding · demands & needs analysis · risk capture · IDD status disclosure · PROD target-market check · fact-find · consent |
| paper | [`fallinsurancepaper`](https://sjgant80-hub.github.io/fallinsurancepaper/) | D&N statement · status disclosure · key facts · IPID · summary information · Consumer Duty fair-value letter · TOBA |
| practice | [`fallinsurancepractice`](https://sjgant80-hub.github.io/fallinsurancepractice/) | Workflow · renewal pipeline · CASS reconciliation · breach log · file reviews · vulnerable-customer log · complaints register |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-insurance-v2`) on your device
- **BroadcastChannel mesh** — `fall-insurance` for cross-tool sync; `fall-signal` for global hello
- **P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1093**, spine-clean mod 127. Mesh channel **`fall-insurance`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.


## What kind of seed is this?

A **level-0** seed in the FallSeed family. Built on the Fork Seed primitive — see [the spec](https://www.ai-nativesolutions.com/spec.html) for the four invariants of replication, the SEED schema, and the six-step fork protocol that every conforming seed implements.
