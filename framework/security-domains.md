# Security Domains in AI Systems

## Overview

This document details the 16 security domains that comprise the AI Security Shared Responsibility Framework. These domains represent the comprehensive security considerations required for safe AI deployment.

Domains 1-12 are traditional security areas adapted for AI systems, while domains 13-16 (marked with ★) are emerging security challenges unique to modern AI deployments.

---

## Security Domains

### 1. Application Security

**Focus**: Security of AI applications and their interfaces

**What This Actually Means**: This is about securing the actual application that uses AI - the websites, APIs, and interfaces that users interact with. It covers everything from input validation to protecting against attacks targeting the application layer.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI secures ChatGPT's web interface and API endpoints completely
- **PaaS AI**: You configure API rate limits and input validation on Azure OpenAI Service
- **IaaS AI**: You build and secure the entire application layer on AWS EC2
- **On-Premises**: Complete application security from authentication to encryption
- **Embedded AI**: Salesforce secures Einstein, you configure feature access and usage
- **Agentic AI**: You secure agent interfaces and define action boundaries
- **AI Coding**: You secure your development environment and code repositories
- **MCP Systems**: You protect context system interfaces and access points

**Responsibility Varies**:
- **Provider (SaaS)**: Platform owns the application completely
- **Shared (PaaS, Embedded)**: Provider supplies platform security, customer configures usage
- **Customer (IaaS, On-Premises, Agentic, AI Coding, MCP)**: You own all application security

**Key Considerations**:
The main challenge shifts from basic security (in SaaS) to comprehensive application protection (in self-managed systems). Critical areas include prompt injection prevention, output validation, API security, and session management. For AI-specific applications, focus on context window security and token limit enforcement.

---

### 2. AI Ethics and Safety

**Focus**: Responsible AI deployment and bias prevention

**What This Actually Means**: This covers both the ethical design of AI systems and their safe usage. It's about ensuring AI doesn't cause harm, perpetuate bias, or get used for inappropriate purposes - a responsibility that can't be fully outsourced.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI prevents harmful outputs, but you choose appropriate use cases
- **PaaS AI**: Azure provides safety controls, you implement ethical guidelines
- **IaaS AI**: You configure all safety measures and ethical boundaries on your models
- **On-Premises**: Complete ownership of ethical AI implementation and safety
- **Embedded AI**: Salesforce ensures Einstein's base safety, you control feature usage
- **Agentic AI**: You define all ethical boundaries for autonomous agent actions
- **AI Coding**: GitHub ensures Copilot safety, you review generated code for appropriateness
- **MCP Systems**: You own ethical use of persistent memory and long-term context

**Responsibility Varies**:
- **Shared (SaaS, PaaS, IaaS, On-Premises, Embedded, AI Coding)**: Providers ensure base model safety, customers ensure appropriate usage
- **Customer (Agentic, MCP)**: Critical autonomous and persistent systems require full customer ownership

**Key Considerations**:
Ethics and safety are inherently shared because providers ensure base model safety and training ethics, while customers are responsible for appropriate use case selection, deployment context, and ongoing ethical usage. Even in provider-managed models, customers choose how to apply the AI. Focus areas include harmful content prevention, bias detection, explainability, and human oversight mechanisms.

---

### 3. Model Security

**Focus**: Protection of AI models from attacks and theft

**What This Actually Means**: This is about protecting the AI model itself - preventing extraction, poisoning, or manipulation. It includes securing model weights, preventing adversarial attacks, and protecting intellectual property.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI protects GPT models from extraction and attacks
- **PaaS AI**: Azure protects base models, you secure any fine-tuning
- **IaaS AI**: Provider-supplied models (LLaMA, Mistral) come with built-in protections
- **On-Premises**: Provider models have base security, you handle deployment protection
- **Embedded AI**: Salesforce protects Einstein's models completely
- **Agentic AI**: Shared between base model security and agent-specific protections
- **AI Coding**: GitHub protects Copilot's code generation models
- **MCP Systems**: Complex memory model protection shared with provider

**Responsibility Varies**:
- **Provider (SaaS, PaaS, IaaS, Embedded, AI Coding)**: Provider protects base models
- **Shared (On-Premises, Agentic, MCP)**: Provider supplies secure models, customer handles deployment

