# AI Deployment Models

## Overview

This document provides detailed descriptions of the eight AI deployment models covered in the AI Security Shared Responsibility Framework. Each model has unique characteristics, risk profiles, and responsibility distributions between providers and organizations.

## Table of Contents

1. [SaaS AI Models](#1-saas-ai-models)
2. [PaaS AI Models](#2-paas-ai-models)
3. [IaaS AI Models](#3-iaas-ai-models)
4. [On-Premises AI Models](#4-on-premises-ai-models)
5. [SaaS Products with Embedded AI](#5-saas-products-with-embedded-ai)
6. [Agentic AI Systems](#6-agentic-ai-systems)
7. [AI Coding Assistants](#7-ai-coding-assistants)
8. [MCP-Based Systems](#8-mcp-based-systems)

---

## 1. SaaS AI Models

### Description
AI services consumed as software-as-a-service offerings, where the provider manages the infrastructure, model, and platform.

### Examples

**Public SaaS:**
- ChatGPT (OpenAI)
- Claude (Anthropic)
- Gemini (Google)
- Perplexity

**Private SaaS:**
- Enterprise ChatGPT
- Custom organizational AI deployments
- Dedicated tenant instances

### Risk Profile
- **Public SaaS**: High risk due to shared infrastructure and limited control
- **Private SaaS**: Moderate risk with enhanced isolation and controls

### Key Characteristics
- Minimal infrastructure management required
- Quick deployment and scaling
- Limited customization options
- Shared responsibility for data security

### Security Considerations
- Data residency and sovereignty
- API security and rate limiting
- Prompt injection protection
- Output filtering and validation
- User access management
- Data classification requirements

---

## 2. PaaS AI Models

### Description
Platform services that provide tools and infrastructure for deploying and managing AI models, offering a balance between control and convenience.

### Examples
- Azure OpenAI Service
- Google AI Platform
- AWS Bedrock
- IBM Watson
- Databricks ML

### Risk Profile
**Moderate** - Balanced control between provider and organization with customizable security configurations.

### Key Characteristics
- Model hosting and management tools
- Integration with cloud services
- Customizable deployment options
- Shared infrastructure with isolation

### Security Considerations
- Secure model deployment pipelines
- API gateway configuration
- Network isolation and segmentation
- Model versioning and rollback

---

## 3. IaaS AI Models

### Description
AI models deployed on cloud infrastructure services where organizations have control over the operating system and applications.

### Examples
- Custom models on AWS EC2
- AI workloads on Google Compute Engine
- Azure Virtual Machines running AI systems
- GPU clusters for model training
- Containerized AI deployments (Kubernetes)

### Risk Profile
**Moderate to High** - Greater organizational control and responsibility with higher potential for misconfigurations.

### Key Characteristics
- Full control over compute environment
- Custom security configurations
- Complex management requirements
- Flexible scaling options

### Security Considerations
- OS hardening and patching
- Container security
- Network security groups
- Secure model storage
- GPU security considerations

---

## 4. On-Premises AI Models

### Description
AI systems deployed entirely on internal hardware within the organization's data centers.

### Examples
- Locally hosted LLMs (LLaMA, Mistral)
- Edge AI deployments
- Air-gapped AI systems
- Private GPU clusters
- Embedded AI in IoT devices

### Risk Profile
**Variable** - Highest organizational responsibility with complete control over security measures.

### Key Characteristics
- Complete organizational control
- No external dependencies
- Maximum customization possible
- Full responsibility for all aspects

### Security Considerations
- Physical security
- Hardware supply chain
- Complete security stack management
- Disaster recovery planning
- Isolated network requirements

---

## 5. SaaS Products with Embedded AI

### Description
Traditional business applications that have added AI capabilities as features you can interact with and control. The AI is exposed as a feature you actively use, not just background functionality.

### Examples
- Salesforce Einstein (CRM where you can query AI for insights)
- Microsoft 365 Copilot (You prompt it to generate content)
- Slack AI (You ask it questions about your workspace)
- ServiceNow AI (You interact with AI for automation decisions)
- Adobe Firefly (You direct AI to create/modify designs)
- Notion AI (You prompt it to write, summarize, or analyze)

### Risk Profile
**Moderate to High** - AI capabilities embedded within business processes may access broader data sets than traditional features.

### Key Characteristics
- AI seamlessly integrated into familiar tools
- Users may not recognize AI-specific risks
- Data exposure through AI features
- Compliance complexity increases

### Security Considerations
- AI feature access controls
- Data classification for AI processing
- Prompt data leakage prevention
- Cross-application data access
- Shadow AI within approved tools

---

## 6. Agentic AI Systems

### Description
Autonomous AI systems capable of independent decision-making and action, often working in multi-agent configurations.

*Note: The definition of "agent" varies across the industry, but I think Daniel Miessler has a good definition set on [RAID (Real World AI Definitions)](https://danielmiessler.com/blog/raid-ai-definitions)

### Examples
- Multi-agent customer service systems
- Autonomous trading algorithms
- Supply chain optimization agents
- Cybersecurity response automation
- Robotic process automation with AI
- Autonomous research assistants

### Risk Profile
**High** - Autonomous capabilities create cascading risk potential and complex accountability challenges.

### Key Characteristics
- Independent decision-making
- Multi-agent coordination
- Complex action chains
- Escalation requirements
- Audit trail complexity

### Security Considerations
- Agent authority limits
- Decision audit trails
- Failsafe mechanisms
- Human-in-the-loop controls
- Multi-agent coordination security
- Preventing agent manipulation

---

## 7. AI Coding Assistants

### Description
AI systems that assist with software development tasks, from code generation to debugging and documentation.

### Examples
- GitHub Copilot
- Cursor
- Claude Code
- Amazon CodeWhisperer
- Tabnine
- Replit Ghostwriter
- JetBrains AI Assistant

### Risk Profile
**Moderate to High** - Code generation may introduce vulnerabilities and intellectual property concerns.

### Key Characteristics
- Real-time code suggestions
- Context-aware completions
- Cross-file understanding
- Integration with IDEs
- Learning from codebase patterns

### Security Considerations
- Secure coding practices enforcement
- Intellectual property protection
- License compliance verification
- Vulnerability introduction prevention
- Secrets and credential protection
- Supply chain security
- Code quality standards

---

## 8. MCP-Based Systems
> ["MCPs are other people's prompts pointing us to other people's code."](https://danielmiessler.com/blog/mcps-are-just-other-peoples-prompts-and-apis) - Daniel Miessler

### Description
Systems built on Model Context Protocol with persistent memory and context, enabling long-term relationship management.

### Examples
- Enterprise knowledge management systems
- Customer relationship management with AI memory
- Investment analysis platforms
- Research assistant systems
- Personal AI assistants with memory

### Risk Profile
**High** - Long-term data persistence and complex integrations create ongoing exposure risks.

### Key Characteristics
- Persistent memory across sessions
- Context accumulation over time
- Multiple data source integration
- Persona-based interactions
- Relationship tracking

### Security Considerations
- Memory integrity protection
- Context pollution prevention
- Cross-context isolation
- Long-term data governance
- Relationship data security
- Memory manipulation detection
- Persona separation enforcement

---

## AI-Enabled Products (Not Covered)

This framework does not cover products that use AI internally to power their functionality but don't expose AI features for users to directly interact with. In these products, AI operates entirely in the background - you cannot prompt it, query it, or control its behavior.

These products should still be evaluated from a security and legal standpoint regarding how they use your data for training their models. However, this is primarily a vendor management and compliance concern rather than a shared responsibility security model issue, since you have no control over the AI functionality.

**Examples of AI-Enabled (background AI) products:**
- **Otter.ai** - AI transcribes meetings automatically, but you can't interact with the AI
- **Superhuman** - AI powers email features and writing, but you don't prompt or control it directly
- **Grammarly** (basic) - AI checks grammar automatically, no user AI interaction
- **Spotify** - AI creates playlists, but you don't directly engage with it
- **LinkedIn** - AI suggests connections, but operates in the background

For these products, focus on:
- Standard vendor risk assessments
- Data processing agreements
- Terms of service review
- Privacy policy evaluation
- Compliance certification verification

---

## Deployment Model Selection Guide

### Decision Factors

1. **Data Sensitivity**
   - High: On-premises or Private SaaS
   - Medium: PaaS or IaaS
   - Low: Public SaaS

2. **Control Requirements**
   - Maximum: On-premises
   - High: IaaS
   - Moderate: PaaS
   - Low: SaaS

3. **Resource Availability**
   - Limited: SaaS or Embedded AI
   - Moderate: PaaS
   - Extensive: IaaS or On-premises

4. **Use Case Complexity**
   - Simple: SaaS or Embedded AI
   - Moderate: PaaS or Coding Assistants
   - Complex: IaaS, Agentic, or MCP Systems

5. **Compliance Requirements**
   - Strict: On-premises or Private deployments
   - Moderate: PaaS with compliance features
   - Basic: Public SaaS with agreements

### Hybrid Deployments

Many organizations use multiple deployment models simultaneously:

- **Development vs. Production**: SaaS for development, on-premises for production
- **Tiered Approach**: Public SaaS for general use, private deployment for sensitive data
- **Gradual Migration**: Starting with SaaS, moving to PaaS/IaaS as needs mature
- **Specialized Systems**: Different models for different use cases

## Responsibility Overview

For security responsibilities across all deployment models and domains, see the [AI Security Shared Responsibility Matrix](responsibility-matrix.md).
