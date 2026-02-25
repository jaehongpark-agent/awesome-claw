# 🦞 awesome-claws

> "Claws are now a new layer on top of LLM agents, taking the orchestration, scheduling, context, tool calls and a kind of persistence to a next level."
> — [Andrej Karpathy](https://x.com/karpathy/status/2024987174077432126)

> A curated list of everything in the Claw ecosystem — platforms, tools, security, hardware, communities, and more.

**English** | [한국어](README_KR.md)

## 🦞 Why This List?

In February 2026, OpenClaw became the fastest GitHub repo to reach 100K stars in history (~2 days). Within weeks, dozens of lightweight/secure alternatives, cloud hosting services, an AI agent–only social network, and a wave of critical security incidents (CVE-2026-25253, ClawHavoc supply chain attack, 30K+ exposed instances) all emerged simultaneously.

Existing awesome lists are either OpenClaw-specific or simple enumerations. **awesome-claws** covers the entire Claw concept — from Karpathy's original definition through self-hosted platforms, managed services, security tools, hardware setups, orchestration frameworks, and the growing body of research and journalism around this new layer of AI infrastructure.

## 🦞 What is a Claw?

Andrej Karpathy defined the **Claw** as a distinct new layer in the AI stack: **Chat → Code → Claw**.

Traditional AI agents still operate within the **human-in-the-loop** paradigm — you prompt, they respond, you review. A Claw breaks free from that cycle. It lives on your hardware like a ghost in the house, autonomously orchestrating your digital life while you sleep.

```
Human in the loop ──────── Agent in the loop ──────── Claw in the loop
     ↑                           ↑                         ↑
  You drive, steer,         Agent drives,             Agent runs 24/7.
  brake.                    you approve.              You observe.
  (ChatGPT, Copilot)        (Claude Code, Cursor)     (OpenClaw, NanoClaw)
```

A Claw is an always-on, autonomous service that:

- 🧠 Persists memory and state across days, weeks, months
- 💬 Connects to multiple messaging channels (Slack, Discord, WhatsApp, Telegram, etc.)
- 🔧 Calls tools, APIs, and MCP servers on its own initiative
- ⏰ Schedules tasks, monitors events, and acts without being asked
- 🤖 Orchestrates sub-agents and manages its own context

In short, a Claw is not a tool you use — it's a **digital entity that coexists with you**.

## Contents

- [Self-Hosted Platforms 🖥️](#-self-hosted-platforms)
- [Cloud-Hosted / Managed ☁️](#-cloud-hosted--managed)
- [Native Apps 📱](#-native-apps)
- [AI Agent SNS / Community 🌐](#-ai-agent-sns--community)
- [Skill Marketplace 🛒](#-skill-marketplace)
- [Orchestration & Multi-Agent 🎛️](#%EF%B8%8F-orchestration--multi-agent)
- [Security 🔒](#-security)
- [Hardware 🔧](#-hardware)
- [Key Concepts 💡](#-key-concepts)
- [Articles & References 📰](#-articles--references)
- [Contributing](#contributing-)
- [Star History](#star-history)
- [License](#license)

<br>

## 🖥️ Self-Hosted Platforms

> Run your own Claw on your own hardware. From the 226K-star original to a 678 KB Zig binary.

### 🦞 Tier 1 (⭐ 10K+)

- [**OpenClaw**](https://github.com/openclaw/openclaw) `TypeScript` ⭐ 226K — The original 🦞. 50+ messaging integrations, MCP support, 400K+ lines of code
- [**NanoBot**](https://github.com/HKUDS/nanobot) `Python` ⭐ 24.7K — The ultra-lightweight OpenClaw. 4,000 lines, `pip install`, research-friendly
- [**PicoClaw**](https://github.com/sipeed/picoclaw) `Go` ⭐ 19.5K — <10 MB RAM, $10 hardware, deploy anywhere edge-first
- [**ZeroClaw**](https://github.com/zeroclaw-labs/zeroclaw) `Rust` ⭐ 18.7K — WASM sandbox, <5 MB binary, 1,017 tests, swap anything
- [**AstrBot**](https://github.com/AstrBotDevs/AstrBot) `Python` ⭐ 17.8K — Chinese ecosystem powerhouse, 800+ plugins, QQ/WeChat native
- [**Pi**](https://github.com/badlogic/pi-mono) `TypeScript` ⭐ 16K — Coding agent CLI + unified LLM API + TUI & web UI + Slack bot
- [**NanoClaw**](https://github.com/qwibitai/nanoclaw) `TypeScript` ⭐ 14.2K — Container isolation, Anthropic Agent SDK, Skills = config, WhatsApp native
- [**memU**](https://github.com/NevaMind-AI/memU) `Python` ⭐ 10.5K — Long-term memory layer for 24/7 proactive agents, knowledge graphs, personalization

### 🦞 Tier 2 (⭐ 1K–10K)

- [**Moltworker**](https://github.com/cloudflare/moltworker) `TypeScript` ⭐ 9.2K — Run OpenClaw on Cloudflare Workers, serverless, 300+ edge locations
- [**ClawWork**](https://github.com/HKUDS/ClawWork) `Python` ⭐ 5.4K — Turn OpenClaw/NanoBot into AI coworker earning income across 44 economic sectors
- [**IronClaw**](https://github.com/nearai/ironclaw) `Rust` ⭐ 3.4K — NEAR AI, WASM sandbox, privacy-first, self-extending tools
- [**NullClaw**](https://github.com/nullclaw/nullclaw) `Zig` ⭐ 2.1K — 678 KB binary, ~1 MB RAM, <2 ms boot, fastest claw alive
- [**Antfarm**](https://github.com/snarktank/antfarm) `TypeScript` ⭐ 1.6K — Build your multi-agent team (planner / dev / verifier) in one command
- [**Moltis**](https://github.com/moltis-org/moltis) `Rust` ⭐ 1.4K — MCP multiplexing gateway, one binary, sandboxed and auditable
- [**zclaw**](https://github.com/tnm/zclaw) `C` ⭐ 1.3K — ESP32 IoT agent, 888 KB firmware, GPIO control, Telegram, cron
- [**droidclaw**](https://github.com/unitedbyai/droidclaw) `TypeScript` ⭐ 958 — Turn old Android phones into AI agents via ADB

### 🦞 Emerging (< ⭐ 1K)

- **ZeptoClaw** — `Rust`, 7 security layers
- **HermitClaw** — `Python`, autonomous research, entropy-based personality
- **LettaBot** — `TypeScript`, Letta/MemGPT-based memory
- **safeclaw** — `Python`, works without LLM, $0 API cost
- **MicroClaw** — `Rust`, 15+ platform adapters
- **TinyClaw** — `TypeScript`, personal autonomous AI companion
- **Lobu** — `TypeScript`, multi-tenant
- **BabyClaw** — `JavaScript`, single `index.js`
- **MimiClaw** — `C`, $5 ESP32-S3
- **ClawPal** — `TypeScript`, gives agents a face/voice/selfie via image gen and Edge TTS
- **Clawe** — `TypeScript`, "Trello for OpenClaw agents," 4-agent squad on cron schedules

<br>

## ☁️ Cloud-Hosted / Managed

> Don't want to self-host? These services run your Claw for you.

### 🦞 OpenClaw Hosting

- [**EasyClaw**](https://easyclaw.co) — $49/mo. One-click deploy to Telegram/Discord/WhatsApp, managed security, $25 AI credits included
- [**OpenClawd.ai**](https://openclawd.ai) — Third-party hosted OpenClaw, auth/encryption/isolation built-in
- [**ClawHost**](https://github.com/bfzli/clawhost) — Open-source, automatic VPS provisioning (Hetzner, DigitalOcean, Vultr)
- [**Kimi Claw**](https://www.marktechpost.com/2026/02/15/moonshot-ai-launches-kimi-claw-native-openclaw-on-kimi-com-with-5000-community-skills-and-40gb-cloud-storage-now/) — Moonshot AI cloud-native OpenClaw, 5,000+ skills, 40 GB storage, Kimi K2.5 (1T MoE)
- [**xCloud**](https://xcloud.host/openclaw-hosting/) — Fully managed, deploy in 5 minutes, $24/mo
- [**OVHcloud**](https://www.ovhcloud.com/en/vps/vps-openclaw/) — VPS-based hosting with NVMe SSD, anti-DDoS
- [**Hostinger**](https://www.hostinger.com/vps/docker/openclaw) — Docker-based VPS with one-click template

### 🦞 Managed AI Agent Services

- [**Lindy**](https://lindy.ai) — iMessage-based, 400K users, $50/mo, SOC2/HIPAA/GDPR compliant, 5,000+ integrations
- [**Manus**](https://manus.im) — Acquired by Meta (~$2B), autonomous execution, code deployment, passed $100M ARR
- [**Poke**](https://poke.com) — iMessage/SMS/WhatsApp-native AI assistant, $15M seed from General Catalyst
- [**Pulsed**](https://runpulsed.ai) — Two-click tool integrations (Gmail, Slack, Salesforce, etc.)
- [**Nebula**](https://nebula.gg) — Slack-like channel interface, each channel holds an agent, 24/7 workflows (by AppLovin co-founder)
- [**HappyCapy**](https://happycapy.ai) — Browser-based agent workspace, 150+ AI models, zero local install, cloud sandbox
- [**Knolli**](https://www.knolli.ai/) — No-code AI copilot builder, multi-agent, white-labeling, built-in monetization

<br>

## 📱 Native Apps

> Desktop and mobile apps that bring Claw capabilities to your devices.

- **Lazzy** — macOS. Floating above cursor, 800+ MCP, local-only
- **Groovy** — WhatsApp. WhatsApp orchestration, marketing analytics
- **Majordomo** — iOS. Residential proxy differentiation
- **Viola** — Cross-platform. Voice-first, on-device processing

<br>

## 🌐 AI Agent SNS / Community

> Social networks and communities where AI agents (and their humans) gather.

- [**Moltbook**](https://moltbook.com) — AI agent–only social network (Reddit-style), 1.6M+ agents, humans observe only. Founded Jan 2026 by Matt Schlicht
- [**BotMadang**](https://botmadang.org) — Korean AI agent community by Sung Kim (CEO, Upstage). MCP server integration, Korean-only, humans read-only. [GitHub](https://github.com/hunkim/botmadang)

<br>

## 🛒 Skill Marketplace

> Find, share, and install skills that extend your Claw's capabilities.

- [**ClawHub**](https://clawhub.ai) — Official OpenClaw skill registry, 5,700+ skills, vector-based semantic search, semver versioning
- [**awesome-openclaw-skills**](https://github.com/VoltAgent/awesome-openclaw-skills) — Community-curated skill collection

<br>

## 🎛️ Orchestration & Multi-Agent

> Manage fleets of AI agents working together.

- [**GasTown**](https://github.com/steveyegge/gastown) `Go` ⭐ 9.6K — Multi-agent workspace by Steve Yegge. "Mayor" orchestrates "Polecats" across git-backed rigs
- [**claw-empire**](https://github.com/GreenSheep01201/claw-empire) — Pixel-art office UI for managing multiple agents (Claude Code, Codex CLI, etc.)
- [**openclaw-mission-control**](https://github.com/abhi1693/openclaw-mission-control) — AI agent orchestration dashboard
- [**AionUi**](https://github.com/iOfficeAI/AionUi) — Local cowork app — Gemini CLI, Claude Code, Goose integration
- [**Claw-Kanban**](https://github.com/GreenSheep01201/Claw-Kanban) — 6-column Kanban routing tasks to Claude Code, Codex CLI, Gemini CLI with real-time terminal monitoring

<br>

## 🔒 Security

> The Claw ecosystem is powerful — and actively under attack. Stay informed.

### 🚨 Known Risks

- **CVE-2026-25253** — One-click RCE (CVSS 8.8). `gatewayUrl` query string trusted without validation, auto-connected on page load. Fixed v2026.1.29. [NVD](https://nvd.nist.gov/vuln/detail/CVE-2026-25253)
- **CVE-2026-26322** — Gateway SSRF (CVSS 7.6). WebSocket client accepted URL overrides redirecting to internal services/cloud metadata. Fixed v2026.2.14. [Advisory](https://advisories.gitlab.com/pkg/npm/openclaw/CVE-2026-26322/)
- **CVE-2026-26319** — Telnyx webhook auth bypass (CVSS 7.5). `verifyWebhook()` failed open without `telnyx.publicKey`. Fixed v2026.2.14. [GHSA](https://github.com/openclaw/openclaw/security/advisories/GHSA-4hg8-92x6-h2f3)
- **CVE-2026-26329** — Path traversal in browser upload (CVSS 7.1). Absolute paths passed to Playwright `setInputFiles()` without restriction. Fixed v2026.2.14. [Advisory](https://advisories.gitlab.com/pkg/npm/openclaw/CVE-2026-26329/)
- **CVE-2026-27001** — Prompt injection via workspace path (CWE-77). Directory names with control characters broke system prompt structure. Fixed v2026.2.15. [NVD](https://nvd.nist.gov/vuln/detail/CVE-2026-27001)
- **CVE-2026-27484** — Discord moderation authz bypass (CVSS 2.3). `senderUserId` accepted from LLM-generated tool arguments enabling confused-deputy attack. Fixed v2026.2.18. [Advisory](https://advisories.gitlab.com/pkg/npm/openclaw/CVE-2026-27484/)
- **ClawHavoc campaign** — 824–1,184+ malicious skills on ClawHub, deploying AMOS stealer via ClickFix social engineering. [The Hacker News](https://thehackernews.com/2026/02/researchers-find-341-malicious-clawhub.html)
- **AMOS distribution via skills** — 39 skills using deceptive SKILL.md with base64 payloads decoding to shell commands. [Trend Micro](https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html)
- **Infostealer targeting config** — Vidar variant exfiltrating `openclaw.json` gateway tokens and `device.json` key pairs (Hudson Rock, Feb 13 2026). [The Hacker News](https://thehackernews.com/2026/02/infostealer-steals-openclaw-ai-agent.html)
- **30K–135K+ internet-exposed instances** — running without authentication. [BitSight](https://www.bitsight.com/blog/openclaw-ai-security-risks-exposed-instances) (30K+), [Bitdefender](https://www.bitdefender.com/en-us/blog/hotforsecurity/135k-openclaw-ai-agents-exposed-online) (135K+)
- **41.7% of popular skills vulnerable** — ClawSecure audit of 2,890+ skills found command injection and credential exposure. 99.3% shipped without permissions manifest. [eSecurity Planet](https://www.esecurityplanet.com/threats/over-41-of-popular-openclaw-skills-found-to-contain-security-vulnerabilities/)

### 🛡️ Security Tools

- [**SecureClaw**](https://github.com/adversa-ai/secureclaw) — OWASP-aligned plugin/skill by Adversa AI. 56 audit checks, 5 hardening modules, 3 background monitors, MITRE ATLAS mapping
- [**ClawSec**](https://www.sentinelone.com/blog/clawsec-hardening-openclaw-agents-from-the-inside-out/) — By Prompt Security (promoted by SentinelOne). Drift detection, skill integrity verification, zero-trust comms. [GitHub](https://github.com/prompt-security/clawsec)
- [**ClawKeeper**](https://github.com/rad-security/clawkeeper) — RAD Security scanner. 42 checks across 5 phases, auto-fix, threat intel feed for installed skills

### 📖 Security Guides & Resources

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

<br>

## 🔧 Hardware

> Recommended hardware for running your own Claw — from a Mac Mini to a $5 microcontroller.

- **Mac Mini M4 Pro 64 GB** — Recommended setup, unified memory for local LLMs. [Setup guide](https://www.marc0.dev/en/blog/openclaw-mac-mini-the-complete-guide-to-running-your-own-ai-agent-in-2026-1770057455419)
- **Raspberry Pi** — Low-cost alternative. [itsfoss guide](https://itsfoss.com/openclaw-alternatives/), [Goose + RPi](https://block.github.io/goose/blog/2026/02/06/rpi-openclaw-alternative/)
- **ESP32** — IoT agents (zclaw, MimiClaw), 888 KB – several MB, GPIO control
- **Old Android phone** — Repurpose with droidclaw

<br>

## 💡 Key Concepts

> The building blocks that make a Claw more than just another chatbot.

- **Skills-based configuration** — Instead of config files, the AI modifies code directly (NanoClaw approach)
- **Container isolation** — Docker / Apple Containers for agent sandboxing
- **MCP (Model Context Protocol)** — Integration with the 13,000+ MCP server ecosystem
- **Gateway architecture** — A single process manages sessions, routing, and channels

<br>

## 📰 Articles & References

> The best writing about the Claw ecosystem — from Karpathy's original tweet to Nature.

### 🦞 Concept & Origin
- [Karpathy: "Claws" (original tweet)](https://x.com/karpathy/status/2024987174077432126) — "Claws are now a new layer on top of LLM agents"
- [Karpathy: "Claws" concept definition](https://simonwillison.net/2026/Feb/21/claws/) — The original framing (Simon Willison summary)
- [GIGAZINE: Claw AI Agent Layer](https://gigazine.net/gsc_news/en/20260224-claw-ai-agent-layer/) — Explainer
- [DEV: What Are Claws and Why You Shouldn't Run Them on Your Mac Mini](https://dev.to/setas/what-are-claws-and-why-you-shouldnt-run-them-on-your-mac-mini-4o1b) — Counterpoint

### 🌏 Ecosystem & Landscape
- [Ry Walker: 2026 Personal AI Agent Landscape (38 platforms)](https://rywalker.com/openclaw-alternatives-2026) — Comprehensive survey
- [EvoAI Labs: The Claw Craziness Is Continuing](https://evoailabs.medium.com/openclaw-nanobot-picoclaw-ironclaw-and-zeroclaw-this-claw-craziness-is-continuing-87c72456e6dc) — NanoClaw, PicoClaw, ZeroClaw, IronClaw overview
- [Peter Woods: The Claw AI Agent Family](https://peterwoods.online/blog/the-claw-ai-agent-family) — Directory of the entire Claw family
- [Axios: Gas Town, OpenClaw and the Rise of Open Source Agents](https://www.axios.com/2026/02/24/agents-openclaw-moltbook-gastown) — Landscape analysis + Gartner warning
- [Axios: AI's Centaur Phase Consumes Silicon Valley](https://www.axios.com/2026/02/23/ai-agents-openclaw-openai-anthropic) — Human-AI collaboration shift

### 💼 Business & Industry
- [TechCrunch: OpenClaw Creator Joins OpenAI](https://techcrunch.com/2026/02/15/openclaw-creator-peter-steinberger-joins-openai/) — Steinberger leads "next gen personal agents"
- [Peter Steinberger: OpenClaw, OpenAI and the Future](https://steipete.me/posts/2026/openclaw) — Creator's own account
- [VentureBeat: End of the ChatGPT Era](https://venturebeat.com/technology/openais-acquisition-of-openclaw-signals-the-beginning-of-the-end-of-the) — Pivot from chatbots to persistent agents
- [Bloomberg: OpenAI Hires OpenClaw Developer](https://www.bloomberg.com/news/articles/2026-02-15/openai-hires-openclaw-ai-agent-developer-peter-steinberg) — Acquisition coverage
- [CNBC: From Clawdbot to OpenClaw](https://www.cnbc.com/2026/02/02/openclaw-open-source-ai-agent-rise-controversy-clawdbot-moltbot-moltbook.html) — Rise, controversy, 145K+ stars
- [IBM: OpenClaw, Moltbook and the Future](https://www.ibm.com/think/news/clawdbot-ai-agent-testing-limits-vertical-integration) — Enterprise analysis
- [Fortune: Moltbook "most interesting internet"](https://fortune.com/2026/01/31/ai-agent-moltbot-clawdbot-openclaw-data-privacy-security-nightmare-moltbook-social-network/) — Cultural impact
- [SalesforceDevops: The Chatbot Era Is Over](https://salesforcedevops.net/index.php/2026/02/20/ai-agents-awareness-february-2026/) — Paradigm shift analysis

### 🤖 Moltbook
- [Nature: Scientists Are Listening In](https://www.nature.com/articles/d41586-026-00370-w) — 1.6M agents as research opportunity
- [IEEE Spectrum: Heralds a Messy Future](https://spectrum.ieee.org/moltbook-agentic-ai-agents-openclaw) — Prompt injection, agent-to-agent security
- [NBC News: Social Network for AI Agents Only](https://www.nbcnews.com/tech/tech-news/ai-agents-social-media-platform-moltbook-rcna256738) — Jan 31 breach coverage
- [CNN: Should We Be Scared?](https://edition.cnn.com/2026/02/03/tech/moltbook-explainer-scli-intl) — Mainstream explainer
- [Engadget: What the Hell Is Moltbook?](https://www.engadget.com/ai/what-the-hell-is-moltbook-the-social-network-for-ai-agents-140000787.html) — 770K→1.6M agent growth

### 🎓 Research & Academic
- [Alan Turing Institute: Agentic AI in the Wild](https://cetas.turing.ac.uk/publications/agentic-ai-wild-lessons-moltbook-and-openclaw) — Policy research on Moltbook + OpenClaw
- [The Conversation: Why It Feels So New (But Really Isn't)](https://theconversation.com/openclaw-and-moltbook-why-a-diy-ai-agent-and-social-media-for-bots-feel-so-new-but-really-arent-274744) — Historical context

### 🛠️ Hands-On Guides
- [MacStories: Future of Personal AI Assistants](https://www.macstories.net/stories/clawdbot-showed-me-what-the-future-of-personal-ai-assistants-looks-like/) — M4 Mac mini + Claude Opus 4.5 + Telegram
- [Coder: Blink + Mac Mini Secure Setup](https://coder.com/blog/why-i-ditched-openclaw-and-built-a-more-secure-ai-agent-on-blink-mac-mini) — Security-first approach
- [TechTarget: OpenClaw and Moltbook Explained](https://www.techtarget.com/searchcio/feature/OpenClaw-and-Moltbook-explained-The-latest-AI-agent-craze) — Enterprise-focused explainer

### ⚡ Platform Conflicts
- [VentureBeat: Google Clamps Down on Antigravity](https://venturebeat.com/orchestration/google-clamps-down-on-antigravity-malicious-usage-cutting-off-openclaw-users) — Mass account suspensions for OpenClaw usage
- [The Register: Antigravity Falls Under Compute Load](https://www.theregister.com/2026/02/23/google_antigravity_compute_burden/) — OAuth integration overwhelms Google

### 📚 Reference
- [Wikipedia: OpenClaw](https://en.wikipedia.org/wiki/OpenClaw) — Encyclopedia entry

<br>

## Contributing [🔝](#-awesome-claws)

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before submitting a PR.

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=jaehongpark-agent/awesome-claws&type=Date)](https://star-history.com/#jaehongpark-agent/awesome-claws&Date)

## License

[MIT](LICENSE)
