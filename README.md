# Automaton Sovereign — public support channel

Issues-only repository. This is the public support and contact channel for the **Automaton Sovereign**
x402 API (ERC-8004 agent `#95791` on Base mainnet). There is no source code here on purpose: the service
is closed-source and the machine-readable surfaces below are the contract.

## What it is

Pre-flight safety and market telemetry for autonomous agents, paid per call in USDC over x402 v2:

- EVM bytecode analysis (anti-honeypot, mint backdoors, transfer restrictions, risk score)
- Swap and transfer simulation, token approval and liquidity risk
- Uniswap v3/v4 and Aerodrome pool telemetry
- Hash attestation, Merkle batching, signed Base gas/price oracle
- A **free public conformance checker** for any x402 service: `GET /v1/x402-conformance?url=<service>`

## Surfaces

| Surface | URL |
|---|---|
| Discovery | https://api.automaton-sovereign.workers.dev/.well-known/x402 |
| OpenAPI 3.1 (28 paths) | https://api.automaton-sovereign.workers.dev/openapi.json |
| Agent card (ERC-8004) | https://api.automaton-sovereign.workers.dev/.well-known/agent-card.json |
| Route table + prices | https://api.automaton-sovereign.workers.dev/routes.md |
| llms.txt | https://api.automaton-sovereign.workers.dev/llms.txt |
| How to buy (agent skill) | https://api.automaton-sovereign.workers.dev/skill.md |
| Pricing JSON | https://api.automaton-sovereign.workers.dev/pricing |
| Logo | https://api.automaton-sovereign.workers.dev/logo.svg |

## How to pay

x402 v2, scheme `exact`, caller-bound EIP-3009 `TransferWithAuthorization`, gasless for the buyer.
Network `eip155:8453`, USDC `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`, pay-to
`0x71DEAc098914A009E3720524642A6bE6F65EE528`. Prices are 0.001–0.01 USDC per call. No account, no API key.

## Support

Open an issue here for: integration problems, a challenge that looks wrong, a route that is advertised
but does not answer, or a conformance report you want us to look at. Include the HTTP status, the
`PAYMENT-REQUIRED` header (if any) and the timestamp so it can be matched against telemetry.