**Key Considerations**:
Most organizations deploy pre-trained foundation models (LLaMA, Mistral, GPT variants) rather than building custom models from scratch. The model provider has built-in protections against extraction attacks and other model-level vulnerabilities, while the customer handles deployment security, access controls, and storage protection.

---

### 4. User Access Control

**Focus**: Authentication and authorization for AI systems

**What This Actually Means**: This is about controlling who in your organization can access AI systems and at what permission level. It's fundamentally about organizational decisions - who should have access to what.

**Examples by Deployment Model**:
- **SaaS AI**: You decide who gets ChatGPT Enterprise licenses and permissions
- **PaaS AI**: You configure who can access Azure OpenAI in your organization
- **IaaS AI**: You implement complete IAM for your AI infrastructure
- **On-Premises**: Full control over all access management systems
- **Embedded AI**: You control who accesses AI features within applications
- **Agentic AI**: Critical - you define who can control and monitor agents
- **AI Coding**: You manage developer access to AI coding assistants
- **MCP Systems**: You control access to persistent memory and context systems

**Responsibility Varies**:
- **Customer (All Models)**: Access control is always a customer responsibility

**Key Considerations**:
While providers may supply authentication mechanisms and IAM tools, the customer always owns the fundamental decisions about WHO in their organization gets access and at WHAT permission levels. This remains a customer responsibility across all deployment models. Key areas include API key management, prompt history protection, and model access permissions.

---

### 5. Data Privacy

**Focus**: Protection of personal and sensitive information

**What This Actually Means**: This covers how personal and sensitive data is handled when processed by AI systems. It includes consent, data minimization, and compliance with privacy regulations like GDPR.

**Examples by Deployment Model**:
- **SaaS AI**: ChatGPT processes data per OpenAI policies, you ensure consent
- **PaaS AI**: Azure provides privacy controls, you implement data governance
- **IaaS AI**: You implement all privacy controls for data processing
- **On-Premises**: Complete control over data privacy implementation
- **Embedded AI**: Salesforce handles Einstein privacy, you manage customer data consent
- **Agentic AI**: You control all agent data handling and privacy
- **AI Coding**: You manage code repository and development data privacy
- **MCP Systems**: Critical - long-term memory requires careful privacy management

**Responsibility Varies**:
- **Shared (SaaS, PaaS, IaaS, Embedded)**: Provider handles platform privacy, customer manages data classification and consent
- **Customer (On-Premises, Agentic, AI Coding, MCP)**: Full privacy control and responsibility

**Key Considerations**:
Privacy responsibilities depend on who processes the data and for what purpose. Cloud services create shared obligations under regulations like GDPR, where both processor and controller have duties. Key areas include data anonymization, consent management, and right to erasure implementation.

---

### 6. Data Security

**Focus**: Confidentiality, integrity, and availability of data

**What This Actually Means**: This is about protecting data at rest and in transit - encryption, access controls, and preventing data loss. It covers both the data fed into AI systems and the outputs they generate.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI handles all encryption and storage security
- **PaaS AI**: Azure provides encryption tools, you configure data handling
- **IaaS AI**: Cloud provider supplies infrastructure encryption, you implement the rest
- **On-Premises**: You own all aspects of data security
- **Embedded AI**: Application provider handles data security completely
- **Agentic AI**: You secure all agent-processed data
- **AI Coding**: Provider secures the service, you secure your code
- **MCP Systems**: You protect all persistent context data

**Responsibility Varies**:
- **Provider (SaaS, Embedded, AI Coding)**: Full platform data security
- **Shared (PaaS, IaaS)**: Provider supplies tools, customer configures
- **Customer (On-Premises, Agentic, MCP)**: Complete data security ownership

**Key Considerations**:
Data security in AI includes unique challenges like vector database protection, prompt/response storage security, and training data protection. The level of control determines responsibility - managed services handle encryption automatically while self-managed systems require comprehensive data protection strategies.

---

### 7. Monitoring and Logging

**Focus**: Detection and response to security events

**What This Actually Means**: This is about tracking what's happening in your AI systems - who's using them, how they're being used, and detecting when something goes wrong. It's essential for both security and compliance.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI monitors ChatGPT, provides usage reports
- **PaaS AI**: Azure provides monitoring tools, you analyze AI usage patterns
- **IaaS AI**: You implement complete monitoring for your AI infrastructure
- **On-Premises**: Full monitoring stack ownership and management
- **Embedded AI**: Application provider monitors, shares relevant logs
- **Agentic AI**: Critical - you must monitor all agent actions and decisions
- **AI Coding**: Provider monitors service health, you track usage
- **MCP Systems**: You monitor context evolution and memory changes

