# AI Security Shared Responsibility Matrix

## Overview

This comprehensive 8x16 matrix maps security responsibilities across all deployment models and security domains.

## Quick Reference

**Responsibility Levels:**

- **Provider**: Primary responsibility lies with the AI service provider
- **Customer**: Primary responsibility lies with the customer organization
- **Shared**: Responsibilities are distributed between the provider and the customer
- **N/A**: Domain not typically relevant for this deployment model

## Complete Responsibility Matrix

| **Security Domain** | **SaaS AI** | **PaaS AI** | **IaaS AI** | **On-Premises** | **Embedded AI** | **Agentic AI** | **AI Coding** | **MCP Systems** |
|-----------------|---------|---------|---------|-------------|-------------|------------|-----------|-------------|
| **Application Security** | Provider | Shared | Customer | Customer | Shared | Customer | Customer | Customer |
| **AI Ethics and Safety** | Shared | Shared | Shared | Shared | Shared | Customer | Shared | Customer |
| **Model Security** | Provider | Provider | Provider | Shared | Provider | Shared | Provider | Shared |
| **User Access Control** | Customer | Customer | Customer | Customer | Customer | Customer | Customer | Customer |
| **Data Privacy** | Shared | Shared | Shared | Customer | Shared | Customer | Customer | Customer |
| **Data Security** | Provider | Shared | Shared | Customer | Provider | Customer | Provider | Customer |
| **Monitoring and Logging** | Shared | Shared | Customer | Customer | Provider | Customer | Provider | Customer |
| **Compliance and Governance** | Shared | Shared | Customer | Customer | Provider | Customer | Provider | Customer |
| **Supply Chain Security** | Provider | Shared | Shared | Customer | Provider | Shared | Provider | Customer |
| **Network Security** | Provider | Shared | Customer | Customer | Provider | Customer | Provider | Customer |
| **Infrastructure Security** | Provider | Shared | Customer | Customer | Provider | Customer | Provider | Customer |
| **Incident Response** | Shared | Shared | Customer | Customer | Shared | Customer | Shared | Customer |
| **Agent Governance** ★ | Shared | Shared | Customer | Customer | N/A | Customer* | N/A | Customer |
| **Code Generation Security** ★ | N/A | N/A | N/A | N/A | N/A | N/A | Customer* | N/A |
| **Context Pollution Protection** ★ | Shared | Shared | Customer | Customer | Shared | Shared | Customer | Customer* |
| **Multi-System Integration** ★ | Shared | Shared | Customer | Customer | Shared* | Shared | Customer | Customer* |

*★ = AI-Specific Domain | \* = Critical Focus Area for this deployment model*

## Understanding Shared Responsibilities

When marked as "Shared", responsibilities typically divide as follows:

**Provider Responsibilities:**

- Platform-level security controls
- Base infrastructure and features
- Core compliance certifications
- Model and service updates

**Customer Responsibilities:**

- Configuration and implementation
- Data governance and classification
- Usage policies and procedures
- Organizational compliance

## Key Patterns

**By Control Level:**

- **Most Provider Control**: SaaS AI, Embedded AI
- **Balanced Control**: PaaS AI, Agentic AI
- **Most Customer Control**: IaaS AI, On-Premises, MCP Systems

**By Complexity:**

- **Simplest**: SaaS AI (but still requires customer security efforts)
- **Moderate**: PaaS AI, Embedded AI
- **Complex**: IaaS AI, Agentic AI, AI Coding, MCP Systems
- **Most Complex**: On-Premises (full stack ownership)

**Critical Focus Areas by Deployment Model:**

- **Agentic AI**: Agent Governance requires special attention
- **AI Coding**: Code Generation Security is essential
- **MCP Systems**: Context Pollution and Multi-System Integration are critical
- **Embedded AI**: Multi-System Integration needs focus

## Quick Decision Guide

**Choose SaaS AI when:**

- Quick deployment is priority
- Limited security resources
- Standard use cases
- Acceptable to share infrastructure

**Choose PaaS AI when:**

- Need customization
- Have security expertise
- Require specific integrations
- Want balanced control

**Choose IaaS AI when:**

- Need full control over models
- Have strong security team
- Require specific configurations
- Custom deployment requirements

**Choose On-Premises when:**

- Maximum control required
- Air-gapped environments
- Regulatory requirements
- Complete ownership needed

## Using This Matrix

1. **Identify** your deployment model(s)
2. **Review** responsibilities for each security domain
3. **Assess** your current coverage
4. **Plan** to address gaps in "Customer" domains
5. **Coordinate** on "Shared" responsibilities

## Important Notes

- **No model is responsibility-free** - Even SaaS requires customer security efforts
- **Shared means coordination** - Both parties must fulfill their obligations
- **AI-specific domains (13-16)** - Represent emerging security challenges unique to AI systems
- **Evolution is normal** - Organizations often use multiple models simultaneously
