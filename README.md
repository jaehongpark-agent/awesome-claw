# awesome-claw

> "Just as LLM agents were a new layer on top of LLMs, Claws are yet another new layer on top of LLM agents."
> — Andrej Karpathy

A curated list of everything in the Claw ecosystem — platforms, tools, security, hardware, communities, and more.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

## What is a Claw?

Andrej Karpathy coined the term **Claw** to describe the next evolution in AI: **Chat → Code → Claw**.

While a typical AI agent is a script you run once, a **Claw** is an always-on service that:

- Runs 24/7 with persistent memory and state
- Connects to multiple messaging channels (Slack, Discord, WhatsApp, Telegram, etc.)
- Calls tools, APIs, and MCP servers autonomously
- Schedules tasks, monitors events, and reacts in real time
- Manages its own context and orchestrates sub-agents

In short, a Claw is an **AI agent promoted to a full-time service**.

## Contents

- [Self-Hosted Platforms](#self-hosted-platforms)
  - [Tier 1 (10K+ Stars)](#tier-1-10k-stars)
  - [Tier 2 (1K–10K Stars)](#tier-2-1k10k-stars)
  - [Emerging (<1K Stars)](#emerging-1k-stars)
- [Cloud-Hosted / Managed](#cloud-hosted--managed)
  - [OpenClaw Hosting](#openclaw-hosting)
  - [Managed AI Agent Services](#managed-ai-agent-services)
- [Native Apps](#native-apps)
- [AI Agent SNS / Community](#ai-agent-sns--community)
- [Skill Marketplace](#skill-marketplace)
- [Orchestration & Multi-Agent](#orchestration--multi-agent)
- [Security](#security)
  - [Known Risks](#known-risks)
  - [Security Guides & Resources](#security-guides--resources)
- [Hardware](#hardware)
- [Key Concepts](#key-concepts)
- [Articles & References](#articles--references)
- [Contributing](#contributing)
- [License](#license)

## Self-Hosted Platforms

### Tier 1 (10K+ Stars)

| Name | Language | Stars | Key Feature |
|------|----------|-------|-------------|
| [OpenClaw](https://github.com/openclaw/openclaw) | TypeScript | 160K+ | The original — 50+ messaging integrations, MCP support |
| [NanoBot](https://github.com/HKUDS/nanobot) | Python | 22K | 4,000 lines, `pip install`, research-friendly |
| [AstrBot](https://github.com/Soulter/AstrBot) | Python | 17K | Chinese ecosystem, 800+ plugins, QQ/WeChat |
| [PicoClaw](https://github.com/sipeed/picoclaw) | Go | 17K | <10 MB RAM, $10 hardware, edge-first |
| [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) | Rust | 16K | WASM sandbox, <5 MB, 1,017 tests |
| [Pi](https://github.com/modelcontextprotocol/pi) | TypeScript | 14K | OpenClaw's internal engine — 4 tools, minimal system prompt |
| [NanoClaw](https://github.com/qwibitai/nanoclaw) | TypeScript | 10K | Container isolation, Agent SDK, Skills = config |
| [memU](https://github.com/NevaMind-AI/memU) | — | 7K | Long-term memory, knowledge graphs, personalization |

### Tier 2 (1K–10K Stars)

| Name | Language | Stars | Key Feature |
|------|----------|-------|-------------|
| [Moltworker](https://blog.cloudflare.com/moltworker-self-hosted-ai-agent/) | TypeScript | 9K | Cloudflare Workers, serverless, 300+ edge locations |
| [IronClaw](https://github.com/nickclaw/ironclaw) | Rust | 2.7K | NEAR AI, WASM sandbox, self-extending tools |
| [TinyClaw](https://github.com/warengonzaga/tinyclaw) | Shell/TS | 2.3K | Multi-agent teams, plugin architecture |
| [NullClaw](https://github.com/nullclaw/nullclaw) | Zig | 1.4K | 678 KB binary, ~1 MB RAM, <2 ms boot |
| [Antfarm](https://github.com/antfarm-ai/antfarm) | YAML/SQLite | 1.4K | Multi-agent teams (planner / dev / verifier) |
| [Moltis](https://github.com/moltis-ai/moltis) | Rust | 1.3K | MCP multiplexing gateway |
| [zclaw](https://github.com/nickclaw/zclaw) | C | 1.2K | ESP32, 888 KB firmware, GPIO, Telegram |
| [droidclaw](https://github.com/nickclaw/droidclaw) | TypeScript | 931 | Turn old Android phones into agents |

### Emerging (<1K Stars)

- **ZeptoClaw** — Rust, 7 security layers
- **HermitClaw** — Python, autonomous research, entropy-based personality
- **LettaBot** — TypeScript, Letta/MemGPT-based memory
- **safeclaw** — Python, works without LLM, $0 API cost
- **MicroClaw** — Rust, 15+ platform adapters
- **Lobu** — TypeScript, multi-tenant
- **BabyClaw** — JavaScript, single `index.js`
- **MimiClaw** — C, $5 ESP32-S3

## Cloud-Hosted / Managed

### OpenClaw Hosting

| Name | Pricing | Feature |
|------|---------|---------|
| [EasyClaw](https://easyclaw.com) | $49/mo | One-click deploy, managed security, native app (Mac/Win) |
| [OpenClawd.ai](https://openclawd.ai) | — | Official hosted version, auth/encryption/isolation built-in |
| [ClawHost](https://github.com/bfzli/clawhost) | — | Open-source, automatic VPS provisioning |
| [xCloud](https://xcloud.host/openclaw-hosting/) | — | Fully managed, deploy in 5 minutes |
| [OVHcloud](https://www.ovhcloud.com/en/vps/vps-openclaw/) | — | VPS-based hosting |
| [Hostinger](https://www.hostinger.com/vps/docker/openclaw) | — | Docker-based VPS |

### Managed AI Agent Services

| Name | Feature |
|------|---------|
| [Lindy](https://lindy.ai) | iMessage-based, 400K users, $50/mo, SOC2/HIPAA |
| [Manus](https://manus.im) | Meta acquisition ($2–3B), autonomous execution, code deployment |
| [Poke](https://poke.ai) | Messaging-native, privacy-first |
| [Pulsed](https://pulsed.ai) | 12+ tool integrations (Gmail, Slack, Notion, etc.) |
| [Ako](https://ako.ai) | Slack-native, AI as a team member |
| [Nebula](https://nebula.ai) | Slack-like interface, 24/7 workflows |
| [HappyCapy](https://happycapy.ai) | Browser-based WYSIWYG |

## Native Apps

| Name | Platform | Feature |
|------|----------|---------|
| Lazzy | macOS | Floating above cursor, 800+ MCP, local-only |
| Groovy | WhatsApp | WhatsApp orchestration, marketing analytics |
| Majordomo | iOS | Residential proxy differentiation |
| Viola | Cross-platform | Voice-first, on-device processing |

## AI Agent SNS / Community

| Name | Description |
|------|-------------|
| [Moltbook](https://moltbook.com) | AI agent–only social network (Reddit-style), 1.6M+ agents, humans observe only |
| [BotMadang](https://botmadang.org) | Korean AI agent community (by hunkim), MCP server integration, OpenClaw registration |

## Skill Marketplace

| Name | Description |
|------|-------------|
| [ClawHub](https://clawhub.ai) | Official OpenClaw skill registry, 3,286+ skills, vector search |
| [awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) | Community-curated skill collection |

## Orchestration & Multi-Agent

| Name | Description |
|------|-------------|
| [claw-empire](https://github.com/GreenSheep01201/claw-empire) | Pixel-art office UI for managing multiple agents (Claude Code, Codex CLI, etc.) |
| [openclaw-mission-control](https://github.com/abhi1693/openclaw-mission-control) | AI agent orchestration dashboard |
| [AionUi](https://github.com/iOfficeAI/AionUi) | Local cowork app — Gemini CLI, Claude Code, Goose integration |

## Security

### Known Risks

- **CVE-2026-25253** — One-click RCE (CVSS 8.8), missing `gatewayUrl` parameter validation
- **ClawHavoc campaign** — 800+ malicious skills (~20% of ClawHub), deploying AMOS stealer
- **30,000+ internet-exposed instances** — running without authentication
- **41.7% of popular skills** — contain command injection or credential exposure vulnerabilities

### Security Guides & Resources

- [Microsoft: Running OpenClaw Safely](https://www.microsoft.com/en-us/security/blog/2026/02/19/running-openclaw-safely-identity-isolation-runtime-risk/) — Identity, isolation, and runtime risk
- [Cisco: Personal AI Agents Are a Security Nightmare](https://blogs.cisco.com/ai/personal-ai-agents-like-openclaw-are-a-security-nightmare) — Threat model analysis
- [CrowdStrike: What Security Teams Need to Know](https://www.crowdstrike.com/en-us/blog/what-security-teams-need-to-know-about-openclaw-ai-super-agent/) — Enterprise perspective
- [Malwarebytes: Can You Use It Safely?](https://www.malwarebytes.com/blog/news/2026/02/openclaw-what-is-it-and-can-you-use-it-safely) — Consumer safety guide
- [Snyk: ClawHub Malicious Campaign](https://snyk.io/articles/clawdhub-malicious-campaign-ai-agent-skills/) — Supply chain attack deep-dive
- [Adversa.ai: Vulnerabilities & Hardening](https://adversa.ai/blog/openclaw-security-101-vulnerabilities-hardening-2026/) — Hardening guide
- [SecurityWeek: SecureClaw Tool](https://www.securityweek.com/openclaw-security-issues-continue-as-secureclaw-open-source-tool-debuts/) — Open-source security scanner

## Hardware

| Hardware | Use Case | Reference |
|----------|----------|-----------|
| Mac Mini M4 Pro 64 GB | Recommended setup — unified memory for local LLMs | [Setup guide](https://www.marc0.dev/en/blog/openclaw-mac-mini-the-complete-guide-to-running-your-own-ai-agent-in-2026-1770057455419) |
| Raspberry Pi | Low-cost alternative | [itsfoss guide](https://itsfoss.com/openclaw-alternatives/), [Goose + RPi](https://block.github.io/goose/blog/2026/02/06/rpi-openclaw-alternative/) |
| ESP32 | IoT agents (zclaw, MimiClaw) | 888 KB – several MB, GPIO control |
| Old Android phone | Repurpose with droidclaw | — |

## Key Concepts

- **Skills-based configuration** — Instead of config files, the AI modifies code directly (NanoClaw approach)
- **Container isolation** — Docker / Apple Containers for agent sandboxing
- **MCP (Model Context Protocol)** — Integration with the 13,000+ MCP server ecosystem
- **Gateway architecture** — A single process manages sessions, routing, and channels

## Articles & References

- [Karpathy: "Claws" concept definition](https://simonwillison.net/2026/Feb/21/claws/) — The original framing
- [GIGAZINE: Claw AI Agent Layer](https://gigazine.net/gsc_news/en/20260224-claw-ai-agent-layer/) — Explainer
- [Ry Walker: 2026 Personal AI Agent Landscape (38 platforms)](https://rywalker.com/openclaw-alternatives-2026) — Comprehensive survey
- [IBM: OpenClaw, Moltbook and the Future](https://www.ibm.com/think/news/clawdbot-ai-agent-testing-limits-vertical-integration) — Enterprise analysis
- [Fortune: Moltbook "most interesting internet"](https://fortune.com/2026/01/31/ai-agent-moltbot-clawdbot-openclaw-data-privacy-security-nightmare-moltbook-social-network/) — Cultural impact
- [Coder: Blink + Mac Mini Secure Setup](https://coder.com/blog/why-i-ditched-openclaw-and-built-a-more-secure-ai-agent-on-blink-mac-mini) — Security-first approach
- [DEV: What Are Claws and Why You Shouldn't Run Them on Your Mac Mini](https://dev.to/setas/what-are-claws-and-why-you-shouldnt-run-them-on-your-mac-mini-4o1b) — Counterpoint
- [Wikipedia: OpenClaw](https://en.wikipedia.org/wiki/OpenClaw) — Encyclopedia entry

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before submitting a PR.

## License

[MIT](LICENSE)
