# AI Security Shared Responsibility Model

![mission badge](https://img.shields.io/badge/mission-Clarify_AI_Security_Ownership-8B5CF6) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Version](https://img.shields.io/badge/Version-1.1.0-blue.svg)](https://github.com/mikeprivette/ai-security-shared-responsibility/releases)

![AI Security Shared Responsibility Model Matrix](resources/images/AI%20Shared%20Responsibility%20Model.png)

## Clear security ownership for every AI deployment model

**[Quick Start](#quick-start) • [Framework](#the-framework) • [Deployment Models](#8-deployment-models) • [Security Domains](#16-security-domains) • [About](#about)**

---

## The Problem

AI is transforming industries at unprecedented pace, but security ownership remains unclear. Organizations deploying AI systems—from simple ChatGPT usage to complex custom models—lack clarity on who's responsible for what.

This gap creates risk. Without clear ownership boundaries, critical security tasks fall through the cracks. Data governance, model security, and compliance requirements become nobody's responsibility—until something goes wrong.

The shared responsibility model solved this for cloud computing. Now AI needs the same clarity.

## What This Is

A framework for understanding security responsibilities across AI deployments. Like cloud computing's shared responsibility model, this framework maps who owns what across **8 deployment models** and **16 security domains**.

Whether you're using ChatGPT, building custom models, or deploying autonomous agents, this framework shows exactly what you're responsible for—and what your providers handle.

## Quick Start

| If you are a... | Start here | Focus on |
|---|---|---|
| Security Leader | [Responsibility Matrix](framework/responsibility-matrix.md) | Understanding your obligations across all AI initiatives |
| AI Practitioner | [Deployment Models](framework/deployment-models.md) | Identifying which model fits your use case |
| Architect | [Security Domains](framework/security-domains.md) | Comprehensive security coverage areas |
| Getting Started | [This Section](#getting-started) | Step-by-step implementation guide |

## Why This Framework vs Others

Think of this as your **Day 1 framework**—what you need before diving into technical specifications.

| **Framework** | **Best For** | **When to Use** | **Limitation** |
|:---|:---|:---|:---|
| **🎯 This Framework** | Initial alignment & planning | Before deployment decisions | Less technical depth |
| **NIST AI RMF** | Comprehensive risk management | Mature AI programs | Assumes AI maturity |
| **CSA Models** | Cloud-specific implementations | Azure/AWS deployments | Too narrow for full AI landscape |
| **Microsoft Approach** | Azure ecosystem | Technical implementation | Vendor-specific |

Other frameworks assume you already know your deployment model and have organizational alignment. This framework helps you **build that alignment first**.

## The Framework

### Core Components

| Component | What It Covers | Key Insight |
|---|---|---|
| [8 Deployment Models](framework/deployment-models.md) | From SaaS to on-premises, agents to assistants | Each model has distinct security boundaries |
| [16 Security Domains](framework/security-domains.md) | Traditional + AI-specific (marked with ★) | New domains like agent governance are critical now |
| [Responsibility Matrix](framework/responsibility-matrix.md) | Complete 8x16 mapping | Visual guide to all responsibilities |

### Key Principles

- **No deployment is responsibility-free** - Even SaaS requires customer security efforts
- **Control = Responsibility** - More control means more security obligations
- **Shared requires coordination** - Both parties must fulfill their parts
- **New domains matter now** - Agent governance isn't a future problem

## Getting Started

1. **📍 Identify** your AI deployment model(s) using the [deployment models guide](framework/deployment-models.md)
2. **✅ Check** the [responsibility matrix](framework/responsibility-matrix.md) for your obligations
3. **📋 Review** the [security domains](framework/security-domains.md) to understand coverage areas
4. **🎯 Plan** improvements based on identified gaps

## 8 Deployment Models

Comprehensive coverage from simple SaaS to complex autonomous systems:

### Cloud-Based Models

- **SaaS AI Models** — ChatGPT, Claude, Gemini (Public & Private)
- **PaaS AI Models** — Azure OpenAI, AWS Bedrock, Google AI Platform
- **IaaS AI Models** — Custom models on cloud infrastructure

### Self-Managed & Specialized

- **On-Premises AI Models** — Local LLMs, air-gapped systems
- **SaaS Products with Embedded AI** — Salesforce Einstein, MS Copilot
- **Agentic AI Systems** — Autonomous multi-agent configurations
- **AI Coding Assistants** — GitHub Copilot, Cursor, Claude Code
- **MCP-Based Systems** — Persistent memory & context systems

[→ Full deployment models guide](framework/deployment-models.md)

## 16 Security Domains

Comprehensive coverage across traditional and emerging AI security areas:

### Traditional Domains (1-12)

- Application Security
- AI Ethics and Safety
- Model Security
- User Access Control
- Data Privacy
- Data Security
- Monitoring and Logging
- Compliance and Governance
- Supply Chain Security
- Network Security
- Infrastructure Security
- Incident Response

### Emerging AI Domains (13-16) ★

- **Agent Governance** — Control of autonomous AI agents
- **Code Generation Security** — AI-generated code protection
- **Context Pollution Protection** — Preventing false information injection
- **Multi-System Integration Security** — Cross-system AI orchestration

[→ Full security domains guide](framework/security-domains.md)

Securing an AI system is a multi-faceted challenge that requires attention to various domains and usage states. As the deployment models evolve, so too will these focus areas.

## Contributing

This framework improves with real-world input. Looking for:

- Implementation experiences
- Framework improvements
- Templates and tools

See [CONTRIBUTING.md](CONTRIBUTING.md) for details or open an issue to start a discussion.

## Evolution

- **August 2024**: [Original framework published](https://www.returnonsecurity.com/p/ai-security-shared-responsibility-model-navigating-risks-ai-deployment)
- **September 2025**: Expanded to 8 models and 16 domains, open sourced

The framework has grown from 4 to 8 deployment models and added 4 emerging security domains based on how AI security has evolved over the past year.

## About

Created by [Mike Privette](https://www.linkedin.com/in/mikeprivette/), founder of [Return on Security](https://returnonsecurity.com).

Questions? Open an issue to start a discussion.

## License

MIT - See [LICENSE](LICENSE) file.
