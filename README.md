# AI Security Shared Responsibility Model

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/mikeprivette/ai-security-shared-responsibility/releases)

## What This Is

A framework for understanding who's responsible for what when deploying AI systems. Just as cloud computing needed a shared responsibility model, AI deployments need clear security ownership delineation.

The framework maps security responsibilities across 8 deployment models and 16 security domains, helping organizations understand their obligations whether using ChatGPT, building custom models, or anything in between.

## The Need for a Shared Responsibility Model

AI is transforming industries at an unprecedented pace, but with great power comes great responsibility.

Shared responsibility, that is.

Enter the shared responsibility model for AI security—a framework designed to clarify the division of security responsibilities between AI service providers and the businesses that use them. This framework was designed to help security practitioners navigate the complex landscape of AI deployments in the current state of the world.

The shared responsibility model is not a new concept; it's been a cornerstone in cloud security for years. However, its application to AI security is relatively novel.

The idea is simple: both the service provider and the user have roles to play in securing AI systems. This division of labor ensures that all aspects of security are covered, reducing the risk of vulnerabilities and breaches.

As businesses increasingly adopt AI technologies, understanding and managing the associated risks is table stakes.

## Why This Framework vs Others

While frameworks from NIST, CSA, and Microsoft provide excellent technical depth for mature AI implementations, this framework serves a different purpose: **getting everyone on the same page first**.

Think of this as your **Day 1 framework** - what you need to understand before diving into technical specifications. Other frameworks assume you already have organizational alignment and are deep into AI development. This framework helps you **build that alignment**.

It's not that other frameworks are wrong - they're essential for later stages. But they're not where you start.

**Framework Comparisons:**
- **NIST AI RMF**: Excellent for risk management in established AI programs, but assumes significant AI maturity
- **CSA Models**: Great for cloud-specific implementations, but too narrow for the full AI landscape
- **Microsoft's Approach**: Comprehensive for Azure users, but vendor-specific and technically dense
- **This Framework**: Vendor-agnostic, deployment-model focused, speaks business language first

## The Framework

### Core Components

- **[8 Deployment Models](framework/deployment-models.md)** - From SaaS AI to on-premises, agentic systems to coding assistants. Detailed descriptions of each model and when to use them.
- **[16 Security Domains](framework/security-domains.md)** - Traditional security areas (1-12) plus emerging AI-specific domains (13-16, marked with ★). Comprehensive coverage of all security aspects.
- **[Responsibility Matrix](framework/responsibility-matrix.md)** - Complete 8x16 mapping showing who's responsible for what across every deployment model and security domain.

### Quick Navigation

| If you're a... | Start here |
|----------------|------------|
| **Security Leader** | [Responsibility Matrix](framework/responsibility-matrix.md) |
| **AI Practitioner** | [Deployment Models](framework/deployment-models.md) |
| **Architect** | [Security Domains](framework/security-domains.md) |

## Getting Started

1. **Identify** your AI deployment model(s) using the [deployment models guide](framework/deployment-models.md)
2. **Check** the [responsibility matrix](framework/responsibility-matrix.md) for your obligations
3. **Review** the [security domains](framework/security-domains.md) to understand coverage areas
4. **Plan** improvements based on identified gaps

## Key Principles

- **No deployment model is responsibility-free** - Even fully managed SaaS requires customer security efforts
- **Responsibilities increase with control** - More control = more security obligations
- **Shared means coordination** - Both parties must fulfill their parts
- **New domains matter now** - Agent governance and context pollution aren't future problems

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