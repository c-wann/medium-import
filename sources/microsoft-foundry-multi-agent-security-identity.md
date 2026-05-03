# Sources: Multi-Agent Security, Identity, and Monitoring in Microsoft Foundry

## Sources Used

### 1. Microsoft Foundry Agent Service — Agent Identity Concepts
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/agent-identity
- **Date:** 2026
- **Key facts used:** Dedicated Entra managed identity per agent, credential-free Azure RBAC integration, least privilege enforcement at agent level, eliminates need for API keys/service principal sharing

### 2. Foundry Control Plane Overview
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/control-plane/overview
- **Date:** Last updated April 2026
- **Key facts used:** Fleet-level security dashboard, Defender/Purview/Policy integrations, anomaly detection, continuous evaluation for risk categories (sensitive data leakage, prohibited actions, task adherence), bulk remediation, scheduled automated red-teaming

### 3. Agent-to-Agent (A2A) Tool — Foundry Agent Service
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/agent-to-agent
- **Date:** 2026
- **Key facts used:** Structured authenticated cross-agent communication, typed endpoints prevent unauthorized insertion, per-agent Entra identity for audit logging, XPIA threat vector addressed

### 4. Foundry Agent Service is GA
- **URL:** https://devblogs.microsoft.com/foundry/foundry-agent-service-ga/
- **Date:** March 6, 2026
- **Key facts used:** End-to-end private networking at GA, BYO VNet for hosted agents, VM-isolated sandbox per session, private endpoints for dependent services (Azure AI Search, Cosmos DB, blob storage)

### 5. Multi-Agent Systems on Azure: Identity, Monitoring, and Security Guardrails
- **URL:** https://techcommunity.microsoft.com/discussions/azure-ai-foundry-discussions/multi-agent-systems-on-azure-identity-monitoring-and-security-guardrails/4504627
- **Date:** 2026
- **Key facts used:** Enterprise adoption context, security maturity curve for agent deployments, threat surfaces in multi-agent systems, content safety filters for XPIA detection

### 6. AI Red Teaming Agent for Foundry
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/evaluation/concepts/red-teaming
- **Date:** 2026
- **Key facts used:** Automated red-teaming as ongoing governance tool, agentic risk categories, Attack Success Rate (ASR) tracking, integration with continuous monitoring
