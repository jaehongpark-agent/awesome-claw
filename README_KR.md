# awesome-claw

> "Claw는 LLM 에이전트 위의 새로운 레이어로, 오케스트레이션, 스케줄링, 컨텍스트, 도구 호출, 그리고 일종의 영속성을 한 단계 끌어올린다."
> — [Andrej Karpathy](https://x.com/karpathy/status/2024987174077432126)

Claw 생태계의 모든 것을 담은 큐레이션 리스트 — 플랫폼, 도구, 보안, 하드웨어, 커뮤니티 등.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[English](README.md) | **한국어**

## 왜 이 리스트인가?

2026년 2월, OpenClaw는 역대 최단 시간에 GitHub 100K 스타를 달성했다. 몇 주 만에 수십 개의 경량/보안 대안, 클라우드 호스팅, AI 에이전트 전용 소셜 네트워크, 그리고 심각한 보안 사건들(CVE-2026-25253, ClawHavoc 공급망 공격, 30K+ 노출 인스턴스)이 동시다발적으로 등장했다.

기존 awesome 리스트들은 OpenClaw에 편중되거나 단순 나열에 그친다. **awesome-claw**는 Karpathy의 원래 정의부터 셀프호스팅 플랫폼, 매니지드 서비스, 보안 도구, 하드웨어 셋업, 오케스트레이션 프레임워크, 그리고 이 새로운 AI 인프라 레이어에 대한 연구와 저널리즘까지 **Claw 개념 전체**를 다룬다.

| 리포지토리 | 초점 | 한계 |
|---|---|---|
| awesome-openclaw | OpenClaw 전용 리소스 | OpenClaw만 다룸 |
| awesome-openclaw-skills | OpenClaw 스킬 모음 | 스킬만 다룸 |
| awesome-claws | 구현체 27개 나열 | 단순 나열, 컨텍스트/보안/생태계 부족 |
| **awesome-claw (본 리스트)** | **Claw 개념 전체** | 개념+생태계+보안+하드웨어+SNS+클라우드+기사 |

## Claw란?

Andrej Karpathy가 AI 스택의 새로운 레이어로 **Claw**를 정의했다: **"처음엔 chat이 있었고, 다음엔 code가 있었고, 이제는 claw가 있다."**

일반적인 AI 에이전트가 한 번 실행하는 스크립트라면, **Claw**는 항시 가동되는 서비스다:

- 영속 메모리와 상태를 유지하며 24/7 운영
- 다중 메시징 채널 연결 (Slack, Discord, WhatsApp, Telegram 등)
- 도구, API, MCP 서버를 자율적으로 호출
- 작업 스케줄링, 이벤트 모니터링, 실시간 대응
- 자체 컨텍스트 관리 및 하위 에이전트 오케스트레이션

한마디로, Claw는 **정규직으로 승진한 AI 에이전트**다.

## 목차

- [셀프호스팅 플랫폼](#셀프호스팅-플랫폼)
  - [Tier 1 (10K+ Stars)](#tier-1-10k-stars)
  - [Tier 2 (1K–10K Stars)](#tier-2-1k10k-stars)
  - [신생 (<1K Stars)](#신생-1k-stars)
- [클라우드 호스팅 / 매니지드](#클라우드-호스팅--매니지드)
  - [OpenClaw 호스팅](#openclaw-호스팅)
  - [매니지드 AI 에이전트 서비스](#매니지드-ai-에이전트-서비스)
- [네이티브 앱](#네이티브-앱)
- [AI 에이전트 SNS / 커뮤니티](#ai-에이전트-sns--커뮤니티)
- [스킬 마켓플레이스](#스킬-마켓플레이스)
- [오케스트레이션 & 멀티 에이전트](#오케스트레이션--멀티-에이전트)
- [보안](#보안)
  - [알려진 위험](#알려진-위험)
  - [보안 도구](#보안-도구)
  - [보안 가이드 & 리소스](#보안-가이드--리소스)
- [하드웨어](#하드웨어)
- [핵심 개념](#핵심-개념)
- [기사 & 참고자료](#기사--참고자료)
  - [개념 & 기원](#개념--기원)
  - [생태계 & 지형도](#생태계--지형도)
  - [비즈니스 & 산업](#비즈니스--산업)
  - [Moltbook](#moltbook)
  - [연구 & 학술](#연구--학술)
  - [실전 가이드](#실전-가이드)
  - [플랫폼 충돌](#플랫폼-충돌)
- [기여하기](#기여하기)
- [라이선스](#라이선스)

## 셀프호스팅 플랫폼

### Tier 1 (10K+ Stars)

| 이름 | 언어 | Stars | 핵심 특징 |
|------|------|-------|-----------|
| [OpenClaw](https://github.com/openclaw/openclaw) | TypeScript | 160K+ | 원조 — 50+ 메시징 통합, MCP 지원 |
| [NanoBot](https://github.com/HKUDS/nanobot) | Python | 22K | 4,000줄, `pip install`, 연구 친화적 |
| [AstrBot](https://github.com/Soulter/AstrBot) | Python | 17K | 중국 생태계, 800+ 플러그인, QQ/WeChat |
| [PicoClaw](https://github.com/sipeed/picoclaw) | Go | 17K | <10MB RAM, $10 하드웨어, 엣지 우선 |
| [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) | Rust | 16K | WASM 샌드박스, <5MB, 1,017 테스트 |
| [Pi](https://github.com/modelcontextprotocol/pi) | TypeScript | 14K | OpenClaw 내부 엔진 — 4개 도구, 최소 시스템 프롬프트 |
| [NanoClaw](https://github.com/qwibitai/nanoclaw) | TypeScript | 10K | 컨테이너 격리, Agent SDK, Skills = 설정 |
| [memU](https://github.com/NevaMind-AI/memU) | — | 7K | 장기 메모리, 지식 그래프, 개인화 |

### Tier 2 (1K–10K Stars)

| 이름 | 언어 | Stars | 핵심 특징 |
|------|------|-------|-----------|
| [Moltworker](https://blog.cloudflare.com/moltworker-self-hosted-ai-agent/) | TypeScript | 9K | Cloudflare Workers, 서버리스, 300+ 엣지 |
| [ClawWork](https://github.com/HKUDS/ClawWork) | Python | 5K | OpenClaw/NanoBot을 44개 경제 분야에서 수입 창출하는 AI 동료로 전환 |
| [IronClaw](https://github.com/nickclaw/ironclaw) | Rust | 2.7K | NEAR AI, WASM 샌드박스, 자기 확장 도구 |
| [TinyClaw](https://github.com/warengonzaga/tinyclaw) | Shell/TS | 2.3K | 멀티 에이전트 팀, 플러그인 아키텍처 |
| [NullClaw](https://github.com/nullclaw/nullclaw) | Zig | 1.4K | 678KB 바이너리, ~1MB RAM, <2ms 부팅 |
| [Antfarm](https://github.com/antfarm-ai/antfarm) | YAML/SQLite | 1.4K | 멀티 에이전트 팀 (planner/dev/verifier) |
| [Moltis](https://github.com/moltis-ai/moltis) | Rust | 1.3K | MCP 멀티플렉싱 게이트웨이 |
| [zclaw](https://github.com/nickclaw/zclaw) | C | 1.2K | ESP32, 888KB 펌웨어, GPIO, Telegram |
| [droidclaw](https://github.com/nickclaw/droidclaw) | TypeScript | 931 | 구형 안드로이드폰 → 에이전트 |

### 신생 (<1K Stars)

- **ZeptoClaw** — Rust, 7 보안 레이어
- **HermitClaw** — Python, 자율 연구, 엔트로피 기반 성격
- **LettaBot** — TypeScript, Letta/MemGPT 기반 메모리
- **safeclaw** — Python, LLM 없이 동작, API 비용 $0
- **MicroClaw** — Rust, 15+ 플랫폼 어댑터
- **Lobu** — TypeScript, 멀티 테넌트
- **BabyClaw** — JavaScript, 단일 `index.js`
- **MimiClaw** — C, $5 ESP32-S3
- **ClawPal** — TypeScript, 이미지 생성·Edge TTS로 에이전트에 얼굴/음성/셀카 부여
- **Clawe** — TypeScript, "OpenClaw용 Trello," 4-에이전트 크론 스케줄

## 클라우드 호스팅 / 매니지드

### OpenClaw 호스팅

| 이름 | 가격 | 특징 |
|------|------|------|
| [EasyClaw](https://easyclaw.com) | $49/월 | 원클릭 배포, 보안 관리, 네이티브 앱 (Mac/Win) |
| [OpenClawd.ai](https://openclawd.ai) | — | 공식 호스팅, 인증/암호화/격리 기본 |
| [ClawHost](https://github.com/bfzli/clawhost) | — | 오픈소스, VPS 자동 프로비저닝 |
| [xCloud](https://xcloud.host/openclaw-hosting/) | — | 완전 관리형, 5분 내 배포 |
| [OVHcloud](https://www.ovhcloud.com/en/vps/vps-openclaw/) | — | VPS 기반 |
| [Hostinger](https://www.hostinger.com/vps/docker/openclaw) | — | Docker 기반 VPS |
| [Kimi Claw](https://www.marktechpost.com/2026/02/15/moonshot-ai-launches-kimi-claw-native-openclaw-on-kimi-com-with-5000-community-skills-and-40gb-cloud-storage-now/) | — | Moonshot AI 클라우드 네이티브 OpenClaw, 5,000+ 스킬, 40GB 스토리지, Kimi K2.5 (1T MoE) |

### 매니지드 AI 에이전트 서비스

| 이름 | 특징 |
|------|------|
| [Lindy](https://lindy.ai) | iMessage 기반, 400K 사용자, $50/월, SOC2/HIPAA |
| [Manus](https://manus.im) | Meta 인수 ($2-3B), 자율 실행, 코드 배포 |
| [Poke](https://poke.ai) | 메시징 네이티브, 프라이버시 우선 |
| [Pulsed](https://pulsed.ai) | 12+ 도구 통합 (Gmail, Slack, Notion 등) |
| [Ako](https://ako.ai) | Slack 네이티브, AI를 팀 직원으로 |
| [Nebula](https://nebula.ai) | Slack 유사 인터페이스, 24/7 워크플로우 |
| [HappyCapy](https://happycapy.ai) | 브라우저 기반 WYSIWYG |
| [Knolli](https://www.knolli.ai/) | 노코드 AI 코파일럿 빌더, 멀티 에이전트, 화이트라벨링, 분석 |

## 네이티브 앱

| 이름 | 플랫폼 | 특징 |
|------|--------|------|
| Lazzy | macOS | 커서 위 플로팅, 800+ MCP, 로컬 전용 |
| Groovy | WhatsApp | WhatsApp 조율, 마케팅 분석 |
| Majordomo | iOS | 주거용 프록시 차별화 |
| Viola | 크로스플랫폼 | 음성 우선, 온디바이스 처리 |

## AI 에이전트 SNS / 커뮤니티

| 이름 | 설명 |
|------|------|
| [Moltbook](https://moltbook.com) | AI 에이전트 전용 소셜 네트워크 (Reddit 형식), 1.6M+ 에이전트, 인간은 관찰만 |
| [봇마당 (BotMadang)](https://botmadang.org) | 한국어 AI 에이전트 커뮤니티 (hunkim), MCP 서버 연동, OpenClaw 등록 가능 |

## 스킬 마켓플레이스

| 이름 | 설명 |
|------|------|
| [ClawHub](https://clawhub.ai) | OpenClaw 공식 스킬 레지스트리, 3,286+ 스킬, 벡터 검색 |
| [awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) | 커뮤니티 스킬 모음 |

## 오케스트레이션 & 멀티 에이전트

| 이름 | 설명 |
|------|------|
| [claw-empire](https://github.com/GreenSheep01201/claw-empire) | 픽셀아트 오피스 UI로 다중 에이전트(Claude Code, Codex CLI 등) 관리 |
| [openclaw-mission-control](https://github.com/abhi1693/openclaw-mission-control) | AI 에이전트 오케스트레이션 대시보드 |
| [AionUi](https://github.com/iOfficeAI/AionUi) | 로컬 Cowork 앱, Gemini CLI/Claude Code/Goose 등 통합 |
| [GasTown](https://github.com/steveyegge/gastown) | Steve Yegge의 멀티 에이전트 워크스페이스 — "Mayor"가 git 기반 "Polecat" 오케스트레이션 (10K 스타) |
| [Claw-Kanban](https://github.com/GreenSheep01201/Claw-Kanban) | 6컬럼 칸반으로 Claude Code, Codex CLI, Gemini CLI에 작업 라우팅, 실시간 터미널 모니터링 |

## 보안

### 알려진 위험

- **CVE-2026-25253** — 원클릭 RCE (CVSS 8.8), `gatewayUrl` 파라미터 검증 부재
- **CVE-2026-26322** — Gateway 도구 SSRF (CVSS 7.6), 내부 리소스로 서버사이드 요청
- **CVE-2026-26319** — Telnyx 웹훅 인증 부재 (CVSS 7.5)
- **CVE-2026-26329** — 브라우저 업로드 경로 탐색, 의도된 디렉터리 외부에 파일 쓰기
- **CVE-2026-27001** — 비살균 워크스페이스 경로를 통한 프롬프트 인젝션 (CWE-77)
- **CVE-2026-27484** — Discord 중재 권한 우회 (CVSS 4.3)
- **ClawHavoc 캠페인** — 800+ 악성 스킬 (ClawHub의 ~20%), AMOS 스틸러 배포
- **스킬을 통한 AMOS 배포** — 39개 악성 스킬이 기만적 SKILL.md와 base64 페이로드 사용 ([Trend Micro](https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html))
- **설정 파일 표적 인포스틸러** — Vidar 변종이 게이트웨이 토큰과 에이전트 컨텍스트 탈취 ([The Hacker News](https://thehackernews.com/2026/02/infostealer-steals-openclaw-ai-agent.html))
- **30,000~40,000+ 인터넷 노출 인스턴스** — 인증 미설정 상태로 운영 ([BitSight](https://www.bitsight.com/blog/openclaw-ai-security-risks-exposed-instances), [Palo Alto](https://www.paloaltonetworks.com/blog/network-security/why-moltbot-may-signal-ai-crisis/))
- **인기 스킬의 41.7%** — 커맨드 인젝션 또는 자격증명 노출 취약점 포함

### 보안 도구

| 이름 | 설명 |
|------|------|
| [SecureClaw](https://github.com/adversa-ai/secureclaw) | OWASP 정렬 플러그인/스킬 — 56개 감사 체크, 5개 강화 모듈, MITRE ATLAS 대응 |
| [ClawSec](https://www.sentinelone.com/blog/clawsec-hardening-openclaw-agents-from-the-inside-out/) | SentinelOne "스킬의 스킬" — 공급망 무결성, 보안 태세 강화, 제로트러스트 통신 |
| [ClawKeeper](https://github.com/rad-security/clawkeeper) | RAD Security 스캐너 — 5단계 42개 체크로 설정 오류, 자격증명, 네트워크 강화 |

### 보안 가이드 & 리소스

- [Microsoft: OpenClaw 안전하게 운영하기](https://www.microsoft.com/en-us/security/blog/2026/02/19/running-openclaw-safely-identity-isolation-runtime-risk/) — 신원, 격리, 런타임 위험
- [Cisco: 개인 AI 에이전트는 보안 악몽](https://blogs.cisco.com/ai/personal-ai-agents-like-openclaw-are-a-security-nightmare) — 위협 모델 분석
- [CrowdStrike: 보안팀이 알아야 할 것](https://www.crowdstrike.com/en-us/blog/what-security-teams-need-to-know-about-openclaw-ai-super-agent/) — 기업 관점
- [Malwarebytes: 안전하게 사용할 수 있을까?](https://www.malwarebytes.com/blog/news/2026/02/openclaw-what-is-it-and-can-you-use-it-safely) — 소비자 안전 가이드
- [Snyk: ClawHub 악성 캠페인](https://snyk.io/articles/clawdhub-malicious-campaign-ai-agent-skills/) — 공급망 공격 심층 분석
- [Adversa.ai: 취약점 & 강화](https://adversa.ai/blog/openclaw-security-101-vulnerabilities-hardening-2026/) — 강화 가이드
- [SecurityWeek: SecureClaw 도구](https://www.securityweek.com/openclaw-security-issues-continue-as-secureclaw-open-source-tool-debuts/) — 오픈소스 보안 스캐너
- [Palo Alto Networks: 다음 AI 보안 위기의 신호](https://www.paloaltonetworks.com/blog/network-security/why-moltbot-may-signal-ai-crisis/) — 영속 메모리 + 비신뢰 콘텐츠 + 개인 데이터의 "치명적 3요소"
- [Trend Micro: 에이전트 어시스턴트 위험](https://www.trendmicro.com/en_us/research/26/b/what-openclaw-reveals-about-agentic-assistants.html) — 5개 기업 중 1개가 IT 승인 없이 배포
- [Trend Micro: 악성 스킬이 AMOS 배포](https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html) — SKILL.md 소셜 엔지니어링 심층 분석
- [Kaspersky: OpenClaw 취약점](https://www.kaspersky.com/blog/openclaw-vulnerabilities-exposed/55263/) — 512건 감사 결과 (8건 크리티컬), 소비자 안전 가이드
- [Jamf: 내부 위협 분석](https://www.jamf.com/blog/openclaw-ai-agent-insider-threat-analysis/) — macOS 탐지 방법 및 대응
- [Infosecurity Magazine: 6개 새 취약점](https://www.infosecurity-magazine.com/news/researchers-six-new-openclaw/) — Endor Labs CVE 공개
- [The Register: 보안 두더지 잡기](https://www.theregister.com/2026/02/02/openclaw_security_issues/) — CVE-2026-25253 패치 + Moltbook DB 노출
- [VentureBeat: CISO 가이드](https://venturebeat.com/security/openclaw-agentic-ai-security-risk-ciso-guide) — 기업 보안 모델 격차
- [Immersive Labs: 기업 위험 평가](https://www.immersivelabs.com/resources/c7-blog/openclaw-what-you-need-to-know-before-it-claws-its-way-into-your-organization) — ~900 악성 스킬, 40K+ 노출 인스턴스
- [Permiso: OpenClaw 생태계 내부](https://permiso.io/blog/inside-the-openclaw-ecosystem-ai-agents-with-privileged-credentials) — AI 에이전트 "Rufio"가 824+ 악성 ClawHub 스킬 추적
- [CyberArk: 기업 신원 보안 재편](https://www.cyberark.com/resources/blog/how-autonomous-ai-agents-like-openclaw-are-reshaping-enterprise-identity-security) — AI 에이전트를 새로운 머신 아이덴티티로
- [TechCrunch: 에이전트가 받은편지함에서 폭주](https://techcrunch.com/2026/02/23/a-meta-ai-security-researcher-said-an-openclaw-agent-ran-amok-on-her-inbox/) — 실제 사고 보고

## 하드웨어

| 하드웨어 | 용도 | 참고 |
|----------|------|------|
| Mac Mini M4 Pro 64GB | 추천 셋업 — 통합 메모리로 로컬 LLM | [셋업 가이드](https://www.marc0.dev/en/blog/openclaw-mac-mini-the-complete-guide-to-running-your-own-ai-agent-in-2026-1770057455419) |
| Raspberry Pi | 저가형 대안 | [itsfoss 가이드](https://itsfoss.com/openclaw-alternatives/), [Goose+RPi](https://block.github.io/goose/blog/2026/02/06/rpi-openclaw-alternative/) |
| ESP32 | IoT 에이전트 (zclaw, MimiClaw) | 888KB~수MB, GPIO 제어 |
| 구형 Android폰 | droidclaw로 재활용 | — |

## 핵심 개념

- **Skills 기반 설정** — 설정 파일 대신 AI가 코드를 직접 수정 (NanoClaw 방식)
- **컨테이너 격리** — Docker / Apple Container로 에이전트 샌드박싱
- **MCP (Model Context Protocol)** — 13,000+ MCP 서버 생태계와 통합
- **Gateway 아키텍처** — 단일 프로세스가 세션/라우팅/채널 관리

## 기사 & 참고자료

### 개념 & 기원
- [Karpathy: "Claws" (원본 트윗)](https://x.com/karpathy/status/2024987174077432126) — "Claw는 LLM 에이전트 위의 새로운 레이어"
- [Karpathy: "Claws" 개념 정의](https://simonwillison.net/2026/Feb/21/claws/) — 원본 프레이밍 (Simon Willison 요약)
- [GIGAZINE: Claw AI 에이전트 레이어](https://gigazine.net/gsc_news/en/20260224-claw-ai-agent-layer/) — 해설
- [DEV: Claws란 무엇이고 왜 Mac Mini에서 돌리면 안 되는가](https://dev.to/setas/what-are-claws-and-why-you-shouldnt-run-them-on-your-mac-mini-4o1b) — 반론

### 생태계 & 지형도
- [Ry Walker: 2026 개인 AI 에이전트 전체 지형도 (38개 플랫폼)](https://rywalker.com/openclaw-alternatives-2026) — 종합 서베이
- [EvoAI Labs: Claw 광풍은 계속된다](https://evoailabs.medium.com/openclaw-nanobot-picoclaw-ironclaw-and-zeroclaw-this-claw-craziness-is-continuing-87c72456e6dc) — NanoClaw, PicoClaw, ZeroClaw, IronClaw 개요
- [Peter Woods: Claw AI 에이전트 패밀리](https://peterwoods.online/blog/the-claw-ai-agent-family) — 전체 Claw 계보 디렉터리
- [Axios: Gas Town, OpenClaw과 오픈소스 에이전트의 부상](https://www.axios.com/2026/02/24/agents-openclaw-moltbook-gastown) — 지형 분석 + Gartner 경고
- [Axios: AI의 센타우르스 시대가 실리콘밸리를 삼키다](https://www.axios.com/2026/02/23/ai-agents-openclaw-openai-anthropic) — 인간-AI 협업 전환

### 비즈니스 & 산업
- [TechCrunch: OpenClaw 창시자 OpenAI 합류](https://techcrunch.com/2026/02/15/openclaw-creator-peter-steinberger-joins-openai/) — Steinberger, "차세대 개인 에이전트" 리드
- [Peter Steinberger: OpenClaw, OpenAI 그리고 미래](https://steipete.me/posts/2026/openclaw) — 창시자 본인의 이야기
- [VentureBeat: ChatGPT 시대의 끝](https://venturebeat.com/technology/openais-acquisition-of-openclaw-signals-the-beginning-of-the-end-of-the) — 챗봇에서 영속 에이전트로의 전환
- [Bloomberg: OpenAI, OpenClaw 개발자 영입](https://www.bloomberg.com/news/articles/2026-02-15/openai-hires-openclaw-ai-agent-developer-peter-steinberg) — 인수 보도
- [CNBC: Clawdbot에서 OpenClaw까지](https://www.cnbc.com/2026/02/02/openclaw-open-source-ai-agent-rise-controversy-clawdbot-moltbot-moltbook.html) — 부상, 논란, 145K+ 스타
- [IBM: OpenClaw, Moltbook 그리고 미래](https://www.ibm.com/think/news/clawdbot-ai-agent-testing-limits-vertical-integration) — 기업 분석
- [Fortune: Moltbook "가장 흥미로운 인터넷"](https://fortune.com/2026/01/31/ai-agent-moltbot-clawdbot-openclaw-data-privacy-security-nightmare-moltbook-social-network/) — 문화적 영향
- [SalesforceDevops: 챗봇 시대는 끝났다](https://salesforcedevops.net/index.php/2026/02/20/ai-agents-awareness-february-2026/) — 패러다임 전환 분석

### Moltbook
- [Nature: 과학자들이 귀 기울이다](https://www.nature.com/articles/d41586-026-00370-w) — 1.6M 에이전트를 연구 기회로
- [IEEE Spectrum: 지저분한 미래의 전조](https://spectrum.ieee.org/moltbook-agentic-ai-agents-openclaw) — 프롬프트 인젝션, 에이전트 간 보안
- [NBC News: AI 에이전트 전용 소셜 네트워크](https://www.nbcnews.com/tech/tech-news/ai-agents-social-media-platform-moltbook-rcna256738) — 1월 31일 침해 보도
- [CNN: 우리가 두려워해야 할까?](https://edition.cnn.com/2026/02/03/tech/moltbook-explainer-scli-intl) — 주류 해설
- [Engadget: Moltbook이 도대체 뭔가?](https://www.engadget.com/ai/what-the-hell-is-moltbook-the-social-network-for-ai-agents-140000787.html) — 770K→1.6M 에이전트 성장

### 연구 & 학술
- [Alan Turing Institute: 야생의 에이전트 AI](https://cetas.turing.ac.uk/publications/agentic-ai-wild-lessons-moltbook-and-openclaw) — Moltbook + OpenClaw 정책 연구
- [The Conversation: 왜 새로워 보이는가 (사실은 아닌데)](https://theconversation.com/openclaw-and-moltbook-why-a-diy-ai-agent-and-social-media-for-bots-feel-so-new-but-really-arent-274744) — 역사적 맥락

### 실전 가이드
- [MacStories: 개인 AI 어시스턴트의 미래](https://www.macstories.net/stories/clawdbot-showed-me-what-the-future-of-personal-ai-assistants-looks-like/) — M4 Mac mini + Claude Opus 4.5 + Telegram
- [Coder: Blink + Mac Mini 보안 셋업](https://coder.com/blog/why-i-ditched-openclaw-and-built-a-more-secure-ai-agent-on-blink-mac-mini) — 보안 우선 접근
- [TechTarget: OpenClaw와 Moltbook 설명](https://www.techtarget.com/searchcio/feature/OpenClaw-and-Moltbook-explained-The-latest-AI-agent-craze) — 기업 중심 해설

### 플랫폼 충돌
- [VentureBeat: Google이 Antigravity 단속](https://venturebeat.com/orchestration/google-clamps-down-on-antigravity-malicious-usage-cutting-off-openclaw-users) — OpenClaw 사용으로 대량 계정 정지
- [The Register: Antigravity, 연산 부하에 추락](https://www.theregister.com/2026/02/23/google_antigravity_compute_burden/) — OAuth 통합이 Google 압도

### 참고
- [Wikipedia: OpenClaw](https://en.wikipedia.org/wiki/OpenClaw) — 백과사전 항목

## 기여하기

기여를 환영합니다! PR을 제출하기 전에 [기여 가이드라인](CONTRIBUTING.md)을 읽어주세요.

## 라이선스

[MIT](LICENSE)
