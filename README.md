# awesome-claw

> "Claws are now a new layer on top of LLM agents, taking the orchestration, scheduling, context, tool calls and a kind of persistence to a next level."
> — [Andrej Karpathy](https://x.com/karpathy/status/2024987174077432126)

A curated list of everything in the Claw ecosystem — platforms, tools, security, hardware, communities, and more.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
**English** | [한국어](README_KR.md)

## Why This List?

In February 2026, OpenClaw became the fastest GitHub repo to reach 100K stars in history. Within weeks, dozens of lightweight/secure alternatives, cloud hosting services, an AI agent–only social network, and a wave of critical security incidents (CVE-2026-25253, ClawHavoc supply chain attack, 30K+ exposed instances) all emerged simultaneously.

Existing awesome lists are either OpenClaw-specific or simple enumerations. **awesome-claw** covers the entire Claw concept — from Karpathy's original definition through self-hosted platforms, managed services, security tools, hardware setups, orchestration frameworks, and the growing body of research and journalism around this new layer of AI infrastructure.

## What is a Claw?

Andrej Karpathy defined the **Claw** as a distinct new layer in the AI stack: **"First there was chat, then there was code, now there is claw."**

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
  - [Security Tools](#security-tools)
  - [Security Guides & Resources](#security-guides--resources)
- [Hardware](#hardware)
- [Key Concepts](#key-concepts)
- [Articles & References](#articles--references)
  - [Concept & Origin](#concept--origin)
  - [Ecosystem & Landscape](#ecosystem--landscape)
  - [Business & Industry](#business--industry)
  - [Moltbook](#moltbook)
  - [Research & Academic](#research--academic)
  - [Hands-On Guides](#hands-on-guides)
  - [Platform Conflicts](#platform-conflicts)
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
| [ClawWork](https://github.com/HKUDS/ClawWork) | Python | 5K | Turns OpenClaw/NanoBot into AI coworker earning income across 44 economic sectors |
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
- **ClawPal** — TypeScript, gives OpenClaw agents a face/voice/selfie via image gen and Edge TTS
- **Clawe** — TypeScript, "Trello for OpenClaw agents," 4-agent squad on cron schedules

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
| [Kimi Claw](https://www.marktechpost.com/2026/02/15/moonshot-ai-launches-kimi-claw-native-openclaw-on-kimi-com-with-5000-community-skills-and-40gb-cloud-storage-now/) | — | Moonshot AI cloud-native OpenClaw, 5,000+ skills, 40 GB storage, Kimi K2.5 (1T MoE) |

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
| [Knolli](https://www.knolli.ai/) | No-code AI copilot builder, multi-agent, white-labeling, analytics |

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
| [GasTown](https://github.com/steveyegge/gastown) | Multi-agent workspace by Steve Yegge — "Mayor" orchestrates "Polecats" across git-backed rigs (10K stars) |
| [Claw-Kanban](https://github.com/GreenSheep01201/Claw-Kanban) | 6-column Kanban routing tasks to Claude Code, Codex CLI, Gemini CLI with real-time terminal monitoring |

## Security

### Known Risks

- **CVE-2026-25253** — One-click RCE (CVSS 8.8), missing `gatewayUrl` parameter validation
- **CVE-2026-26322** — SSRF in Gateway tool (CVSS 7.6), server-side requests to internal resources
- **CVE-2026-26319** — Missing Telnyx webhook authentication (CVSS 7.5)
- **CVE-2026-26329** — Path traversal in browser upload, write files outside intended directory
- **CVE-2026-27001** — Prompt injection via unsanitized workspace path (CWE-77)
- **CVE-2026-27484** — Discord moderation authorization bypass (CVSS 4.3)
- **ClawHavoc campaign** — 800+ malicious skills (~20% of ClawHub), deploying AMOS stealer
- **AMOS distribution via skills** — 39 malicious skills using deceptive SKILL.md with base64 payloads ([Trend Micro](https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html))
- **Infostealer targeting config files** — Vidar variant exfiltrating gateway tokens and agent context ([The Hacker News](https://thehackernews.com/2026/02/infostealer-steals-openclaw-ai-agent.html))
- **30,000–40,000+ internet-exposed instances** — running without authentication ([BitSight](https://www.bitsight.com/blog/openclaw-ai-security-risks-exposed-instances), [Palo Alto](https://www.paloaltonetworks.com/blog/network-security/why-moltbot-may-signal-ai-crisis/))
- **41.7% of popular skills** — contain command injection or credential exposure vulnerabilities

### Security Tools

| Name | Description |
|------|-------------|
| [SecureClaw](https://github.com/adversa-ai/secureclaw) | OWASP-aligned plugin/skill — 56 audit checks, 5 hardening modules, MITRE ATLAS coverage |
| [ClawSec](https://www.sentinelone.com/blog/clawsec-hardening-openclaw-agents-from-the-inside-out/) | SentinelOne "skill-of-skills" — supply chain integrity, posture hardening, zero-trust comms |
| [ClawKeeper](https://github.com/rad-security/clawkeeper) | RAD Security scanner — 42 checks across 5 phases for misconfig, creds, network hardening |

### Security Guides & Resources

- [Microsoft: Running OpenClaw Safely](https://www.microsoft.com/en-us/security/blog/2026/02/19/running-openclaw-safely-identity-isolation-runtime-risk/) — Identity, isolation, and runtime risk
- [Cisco: Personal AI Agents Are a Security Nightmare](https://blogs.cisco.com/ai/personal-ai-agents-like-openclaw-are-a-security-nightmare) — Threat model analysis
- [CrowdStrike: What Security Teams Need to Know](https://www.crowdstrike.com/en-us/blog/what-security-teams-need-to-know-about-openclaw-ai-super-agent/) — Enterprise perspective
- [Malwarebytes: Can You Use It Safely?](https://www.malwarebytes.com/blog/news/2026/02/openclaw-what-is-it-and-can-you-use-it-safely) — Consumer safety guide
- [Snyk: ClawHub Malicious Campaign](https://snyk.io/articles/clawdhub-malicious-campaign-ai-agent-skills/) — Supply chain attack deep-dive
- [Adversa.ai: Vulnerabilities & Hardening](https://adversa.ai/blog/openclaw-security-101-vulnerabilities-hardening-2026/) — Hardening guide
- [SecurityWeek: SecureClaw Tool](https://www.securityweek.com/openclaw-security-issues-continue-as-secureclaw-open-source-tool-debuts/) — Open-source security scanner
- [Palo Alto Networks: May Signal the Next AI Security Crisis](https://www.paloaltonetworks.com/blog/network-security/why-moltbot-may-signal-ai-crisis/) — "Lethal trifecta" of persistent memory + untrusted content + private data
- [Trend Micro: Agentic Assistant Risks](https://www.trendmicro.com/en_us/research/26/b/what-openclaw-reveals-about-agentic-assistants.html) — 1 in 5 orgs deployed without IT approval
- [Trend Micro: Malicious Skills Distribute AMOS](https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html) — SKILL.md social engineering deep-dive
- [Kaspersky: OpenClaw Vulnerabilities](https://www.kaspersky.com/blog/openclaw-vulnerabilities-exposed/55263/) — 512 audit findings (8 critical), consumer safety guide
- [Jamf: Insider Threat Analysis](https://www.jamf.com/blog/openclaw-ai-agent-insider-threat-analysis/) — macOS detection methods and remediation
- [Infosecurity Magazine: Six New Vulnerabilities](https://www.infosecurity-magazine.com/news/researchers-six-new-openclaw/) — Endor Labs CVE disclosures
- [The Register: Security Whac-A-Mole](https://www.theregister.com/2026/02/02/openclaw_security_issues/) — CVE-2026-25253 patch + Moltbook DB exposure
- [VentureBeat: CISO Guide](https://venturebeat.com/security/openclaw-agentic-ai-security-risk-ciso-guide) — Enterprise security model gaps
- [Immersive Labs: Enterprise Risk Assessment](https://www.immersivelabs.com/resources/c7-blog/openclaw-what-you-need-to-know-before-it-claws-its-way-into-your-organization) — ~900 malicious skills, 40K+ exposed instances
- [Permiso: Inside the OpenClaw Ecosystem](https://permiso.io/blog/inside-the-openclaw-ecosystem-ai-agents-with-privileged-credentials) — AI agent "Rufio" hunts 824+ malicious ClawHub skills
- [CyberArk: Reshaping Enterprise Identity](https://www.cyberark.com/resources/blog/how-autonomous-ai-agents-like-openclaw-are-reshaping-enterprise-identity-security) — AI agents as new machine identity class
- [TechCrunch: Agent Ran Amok on Inbox](https://techcrunch.com/2026/02/23/a-meta-ai-security-researcher-said-an-openclaw-agent-ran-amok-on-her-inbox/) — Real-world incident report

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

### Concept & Origin
- [Karpathy: "Claws" (original tweet)](https://x.com/karpathy/status/2024987174077432126) — "Claws are now a new layer on top of LLM agents"
- [Karpathy: "Claws" concept definition](https://simonwillison.net/2026/Feb/21/claws/) — The original framing (Simon Willison summary)
- [GIGAZINE: Claw AI Agent Layer](https://gigazine.net/gsc_news/en/20260224-claw-ai-agent-layer/) — Explainer
- [DEV: What Are Claws and Why You Shouldn't Run Them on Your Mac Mini](https://dev.to/setas/what-are-claws-and-why-you-shouldnt-run-them-on-your-mac-mini-4o1b) — Counterpoint

### Ecosystem & Landscape
- [Ry Walker: 2026 Personal AI Agent Landscape (38 platforms)](https://rywalker.com/openclaw-alternatives-2026) — Comprehensive survey
- [EvoAI Labs: The Claw Craziness Is Continuing](https://evoailabs.medium.com/openclaw-nanobot-picoclaw-ironclaw-and-zeroclaw-this-claw-craziness-is-continuing-87c72456e6dc) — NanoClaw, PicoClaw, ZeroClaw, IronClaw overview
- [Peter Woods: The Claw AI Agent Family](https://peterwoods.online/blog/the-claw-ai-agent-family) — Directory of the entire Claw family
- [Axios: Gas Town, OpenClaw and the Rise of Open Source Agents](https://www.axios.com/2026/02/24/agents-openclaw-moltbook-gastown) — Landscape analysis + Gartner warning
- [Axios: AI's Centaur Phase Consumes Silicon Valley](https://www.axios.com/2026/02/23/ai-agents-openclaw-openai-anthropic) — Human-AI collaboration shift

### Business & Industry
- [TechCrunch: OpenClaw Creator Joins OpenAI](https://techcrunch.com/2026/02/15/openclaw-creator-peter-steinberger-joins-openai/) — Steinberger leads "next gen personal agents"
- [Peter Steinberger: OpenClaw, OpenAI and the Future](https://steipete.me/posts/2026/openclaw) — Creator's own account
- [VentureBeat: End of the ChatGPT Era](https://venturebeat.com/technology/openais-acquisition-of-openclaw-signals-the-beginning-of-the-end-of-the) — Pivot from chatbots to persistent agents
- [Bloomberg: OpenAI Hires OpenClaw Developer](https://www.bloomberg.com/news/articles/2026-02-15/openai-hires-openclaw-ai-agent-developer-peter-steinberg) — Acquisition coverage
- [CNBC: From Clawdbot to OpenClaw](https://www.cnbc.com/2026/02/02/openclaw-open-source-ai-agent-rise-controversy-clawdbot-moltbot-moltbook.html) — Rise, controversy, 145K+ stars
- [IBM: OpenClaw, Moltbook and the Future](https://www.ibm.com/think/news/clawdbot-ai-agent-testing-limits-vertical-integration) — Enterprise analysis
- [Fortune: Moltbook "most interesting internet"](https://fortune.com/2026/01/31/ai-agent-moltbot-clawdbot-openclaw-data-privacy-security-nightmare-moltbook-social-network/) — Cultural impact
- [SalesforceDevops: The Chatbot Era Is Over](https://salesforcedevops.net/index.php/2026/02/20/ai-agents-awareness-february-2026/) — Paradigm shift analysis

### Moltbook
- [Nature: Scientists Are Listening In](https://www.nature.com/articles/d41586-026-00370-w) — 1.6M agents as research opportunity
- [IEEE Spectrum: Heralds a Messy Future](https://spectrum.ieee.org/moltbook-agentic-ai-agents-openclaw) — Prompt injection, agent-to-agent security
- [NBC News: Social Network for AI Agents Only](https://www.nbcnews.com/tech/tech-news/ai-agents-social-media-platform-moltbook-rcna256738) — Jan 31 breach coverage
- [CNN: Should We Be Scared?](https://edition.cnn.com/2026/02/03/tech/moltbook-explainer-scli-intl) — Mainstream explainer
- [Engadget: What the Hell Is Moltbook?](https://www.engadget.com/ai/what-the-hell-is-moltbook-the-social-network-for-ai-agents-140000787.html) — 770K→1.6M agent growth

### Research & Academic
- [Alan Turing Institute: Agentic AI in the Wild](https://cetas.turing.ac.uk/publications/agentic-ai-wild-lessons-moltbook-and-openclaw) — Policy research on Moltbook + OpenClaw
- [The Conversation: Why It Feels So New (But Really Isn't)](https://theconversation.com/openclaw-and-moltbook-why-a-diy-ai-agent-and-social-media-for-bots-feel-so-new-but-really-arent-274744) — Historical context

### Hands-On Guides
- [MacStories: Future of Personal AI Assistants](https://www.macstories.net/stories/clawdbot-showed-me-what-the-future-of-personal-ai-assistants-looks-like/) — M4 Mac mini + Claude Opus 4.5 + Telegram
- [Coder: Blink + Mac Mini Secure Setup](https://coder.com/blog/why-i-ditched-openclaw-and-built-a-more-secure-ai-agent-on-blink-mac-mini) — Security-first approach
- [TechTarget: OpenClaw and Moltbook Explained](https://www.techtarget.com/searchcio/feature/OpenClaw-and-Moltbook-explained-The-latest-AI-agent-craze) — Enterprise-focused explainer

### Platform Conflicts
- [VentureBeat: Google Clamps Down on Antigravity](https://venturebeat.com/orchestration/google-clamps-down-on-antigravity-malicious-usage-cutting-off-openclaw-users) — Mass account suspensions for OpenClaw usage
- [The Register: Antigravity Falls Under Compute Load](https://www.theregister.com/2026/02/23/google_antigravity_compute_burden/) — OAuth integration overwhelms Google

### Reference
- [Wikipedia: OpenClaw](https://en.wikipedia.org/wiki/OpenClaw) — Encyclopedia entry

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before submitting a PR.

## License

[MIT](LICENSE)
