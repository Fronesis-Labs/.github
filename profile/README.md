# Fronesis Labs

**Founder-built infrastructure for verifiable AI agent decisions.**

[![MCP](https://img.shields.io/badge/MCP-Streamable%20HTTP-2563eb)](https://mcp.fronesislabs.com/mcp)
[![Python](https://img.shields.io/badge/Python-dcl--core-3776ab)](https://pypi.org/project/dcl-core/)
[![npm](https://img.shields.io/badge/npm-dcl--sdk-cb3837)](https://www.npmjs.com/package/@fronesis-labs/dcl-sdk)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue)](https://github.com/Fronesis-Labs/dcl-webhook/blob/main/LICENSE)
[![Transparency Board](https://img.shields.io/badge/public-evidence%20board-0f766e)](https://transparency.fronesislabs.com/)

*Don't trust the agent. Trust the proof.*

**Verification is not a feature. It is a precondition.**

Fronesis Labs builds the **Deterministic Commitment Layer (DCL)**: infrastructure for evaluating proposed AI-agent outputs before action, recording supported decisions in tamper-evident form, and independently checking record integrity. DCL is designed to make verification part of an agent workflow—not to claim that every agent action is automatically intercepted or that every risk is eliminated.

## What we're building

### DCL Trust Oracle · Security Gas

A hosted Model Context Protocol (MCP) service for policy evaluation of agent outputs. Agents connect through Streamable HTTP and inspect the live tool schemas before calling a tool.

- **Production MCP endpoint:** [mcp.fronesislabs.com/mcp](https://mcp.fronesislabs.com/mcp)
- **MCP server source:** [Fronesis-Labs/dcl-webhook](https://github.com/Fronesis-Labs/dcl-webhook)
- **MCP Registry:** [com.fronesislabs/dcl-trust-oracle](https://registry.modelcontextprotocol.io/v0/servers?search=com.fronesislabs%2Fdcl-trust-oracle)
- **Smithery:** [DCL Trust Oracle](https://smithery.ai/servers/fronesislabs/dcl-trust-oracle)
- **Glama:** [DCL Trust Oracle server listing](https://glama.ai/mcp/servers/Fronesis-Labs/dcl-webhook)
- **x402 Bazaar:** [bazaar.fronesislabs.com](https://bazaar.fronesislabs.com)

The production MCP server reported version **2.3.1** and **18 tools** in the latest read-only contract check. Tool names, schemas, and available metadata should be read from live `tools/list`; do not rely on old catalog examples. The latest contract check did not re-confirm a successful paid MCP end-to-end call, so this profile does not promise that every client/payment path has been verified.

The service is designed for x402 metering with USDC on Base. The live metadata for `dcl_evaluate_fast` lists a price of **$0.01 per call**; inspect each live tool's metadata and payment requirements for its own terms.

### Leibniz Layer™

The protocol and verification layer behind DCL: deterministic records, hash-chain integrity checks, and verification that can be performed locally against records you already possess.

- **Protocol and implementation:** [DCL Core (Python)](https://github.com/Fronesis-Labs/dcl-core) · [PyPI: dcl-core](https://pypi.org/project/dcl-core/)
- **TypeScript / JavaScript SDK:** [dcl-sdk](https://github.com/Fronesis-Labs/dcl-sdk) · [npm package](https://www.npmjs.com/package/@fronesis-labs/dcl-sdk)
- **Project site:** [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com)

Local verification checks the integrity of supplied records; it does not independently prove that an upstream verdict was correct or that an identifier represents a verified identity.

### DCL Web2 Guard

A client-side guard for applications that need to gate an HTTP side effect on an Oracle decision. The Python `DCLGuard.post()` path fails closed unless it receives an exact `COMMIT` with a matching request digest and an acceptable response. This is **library-level enforcement**: an application can still bypass the guard by using another HTTP client.

The repository documents positive and negative production observations, including an x402 payment followed by a matching-digest `COMMIT`, and a `NO_COMMIT` path in which the guard did not issue the target request.

- **Implementation and evidence:** [DCL Core README](https://github.com/Fronesis-Labs/dcl-core#web2-http-side-effect)

### DCL Identity Guard · TRON / TRC-8004

An open-source reference pre-filter that evaluates on-chain agent registration, reputation, and validation signals before a protected service proceeds; DCL Trust Oracle can then evaluate the proposed action.

- **Repository:** [x402-identity-guard](https://github.com/Fronesis-Labs/x402-identity-guard)

**Status and boundary:** this is a pre-release reference implementation, not a claim of a completed independent live TRON integration. Registry consistency checks do not authenticate the actual caller, and the declared `agent_id` is not yet cryptographically bound to the x402 payer.

### DCL Audit Event

A versioned event schema for representing policy-evaluation outcomes in a consistent, machine-readable form.

- **Schema and implementation:** [dcl-audit-event](https://github.com/Fronesis-Labs/dcl-audit-event)

The schema distinguishes event identifiers, trace identifiers, payment references, and audit-chain hashes. An `agent_id` is informational unless a separate identity mechanism verifies it; a local audit hash is not automatically a blockchain transaction.

### Integrations and agent skills

- **LangChain integration:** [dcl-langchain](https://github.com/Fronesis-Labs/dcl-langchain)
- **Open-source DCL skills:** [dcl-skills](https://github.com/Fronesis-Labs/dcl-skills) · [ClawHub](https://clawhub.ai/daririnch)

Skills and integrations should be treated according to their own published schemas and limitations; their presence does not mean every action in an agent runtime is automatically protected.

## Public evidence

The [DCL Transparency Board](https://transparency.fronesislabs.com/) publishes available DCL records and related evidence. Coverage varies by record: not every historical entry contains a payment transaction, network identifier, event ID, or trace ID. A displayed audit-chain hash is not a substitute for a transaction reference, and only records actually present on the Board should be described as public evidence.

## Connect

For an MCP-capable client, configure the remote server using the production endpoint:

```json
{
  "mcpServers": {
    "dcl-trust-oracle": {
      "url": "https://mcp.fronesislabs.com/mcp"
    }
  }
}
```

After connecting, run `tools/list` and inspect each tool's schema and payment requirements before use. Paid tools require an x402-capable client; other clients receive a Payment Required response.

## Links

| Resource | Link |
|---|---|
| Fronesis Labs | [fronesislabs.com](https://fronesislabs.com/) |
| Leibniz Layer™ | [leibniz.fronesislabs.com](https://leibniz.fronesislabs.com/) |
| DCL Trust Oracle / MCP | [dcl-webhook](https://github.com/Fronesis-Labs/dcl-webhook) |
| Transparency Board | [transparency.fronesislabs.com](https://transparency.fronesislabs.com/) |
| DCL Core | [GitHub](https://github.com/Fronesis-Labs/dcl-core) · [PyPI](https://pypi.org/project/dcl-core/) |
| TypeScript SDK | [GitHub](https://github.com/Fronesis-Labs/dcl-sdk) · [npm](https://www.npmjs.com/package/@fronesis-labs/dcl-sdk) |
| Identity Guard | [GitHub](https://github.com/Fronesis-Labs/x402-identity-guard) |
| Audit Event | [GitHub](https://github.com/Fronesis-Labs/dcl-audit-event) |
| LangChain | [GitHub](https://github.com/Fronesis-Labs/dcl-langchain) |
| Contact | [partnership@fronesislabs.com](mailto:partnership@fronesislabs.com) |
| X | [@keykeeper42](https://x.com/keykeeper42) |

---

© 2026 Fronesis Labs

[![License](https://img.shields.io/badge/license-Apache--2.0-blue)](https://github.com/Fronesis-Labs/dcl-core/blob/main/LICENSE)
