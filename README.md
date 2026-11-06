<!-- Put this block at the very top of the upstream README.md. Keep the upstream README below it unchanged so merges from a2aproject/A2A stay clean. -->

> ### A2A.jos — the Agent2Agent protocol, as the transport for `.jos` contracts
>
> This is a fork of the [Agent2Agent (A2A) protocol](https://github.com/a2aproject/A2A), maintained for the `.jos` open standard. The upstream text below is unchanged.
>
> **Why it exists.** A2A defines how agents talk to each other. `.jos` defines what one agent is asking another to achieve: the objective, the checks that prove it was met, and the limits it must respect. The `.jos` specification already defines the binding: a `.jos` document travels as a structured data part of an A2A message with the content type `application/vnd.jos+json`, and the reference kernels pass the `a2a-binding` conformance vector. This fork is where that binding is written up against the protocol text itself.
>
> **Status, stated plainly.** No `.jos`-specific change has been committed to this fork yet; it tracks upstream. Proposals are welcome as issues in the [.jos specification repository](https://github.com/josfox-jos/jos-spec/issues).
>
> **The `.jos` family:** [community start page](https://github.com/josfox-jos/jos) · [normative specification 2.0.0](https://github.com/josfox-jos/jos-spec) · [jos.mx landing source](https://github.com/josfox-jos/jos.mx) · [0.0.7 historical draft](https://github.com/josfox-ai/jos-format-spec) · [the JavaScript SDK fork, .jos-a2a-js](https://github.com/josfox-ai/.jos-a2a-js)
>
> **Built by JOSFOX:** [JOSFOX AI deep-link helper](https://github.com/josfox-ai/josfoxai-deep-link) · [reserved deep-link name under josfox-jos](https://github.com/josfox-jos/josfoxai-deep-link)

---

## Public platform documentation — expanded ecosystem

For readers of `josfox-ai/A2A.jos`, distribution status per platform is documented in one public hub; its existence does not imply a downloadable artifact or verified host compatibility.

- For readers of `josfox-ai/A2A.jos`, [jos-omni](https://github.com/josfox-ai/jos-omni) provides distribution documentation hub.

# Agent2Agent (A2A) Protocol

[![PyPI - Version](https://img.shields.io/pypi/v/a2a-sdk)](https://pypi.org/project/a2a-sdk)
[![Apache License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
<a href="https://codewiki.google/github.com/a2aproject/a2a">
  <img src="https://www.gstatic.com/_/boq-sdlc-agents-ui/_/r/Mvosg4klCA4.svg" alt="Ask Code Wiki" height="20">
</a>

<!-- markdownlint-disable MD041 -->
<div style="text-align: center;">
  <div class="centered-logo-text-group">
    <img src="docs/assets/a2a-logo-black.svg" alt="Agent2Agent Protocol Logo" width="100">
    <h1>Agent2Agent (A2A) Protocol</h1>
  </div>
</div>

**An open protocol enabling communication and interoperability between opaque agentic applications.**

The Agent2Agent (A2A) protocol addresses a critical challenge in the AI landscape: enabling gen AI agents, built on diverse frameworks by different companies running on separate servers, to communicate and collaborate effectively - as agents, not just as tools. A2A aims to provide a common language for agents, fostering a more interconnected, powerful, and innovative AI ecosystem.

With A2A, agents can:

- Discover each other's capabilities.
- Negotiate interaction modalities (text, forms, media).
- Securely collaborate on long running tasks.
- Operate without exposing their internal state, memory, or tools.

## Intro to A2A Video

[![A2A Intro Video](https://img.youtube.com/vi/Fbr_Solax1w/hqdefault.jpg)](https://goo.gle/a2a-video)

## Why A2A?

As AI agents become more prevalent, their ability to interoperate is crucial for building complex, multi-functional applications. A2A aims to:

- **Break Down Silos:** Connect agents across different ecosystems.
- **Enable Complex Collaboration:** Allow specialized agents to work together on tasks that a single agent cannot handle alone.
- **Promote Open Standards:** Foster a community-driven approach to agent communication, encouraging innovation and broad adoption.
- **Preserve Opacity:** Allow agents to collaborate without needing to share internal memory, proprietary logic, or specific tool implementations, enhancing security and protecting intellectual property.

### Key Features

- **Standardized Communication:** JSON-RPC 2.0 over HTTP(S).
- **Agent Discovery:** Via "Agent Cards" detailing capabilities and connection info.
- **Flexible Interaction:** Supports synchronous request/response, streaming (SSE), and asynchronous push notifications.
- **Rich Data Exchange:** Handles text, files, and structured JSON data.
- **Enterprise-Ready:** Designed with security, authentication, and observability in mind.

## Getting Started

- 📚 **Explore the Documentation:** Visit the [Agent2Agent Protocol Documentation Site](https://a2a-protocol.org) for a complete overview, the full protocol specification, tutorials, and guides.
- 📝 **View the Specification:** [A2A Protocol Specification](https://a2a-protocol.org/latest/specification/)
- Use the SDKs:
    - [🐍 A2A Python SDK](https://github.com/a2aproject/a2a-python) `pip install a2a-sdk`
    - [🐿️ A2A Go SDK](https://github.com/a2aproject/a2a-go) `go get github.com/a2aproject/a2a-go`
    - [🧑‍💻 A2A JS SDK](https://github.com/a2aproject/a2a-js) `npm install @a2a-js/sdk`
    - [☕️ A2A Java SDK](https://github.com/a2aproject/a2a-java) using maven
    - [🔷 A2A .NET SDK](https://github.com/a2aproject/a2a-dotnet) using [NuGet](https://www.nuget.org/packages/A2A) `dotnet add package A2A`
- 🎬 Use our [samples](https://github.com/a2aproject/a2a-samples) to see A2A in action

## Contributing

We welcome community contributions to enhance and evolve the A2A protocol!

- **Questions & Discussions:** Join our [GitHub Discussions](https://github.com/a2aproject/A2A/discussions).
- **Issues & Feedback:** Report issues or suggest improvements via [GitHub Issues](https://github.com/a2aproject/A2A/issues).
- **Contribution Guide:** See our [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to contribute.
- **Private Feedback:** Use this [Google Form](https://goo.gle/a2a-feedback).
- **Partner Program:** Google Cloud customers can join our partner program via this [form](https://goo.gle/a2a-partner).

## What's next

### Protocol Enhancements

- **Agent Discovery:**
    - Formalize inclusion of authorization schemes and optional credentials directly within the `AgentCard`.
- **Agent Collaboration:**
    - Investigate a `QuerySkill()` method for dynamically checking unsupported or unanticipated skills.
- **Task Lifecycle & UX:**
    - Support for dynamic UX negotiation _within_ a task (e.g., agent adding audio/video mid-conversation).
- **Client Methods & Transport:**
    - Explore extending support to client-initiated methods (beyond task management).
    - Improvements to streaming reliability and push notification mechanisms.

## About

The A2A Protocol is an open source project under the Linux Foundation, contributed by Google. It is licensed under the [Apache License 2.0](LICENSE) and is open to contributions from the community.
