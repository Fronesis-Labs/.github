
# Fronesis Labs

**Building the cryptographic verification layer for the AI agent economy.**

[![smithery badge](https://smithery.ai/badge/fronesislabs/dcl-trust-oracle)](https://smithery.ai/servers/fronesislabs/dcl-trust-oracle) [![dcl-webhook MCP server](https://glama.ai/mcp/servers/Fronesis-Labs/dcl-webhook/badges/score.svg)](https://glama.ai/mcp/servers/Fronesis-Labs/dcl-webhook) [![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/Fronesis-Labs/dcl-webhook/blob/main/LICENSE)

---
**Don't trust the agent. Trust the proof.**

## What we build

### ⬡ Leibniz Layer™

A deterministic cryptographic protocol for sealing, verifying, and auditing AI agent decisions.  
Every action an agent takes can be committed into a tamper-evident hash chain — privacy-first (raw content is never stored, only hashes).

→ [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com)

### DCL Trust Oracle

Production implementation of Leibniz Layer™ as a live MCP server.  
Metered via **x402** (USDC on Base). No account. Pay per call.

→ MCP: `https://mcp.fronesislabs.com/mcp`  
→ [Smithery](https://smithery.ai/servers/fronesislabs/dcl-trust-oracle) · [Glama](https://glama.ai/mcp/servers/Fronesis-Labs/dcl-webhook) · [402 Index](https://bazaar.fronesislabs.com)

### SDKs

### SDKs

Client-side verification for the DCL protocol — no server round-trip required. Recomputes the hash locally and tells you if a chain record was tampered with.

→ TypeScript: `npm install @fronesis-labs/dcl-sdk` — [npmjs.com/package/@fronesis-labs/dcl-sdk](https://www.npmjs.com/package/@fronesis-labs/dcl-sdk) · [github.com/Fronesis-Labs/dcl-sdk](https://github.com/Fronesis-Labs/dcl-sdk)
→ Python: `pip install dcl-core` — [pypi.org/project/dcl-core](https://pypi.org/project/dcl-core) · [github.com/Fronesis-Labs/dcl-core](https://github.com/Fronesis-Labs/dcl-core)

### DCL Skills (open source)

Instruction-only + live-mode skills for AI agents:  
jailbreak defense, PII/secret redaction, policy enforcement, hallucination checks, and a DeFi/crypto suite.

→ [github.com/Fronesis-Labs/dcl-skills](https://github.com/Fronesis-Labs/dcl-skills)  
→ [ClawHub @daririnch](https://clawhub.ai/daririnch)

**License:** Apache 2.0 (this and related repos).  
ClawHub listings are under the platform's required MIT-0.

---

## Connect the MCP endpoint

\`\`\`json
{
  "mcpServers": {
    "dcl-trust-oracle": {
      "url": "https://mcp.fronesislabs.com/mcp"
    }
  }
}
\`\`\`

Payment is handled via x402 (USDC on Base). No API key or account required for x402-capable clients.

---

## Resources

| | |
|---|---|
| 🌐 Website | [fronesislabs.com](https://fronesislabs.com) |
| ⬡ Leibniz Layer™ | [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com) |
| 📦 DCL Skills | [github.com/Fronesis-Labs/dcl-skills](https://github.com/Fronesis-Labs/dcl-skills) |
| 🔌 MCP / Trust Oracle | [github.com/Fronesis-Labs/dcl-webhook](https://github.com/Fronesis-Labs/dcl-webhook) |
| 🛠️ Smithery | [smithery.ai/servers/fronesislabs/dcl-trust-oracle](https://smithery.ai/servers/fronesislabs/dcl-trust-oracle) |
| 🦙 Glama | [glama.ai/mcp/servers/Fronesis-Labs/dcl-webhook](https://glama.ai/mcp/servers/Fronesis-Labs/dcl-webhook) |
| 📄 Whitepaper | [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com) |
| 🐦 X | [@keykeeper42](https://x.com/keykeeper42) |
| 📧 Contact | [partnership@fronesislabs.com](mailto:partnership@fronesislabs.com) |

---

*Every decision, every action — deterministically sealed, tamper-evident, auditable.*

© 2026 Fronesis Labs · Open source (Apache 2.0)
