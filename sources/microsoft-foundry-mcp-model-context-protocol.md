# Sources: MCP (Model Context Protocol) in Microsoft Foundry

## Sources Used

### 1. Agent Tools Overview for Foundry Agent Service
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/tool-catalog
- **Date:** Last updated April 23, 2026
- **Key facts used:** MCP as first-class custom tool type, remote vs local MCP servers, Azure DevOps MCP Server in catalog, Azure Functions webhook endpoint (/runtime/webhooks/mcp), three auth options (key-based/Entra/OAuth OBO), Toolbox as MCP-compatible bundle, full built-in tool list (web search, code interpreter, file search, Azure AI Search, Azure Functions, etc.), structured inputs for runtime customization, private tool catalog, governance via AI gateway, key terminology (remote MCP server, local MCP server, toolbox, custom tools)

### 2. Introducing Toolboxes in Foundry (Dev Blog)
- **URL:** https://devblogs.microsoft.com/foundry/introducing-toolboxes-in-foundry/
- **Date:** April 22, 2026
- **Key facts used:** Toolbox public preview, problem solved (duplicated tool wiring across agents), single MCP-compatible endpoint, works with Agent Framework/LangGraph/GitHub Copilot SDK, versioning and promotion flow, centralized authentication management

### 3. Foundry Agent Service is GA (Dev Blog)
- **URL:** https://devblogs.microsoft.com/foundry/foundry-agent-service-ga/
- **Date:** March 6, 2026
- **Key facts used:** Expanded MCP authentication at GA, GA milestone for Agent Service including MCP support

### 4. Microsoft Foundry Agent Service Overview
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/agents/overview
- **Date:** Last updated April 29, 2026
- **Key facts used:** MCP as both built-in connectivity and custom server hosting pattern, tool authentication methods detail

### 5. Build and Register an MCP Server
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/mcp/build-your-own-mcp-server
- **Date:** 2026
- **Key facts used:** Guidance for building custom MCP servers for Foundry
