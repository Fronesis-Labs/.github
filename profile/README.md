Вот актуальная версия заглавного README — без Patent Pending, с open-source позиционированием и актуальным MCP (x402, без API-ключа):

# Fronesis Labs

**Building the cryptographic verification layer for the AI agent economy.**

---

## What we build

### ⬡ Leibniz Layer™

A deterministic cryptographic protocol for sealing, verifying, and auditing AI agent decisions.  
Every action an agent takes can be committed into a tamper-evident hash chain — privacy-first (raw content is never stored, only hashes).

→ [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com)

### DCL Trust Oracle

Production implementation of Leibniz Layer™ as a live MCP server.  
Metered via **x402** (USDC on Base). No account. Pay per call.

→ MCP: `https://mcp.fronesislabs.com/mcp`  
→ [Smithery](https://smithery.ai/servers/fronesislabs/dcl-trust-oracle) · [402 Index](https://bazaar.fronesislabs.com)

### DCL Skills (open source)

Instruction-only + live-mode skills for AI agents:  
jailbreak defense, PII/secret redaction, policy enforcement, hallucination checks, and a DeFi/crypto suite.

→ [github.com/Fronesis-Labs/dcl-skills](https://github.com/Fronesis-Labs/dcl-skills)  
→ [ClawHub @daririnch](https://clawhub.ai/daririnch)

**License:** Apache 2.0 (this and related repos).  
ClawHub listings are under the platform’s required MIT-0.

---

## Connect the MCP endpoint

```json
{
  "mcpServers": {
    "dcl-trust-oracle": {
      "url": "https://mcp.fronesislabs.com/mcp"
    }
  }
}
```

Payment is handled via x402 (USDC on Base). No API key or account required for x402-capable clients.

---

## Resources

| | |
|---|---|
| 🌐 Website | [fronesislabs.com](https://fronesislabs.com) |
| ⬡ Leibniz Layer™ | [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com) |
| 📦 DCL Skills | [github.com/Fronesis-Labs/dcl-skills](https://github.com/Fronesis-Labs/dcl-skills) |
| 🔌 MCP / Trust Oracle | [github.com/Fronesis-Labs/dcl-webhook](https://github.com/Fronesis-Labs/dcl-webhook) |
| 📄 Whitepaper | [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com) |
| 🐦 X | [@keykeeper42](https://x.com/keykeeper42) |
| 📧 Contact | [partnership@fronesislabs.com](mailto:partnership@fronesislabs.com) |

---

*Every decision, every action — deterministically sealed, tamper-evident, auditable.*

© 2026 Fronesis Labs · Open source (Apache 2.0)