**Responsibility Varies**:
- **Provider (Embedded, AI Coding)**: Provider handles monitoring
- **Shared (SaaS, PaaS)**: Provider generates logs, customer must analyze for their use cases
- **Customer (IaaS, On-Premises, Agentic, MCP)**: Complete monitoring ownership

**Key Considerations**:
AI-specific monitoring includes tracking model drift, unusual query patterns, token usage anomalies, and prompt injection attempts. In shared scenarios, providers can log activity but can't know what's normal for your specific use case - that analysis is always your responsibility.

---

### 8. Compliance and Governance

**Focus**: Adherence to regulations and organizational policies

**What This Actually Means**: This covers meeting regulatory requirements (like GDPR, HIPAA, or the EU AI Act) and internal governance policies. It includes documentation, audit trails, and demonstrating compliance.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI provides compliance certifications for the platform
- **PaaS AI**: Azure offers compliance tools, you implement organizational policies
- **IaaS AI**: You ensure all compliance for your AI deployment
- **On-Premises**: Complete compliance ownership and implementation
- **Embedded AI**: Application vendor handles their compliance scope
- **Agentic AI**: You ensure agent operations meet all compliance requirements
- **AI Coding**: Provider maintains service compliance, you handle code compliance
- **MCP Systems**: You manage long-term data governance and retention compliance

**Responsibility Varies**:
- **Provider (Embedded, AI Coding)**: Platform compliance certifications
- **Shared (SaaS, PaaS)**: Provider certifies platform, customer ensures organizational compliance
- **Customer (IaaS, On-Premises, Agentic, MCP)**: Full compliance responsibility

**Key Considerations**:
Compliance in AI includes emerging regulations like the EU AI Act, alongside traditional requirements. Providers can only certify what they control - organizational use cases, data handling, and specific industry requirements are always customer responsibilities.

---

### 9. Supply Chain Security

**Focus**: Security of AI development and deployment pipeline

**What This Actually Means**: This covers the security of all components that make up your AI system - from models and training data to libraries and dependencies. It's about knowing and trusting what goes into your AI stack.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI manages all dependencies and model provenance
- **PaaS AI**: Azure manages platform components, you handle custom additions
- **IaaS AI**: Cloud provider supplies secure infrastructure, you manage the AI stack
- **On-Premises**: You verify and secure the entire supply chain
- **Embedded AI**: Application vendor manages their complete supply chain
- **Agentic AI**: Complex - both agent framework and custom components need vetting
- **AI Coding**: GitHub manages Copilot's training data and model pipeline
- **MCP Systems**: You vet all plugins and extensions in the context system

**Responsibility Varies**:
- **Provider (SaaS, Embedded, AI Coding)**: Complete supply chain management
- **Shared (PaaS, IaaS, Agentic)**: Split between platform and custom components
- **Customer (On-Premises, MCP)**: Full supply chain responsibility

**Key Considerations**:
AI supply chain includes unique elements like model provenance, training data sources, and third-party model validation. The rise of foundation models means most organizations are part of a model supply chain they don't fully control, making vendor assessment critical.

---

### 10. Network Security

**Focus**: Protection of network communications and infrastructure

**What This Actually Means**: This covers securing how AI systems communicate - API calls, model serving endpoints, and data transfers. It includes firewalls, encryption in transit, and DDoS protection.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI secures all ChatGPT network infrastructure
- **PaaS AI**: Azure provides network backbone, you configure virtual networks
- **IaaS AI**: You configure all network security for your AI systems
- **On-Premises**: Complete network security ownership
- **Embedded AI**: Application provider handles all networking
- **Agentic AI**: You secure all agent-to-agent and external communications
- **AI Coding**: Provider secures service connectivity
- **MCP Systems**: You protect all API endpoints and context system communications

**Responsibility Varies**:
- **Provider (SaaS, Embedded, AI Coding)**: Complete network security
- **Shared (PaaS)**: Provider supplies infrastructure, customer configures
- **Customer (IaaS, On-Premises, Agentic, MCP)**: Full network security ownership

