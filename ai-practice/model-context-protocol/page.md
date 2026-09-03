# Model Context Protocol

Model Context Protocol (MCP) is a protocol for exchanging context between AI applications and servers. It leaves the application to decide how it uses an LLM and manages the context it receives.[^\[1\]^](https://app.pensieve.uk/r/506/data/161) A June 2026 practitioner synthesis frames MCP’s shift from a “useful developer tool” to an “infrastructure contract” for deployable agents.[^\[2\]^](https://app.pensieve.uk/r/506/data/145) Across the broader practitioner material, the recurring production question is how to make what works in a demo work when real users hit it.[^\[3\]^](https://app.pensieve.uk/r/506/data/140)

## Architecture and protocol surface

MCP uses a host–client–server architecture: an AI host connects to one or more servers by creating one client per server, and each client maintains a dedicated connection to its corresponding server.[^\[4\]^](https://app.pensieve.uk/r/506/data/161) The protocol separates a JSON-RPC-based data layer, which covers client–server communication, capability and version discovery, and core primitives, from a transport layer that covers connection establishment, message framing, and authorization.[^\[5\]^](https://app.pensieve.uk/r/506/data/161)

Servers expose three core primitives:

- **Tools** are executable functions that AI applications can invoke for actions.[^\[6\]^](https://app.pensieve.uk/r/506/data/161)
- **Resources** are data sources that provide contextual information to AI applications.[^\[7\]^](https://app.pensieve.uk/r/506/data/161)
- **Prompts** are reusable templates that structure interactions with language models.[^\[8\]^](https://app.pensieve.uk/r/506/data/161)

This scope is deliberately bounded: the official architecture documentation says MCP focuses on context exchange and does not dictate how AI applications use LLMs or manage the provided context.[^\[9\]^](https://app.pensieve.uk/r/506/data/161)

## Deployment and production constraints

A transport is a binding: protocol semantics remain the same while the binding determines how messages are framed and delivered, how request metadata is carried, and how cancellation and termination are signaled.[^\[10\]^](https://app.pensieve.uk/r/506/data/160) The standard bindings are stdio, which carries newline-delimited messages over the standard streams of a client-launched subprocess, and Streamable HTTP, in which each message is an HTTP POST to one MCP endpoint and replies arrive as a JSON object or a request-scoped SSE stream.[^\[11\]^](https://app.pensieve.uk/r/506/data/160)

Streamable HTTP has concrete deployment requirements. Servers must validate Origin headers to prevent DNS rebinding, local servers should bind only to localhost rather than all network interfaces, and servers should implement authentication for all connections.[^\[12\]^](https://app.pensieve.uk/r/506/data/160) Authorization is a transport-level capability and is optional; when used over HTTP, the MCP specification defines protected servers as OAuth 2.1 resource servers and clients as OAuth 2.1 clients.[^\[13\]^](https://app.pensieve.uk/r/506/data/162) MCP servers must expose OAuth 2.0 Protected Resource Metadata, which clients use for authorization-server discovery.[^\[14\]^](https://app.pensieve.uk/r/506/data/162)

## Infrastructure contract and governance boundary

The infrastructure framing has concrete adoption signals. The MCP analysis identifies WRITER hiring for an MCP/Connector team and SAP Integration Suite + MCP as enterprise signals.[^\[15\]^](https://app.pensieve.uk/r/506/data/145) It also records Sami U.’s stack hierarchy: MCP → Agent Design → RAG → Vector DB.[^\[16\]^](https://app.pensieve.uk/r/506/data/140) The “USB-C” analogy presents MCP as a universal connector that standardizes previously bespoke integration.[^\[17\]^](https://app.pensieve.uk/r/506/data/145)

The same analysis describes MCP as a mechanism for bridging demos to production through standardized, auditable integration contracts rather than bespoke wiring.[^\[18\]^](https://app.pensieve.uk/r/506/data/145) See [Production Readiness](../production-readiness/page.md) for the broader reliability problem.

MCP does not replace governance. The protocol defines the contract; governance defines what happens when the contract is violated. These are complementary layers, not substitutes.[^\[19\]^](https://app.pensieve.uk/r/506/data/145) See [AI Agent Governance](../ai-agent-governance/page.md).
