# Sources — Using Azure Function to Trade on TradingView (2/3 & 3/3)

**Post files:** `azure-function-tradingview-2.html`, `azure-function-tradingview-3.html`
**Researched:** 2026-05-03
**Published dates embedded:** 2026-05-03T12:00:00.000Z (both posts)

---

## Sources

### Source 1
- **Title:** Using Azure Function to trade on TradingView (1/3)
- **URL:** https://medium.com/@chris10pher/using-azure-function-to-trade-on-tradingview-1-3-dc418668050a
- **Author / Publisher:** Chris Wan / Medium
- **Date published:** March 10, 2025
- **Key fact / quote used:** Original series premise — Azure Function App with Python HTTP trigger, Binance Spot client, `function_app.py` JSON body fields (symbol, side, price, total), deployment steps via VS Code.
- **Used in section:** Hook and code structure (both parts)

---

### Source 2
- **Title:** binance-tradingview-bot / function_app.py
- **URL:** https://github.com/c-wann/binance-tradingview-bot/blob/main/function_app.py
- **Author / Publisher:** c-wann (Chris Wan) / GitHub
- **Date published:** 2024 (last updated ~1 year ago)
- **Key fact / quote used:** Exact JSON keys read by `req.get_json()`: symbol, side, price, total; async lock pattern; `Client.new_order()` call with LIMIT / GTC params.
- **Used in section:** Part 2 — Pine Script payload structure; Part 3 — Azure Functions tool reference

---

### Source 3
- **Title:** How to configure webhook alerts
- **URL:** https://www.tradingview.com/support/solutions/43000529348-about-webhooks/
- **Author / Publisher:** TradingView Support
- **Date published:** Current (last updated 2025–2026)
- **Key fact / quote used:** TradingView sends POST to webhook URL with JSON content-type when message is valid JSON; fixed IP addresses (52.89.214.238, 34.212.75.30, 54.218.53.128, 52.32.178.7); 3-second timeout; 2FA required for webhooks.
- **Used in section:** Part 2 — Configuring the TradingView Webhook

---

### Source 4
- **Title:** About Azure Key Vault
- **URL:** https://learn.microsoft.com/en-us/azure/key-vault/general/overview
- **Author / Publisher:** Microsoft Learn
- **Date published:** December 3, 2025
- **Key fact / quote used:** Key Vault encrypts secrets at rest with FIPS 140-validated HSMs; managed identity access eliminates stored secrets; Key Vault references in App Settings resolve transparently at runtime.
- **Used in section:** Part 2 — Securing Your Endpoint and Testing the Flow

---

### Source 5
- **Title:** What is Microsoft Foundry?
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/what-is-foundry
- **Author / Publisher:** Microsoft Learn
- **Date published:** May 2, 2026
- **Key fact / quote used:** Foundry is a unified PaaS for enterprise AI; 1,900+ models; single Foundry resource replaces Hub + Azure OpenAI split; Responses API (Agents v2); platform is free to explore, pricing at deployment level.
- **Used in section:** Part 3 — What is Microsoft Foundry?

---

### Source 6
- **Title:** Agent tools overview for Foundry Agent Service
- **URL:** https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/tool-catalog
- **Author / Publisher:** Microsoft Learn
- **Date published:** April 23, 2026
- **Key fact / quote used:** Built-in Azure Functions tool lets agents call Azure Functions directly; Web Search tool for real-time web grounding; OpenAPI tool for external HTTP APIs; managed identity / Entra authentication removes need to manage secrets.
- **Used in section:** Part 3 — What is Microsoft Foundry? and Creating a Foundry Agent

---

### Source 7
- **Title:** Pine Script v5 — Alerts
- **URL:** https://www.tradingview.com/pine-script-docs/concepts/alerts
- **Author / Publisher:** TradingView Pine Script Documentation
- **Date published:** Current
- **Key fact / quote used:** `alert()` function fires webhook; `alert.freq_once_per_bar` prevents duplicate signals; embedding dynamic values via `str.tostring()` in JSON string concatenation.
- **Used in section:** Part 2 — Writing a Pine Script Strategy with Alert Conditions