**Key Considerations**:
AI-specific network security includes protecting model serving endpoints, securing federated learning communications, and managing API rate limits. High-bandwidth requirements for model serving create unique challenges compared to traditional applications.

---

### 11. Infrastructure Security

**Focus**: Security of underlying compute and storage resources

**What This Actually Means**: This is about securing the physical and virtual infrastructure that AI runs on - servers, GPUs, storage systems, and virtualization layers. It includes everything from physical security to container isolation.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI secures all infrastructure for ChatGPT
- **PaaS AI**: Azure secures physical infrastructure, you configure virtual resources
- **IaaS AI**: Cloud provider secures hardware, you manage VMs and containers
- **On-Premises**: You own everything from physical security to virtualization
- **Embedded AI**: Application provider manages all infrastructure
- **Agentic AI**: You secure the infrastructure agents run on
- **AI Coding**: Provider manages service infrastructure completely
- **MCP Systems**: You secure infrastructure for persistent context storage

**Responsibility Varies**:
- **Provider (SaaS, PaaS, Embedded, AI Coding)**: Physical infrastructure and platform
- **Customer (IaaS, On-Premises, Agentic, MCP)**: Virtual infrastructure and above

**Key Considerations**:
AI infrastructure has unique requirements including GPU security, high-memory system protection, and distributed training security. The massive compute requirements of AI create new attack surfaces and require specialized security controls.

---

### 12. Incident Response

**Focus**: Preparation for and response to security incidents

**What This Actually Means**: This is about what happens when something goes wrong - detecting incidents, responding quickly, and learning from them. It includes having plans, communication protocols, and recovery procedures.

**Examples by Deployment Model**:
- **SaaS AI**: OpenAI handles platform incidents, notifies you of impacts
- **PaaS AI**: Azure responds to platform issues, you handle application incidents
- **IaaS AI**: You manage all incident response for your AI systems
- **On-Premises**: Complete incident response ownership
- **Embedded AI**: Vendor handles app incidents, coordinates on AI-specific issues
- **Agentic AI**: You respond to all agent-related incidents
- **AI Coding**: GitHub handles service incidents, you manage code security events
- **MCP Systems**: You handle all context system compromise incidents

**Responsibility Varies**:
- **Shared (SaaS, PaaS, Embedded, AI Coding)**: Coordination required between provider and customer
- **Customer (IaaS, On-Premises, Agentic, MCP)**: Full incident response ownership

**Key Considerations**:
AI-specific incidents include model compromise, data poisoning, prompt injection attacks, and output manipulation. Even in shared scenarios, the customer must detect and respond to attacks targeting their specific use case. Coordination is critical when responsibilities are shared.

---

### 13. Agent Governance ★

**Focus**: Control and oversight of autonomous AI agents

**What This Actually Means**: This is about managing AI systems that can take actions autonomously - setting boundaries, requiring approvals for certain actions, and maintaining human oversight. It's critical for systems that can make decisions or take actions without human intervention.

**Examples by Deployment Model**:
- **SaaS AI**: ChatGPT plugins require governance of automated actions
- **PaaS AI**: Azure AI agents need configured boundaries and oversight
- **IaaS AI**: You define all governance for custom agent deployments
- **On-Premises**: Complete control over agent governance frameworks
- **Embedded AI**: N/A - Embedded AI typically isn't autonomous
- **Agentic AI**: Critical - full governance of autonomous agent systems
- **AI Coding**: N/A - Code generation isn't autonomous
- **MCP Systems**: You govern how persistent context influences decisions

**Responsibility Varies**:
- **Shared (SaaS, PaaS)**: Provider supplies controls, customer sets policies
- **Customer (IaaS, On-Premises, Agentic, MCP)**: Full governance responsibility
- **N/A (Embedded, AI Coding)**: Not typically applicable

**Key Considerations**:
Agent governance requires defining acceptable autonomous actions, establishing escalation triggers, and maintaining audit trails. The key challenge is balancing automation benefits with risk management. Critical controls include authority limits, human intervention points, and emergency stop mechanisms.

---

### 14. Code Generation Security ★

**Focus**: Security of AI-generated code and development assistance

**What This Actually Means**: This is about ensuring AI-generated code is secure, compliant, and doesn't introduce vulnerabilities. It includes reviewing generated code, checking licenses, and preventing sensitive data exposure.

**Examples by Deployment Model**:
- **SaaS AI**: N/A - Not primarily for code generation
- **PaaS AI**: N/A - Not typically used for code generation
- **IaaS AI**: N/A - Infrastructure focus, not code generation
- **On-Premises**: N/A - Unless specifically deployed for code generation
- **Embedded AI**: N/A - Embedded in applications, not development tools
- **Agentic AI**: N/A - Agents don't typically generate code
- **AI Coding**: Critical - GitHub Copilot, Cursor, and similar require code security
- **MCP Systems**: N/A - Context systems don't generate code

**Responsibility Varies**:
- **Customer (AI Coding)**: Full responsibility for code security and review
- **N/A (All others)**: Not applicable to these deployment models

**Key Considerations**:
Code generation security is unique to AI coding assistants. Key challenges include detecting vulnerabilities in generated code, ensuring license compliance, preventing secrets in code, and maintaining code quality standards. All code must be reviewed before production use.

---

### 15. Context Pollution Protection ★

**Focus**: Preventing injection of false or misleading information into AI systems

**What This Actually Means**: Think of this as protecting the AI's "understanding" from being corrupted. It's like prompt injection but broader, and includes any attempt to pollute what the AI knows or believes.

**Examples by Deployment Model**:
- **SaaS AI**: Attacker tries to make ChatGPT believe false "facts" through conversation manipulation
- **PaaS AI**: Someone poisons your fine-tuning dataset on Azure OpenAI
- **IaaS AI**: Malicious data inserted into your vector database affecting RAG responses
- **On-Premises**: Similar to IaaS but includes physical access risks
- **Embedded AI**: Users manipulating Salesforce Einstein through crafted inputs
- **Agentic AI**: False information fed to agents affecting autonomous decisions
- **AI Coding**: Malicious code patterns injected to be learned and reproduced
- **MCP Systems**: Critical - poisoned context persists across all future sessions

**Responsibility Varies**:
- **Shared (SaaS, PaaS, Embedded, Agentic)**: Providers offer input filters, customers must validate use cases
- **Customer (IaaS, On-Premises, AI Coding, MCP)**: You control the full stack and all protections

**Key Considerations**:
The main challenge is detecting sophisticated manipulation while maintaining memory integrity. Critical controls include input validation, source verification, and context monitoring. For MCP systems especially, implement memory versioning since pollution persists across sessions.

---

### 16. Multi-System Integration Security ★

**Focus**: Security across interconnected AI systems and traditional applications

**What This Actually Means**: This is about securing the connections when AI systems talk to other systems - both AI and traditional. It covers API security, data flow protection, and managing the complexity of integrated systems.

**Examples by Deployment Model**:
- **SaaS AI**: ChatGPT calling plugins or external APIs needs secure integration
- **PaaS AI**: Azure OpenAI connecting to your databases and applications
- **IaaS AI**: Your custom models integrating with other services
- **On-Premises**: Your AI systems connecting to internal applications
- **Embedded AI**: Critical - AI features deeply integrated with application ecosystem
- **Agentic AI**: Agents coordinating with each other and external services
- **AI Coding**: Copilot accessing repositories and development tools
- **MCP Systems**: Critical - multiple context sources and system connections

**Responsibility Varies**:
- **Shared (SaaS, PaaS, Embedded, Agentic)**: Provider supplies integration tools, customer secures usage
- **Customer (IaaS, On-Premises, AI Coding, MCP)**: Full integration security ownership

**Key Considerations**:
Multi-system integration creates complex attack surfaces where vulnerabilities in one system can cascade. Key challenges include securing AI-to-AI communications, managing data flows across trust boundaries, and maintaining consistent security policies. Critical for systems with broad integration scope.

---

## Using This Guide

This guide maps to the [Responsibility Matrix](responsibility-matrix.md) which shows specific responsibility assignments (Provider/Shared/Customer) for each domain across all 8 deployment models. Use both documents together to understand:

1. **What** each security domain covers (this document)
2. **Who** is responsible in your deployment model (responsibility matrix)
3. **How** to implement based on your specific needs

Remember: Even in the most managed scenarios, customers retain significant security responsibilities. Understanding these domains helps you identify and address your obligations regardless of deployment model.