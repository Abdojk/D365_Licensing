# Copilot, Agents & AI Licensing in Dynamics 365

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 ships with two related but distinct classes of AI: **Copilot** — the AI assistant embedded inside each application — and **Dynamics 365 agents** — autonomous services that carry out tasks and consume a metered currency called **Copilot Credits**. This page explains what is included with a Dynamics 365 license, what requires Copilot Credits, and when a separate Microsoft 365 Copilot license is needed.

## Copilot included with Dynamics 365 apps

The **Copilot in Dynamics 365** experiences are built into the applications and appear as included capabilities in the app entitlement tables — for example *Copilot in Dynamics 365 Sales* is included with Sales Enterprise and Sales Premium,[LG p.51] *Copilot in Dynamics 365 Customer Service* is included with Customer Service Enterprise and Premium,[LG p.26] and *Use of Microsoft Copilot in Dynamics 365 Business Central* is part of the Business Central license.[LG p.10]

These embedded Copilot features include capabilities such as record summarization, record catch-up on recent changes, meeting preparation, email assistance, and news updates.[Learn: Copilot in Dynamics 365 Sales overview](https://learn.microsoft.com/dynamics365/sales/copilot-overview) They are a product feature of the licensed application and do not, by themselves, consume Copilot Credits.

### When Microsoft 365 Copilot is required for premium features

Some AI experiences reach beyond the Dynamics 365 application into the broader Microsoft 365 surface, and those premium capabilities require a separate **Microsoft 365 Copilot** license:

- **Sales agent (Sales Copilot).** Sales Enterprise, Sales Premium, and Microsoft Relationship Sales include the *basic* features of the Sales agent; to use the *premium* features you must buy the Microsoft 365 Copilot license.[Learn: Buy Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales)
- **Microsoft 365 Copilot in a Dynamics 365 app.** To use the Microsoft 365 Copilot feature in a Dynamics 365 app, users must have a Dynamics 365 Enterprise or Premium license — but to get the full capabilities of Work IQ beyond Dataverse grounding, a Microsoft 365 Copilot license is required.[Learn: Use Microsoft 365 Copilot in Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/microsoft-365-copilot-chat-in-sales)

The Sales agent in Microsoft 365 Copilot is positioned as the evolution of the in-app Copilot experience: it works across Microsoft 365 apps (Teams, Outlook, Word, Excel) and Dynamics 365 Sales, whereas Copilot in Dynamics 365 Sales is built into the Sales application itself.[Learn: FAQ about Copilot in Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/sales-copilot-faq)

## Dynamics 365 agents

Dynamics 365 agents are intelligent services within the Dynamics 365 applications that provide AI-driven automation and orchestration as part of the licensed product functionality. They are available in:[LG p.58]

- Dynamics 365 Customer Service
- Dynamics 365 Contact Center
- Dynamics 365 Field Service
- Dynamics 365 Sales
- Dynamics 365 Business Central
- Dynamics 365 Enterprise Resource Planning (ERP)

**Copilot Credits are required for any Dynamics 365 agents usage, and users must also hold a valid license for the corresponding application.**[LG p.58]

## Agents and Copilot Credits

**Copilot Credits are the common currency across Copilot Studio capabilities** and are required for executing and extending Dynamics 365 agents. The number of credits decremented for each response or action depends on the complexity of the task completed by the agent.[LG p.58] Microsoft Learn frames a Copilot Credit as a single interaction between a user and an agent — one unit of consumption for a request that prompts a response or action.[Learn: Manage Copilot Studio credits and capacity](https://learn.microsoft.com/power-platform/admin/manage-copilot-studio-messages-capacity)

Copilot Credits are offered through several mechanisms:[LG p.58]

- The **Copilot Studio pay-as-you-go meter**
- The **Copilot Studio Copilot Credit pack subscription license**
- The **Copilot Credit Pre-Purchase Plan**

In addition, Copilot Credit consumption may be offset through the **Microsoft Agent Pre-Purchase Plan**, which provides **Agent Commit Units** to reconcile eligible Copilot Credit usage.[LG p.58]

Microsoft Learn describes the same two billing models — **prepaid capacity** (Copilot Studio message/credit pack subscriptions) and **pay-as-you-go** (billed for actual consumption, requires an Azure subscription). Prepaid capacity is consumed first, and both models require linking the Dynamics 365 environment to a Power Platform environment.[Learn: Manage consumption-based billing and capacity](https://learn.microsoft.com/dynamics365/customer-service/administer/setup-pay-as-you-go) Copilot Credit capacity is enforced monthly, and unused credits do not carry over month to month.[LG p.65]

> Note: On September 1, 2025 the common currency for agents changed from *messages* to *Copilot Credits*, with no change to the quantity per prepaid pack or the pay-as-you-go rate.[Learn: Copilot Studio licensing](https://learn.microsoft.com/microsoft-copilot-studio/billing-licensing)

### Copilot Credits included with Premium licenses

Dynamics 365 **Sales Premium, Customer Service Premium, Finance Premium, and Supply Chain Management Premium** licenses each include **1,000 Copilot Credits per user/month**. These credits can be used to run prebuilt Dynamics 365 agents or custom agents built with Microsoft Copilot Studio.[LG p.58]

Credits **accrue at the tenant level** and should be **allocated to environments** to prevent them being used in other workloads — for example, to prevent Finance agents from running on Copilot Credits accrued from Sales Premium licenses.[LG p.58]

### Copilot Credit entitlements by license

| Dynamics 365 USL | Copilot Credits required / included |
|---|---|
| **Contact Center** — Digital | Not included, sold separately |
| **Contact Center** — Voice | Not included, sold separately |
| **Contact Center** — Digital + Voice | Not included, sold separately |
| **Customer Service** — Professional | Not included, sold separately |
| **Customer Service** — Enterprise | Not included, sold separately |
| **Customer Service** — Premium | 1,000 Copilot Credits included |
| **Finance** — Finance | Not included, sold separately |
| **Finance** — Finance Premium | 1,000 Copilot Credits included |
| **Sales** — Professional | Not included, sold separately |
| **Sales** — Enterprise | Not included, sold separately |
| **Sales** — Premium | 1,000 Copilot Credits included |
| **Supply Chain Management** — Supply Chain Management | Not included, sold separately |
| **Supply Chain Management** — Supply Chain Management Premium | 1,000 Copilot Credits included |

Source: [LG p.58]

## Model Context Protocol (MCP) for Dynamics 365

The **MCP (Model Context Protocol) server** provides a standardized, secure way for AI agents to access and act on enterprise data through natural language.[LG p.59] MCP is an open standard that connects AI agents to systems and standardizes how applications provide context to large language models; any agent platform that supports the protocol — including Microsoft Copilot Studio — can connect to Dynamics 365 business logic through the MCP server.[Learn: Build agents for finance and operations with MCP](https://learn.microsoft.com/dynamics365/release-plan/2025wave2/enterprise-resource-planning/finance-operations-crossapp-capabilities/build-agents-dynamics-365-finance-operations-model-context-protocol)

### MCP licensing and charges

- **Within Microsoft Copilot Studio.** When MCP tools are used within Microsoft Copilot Studio, **no additional charges for MCP tool execution** are incurred. Standard orchestration charges for such agents or tool calls continue to apply at published billing rates.[LG p.59]
- **Agents created outside Copilot Studio** require a valid license for authentication and access to the MCP server:[LG p.59]
  - Access to **Dynamics 365 data** is included with a **Dynamics 365 Premium license** (Sales Premium, Finance Premium, Supply Chain Premium, and Customer Service Premium).
  - Access to **non-Dynamics 365 data** is included with the **Microsoft 365 Copilot USL**.
  - Access with other applicable licenses is billed: MCP tools are billed at the same rate as AI tools (basic) per Copilot Credit consumption rates, and Dataverse grounding resource calls (e.g. Search and Fetch tool calls) are billed at the same rate as tenant graph grounding.
- **Other platforms.** Customers are responsible for configuration and for covering the orchestration costs associated with other platforms (e.g. Microsoft Foundry, Anthropic Claude).[LG p.59]

### MCP servers available across Dynamics 365

Microsoft provides MCP servers for several Dynamics 365 workloads. The finance and operations (ERP) MCP server exposes **data tools** (create/read/update/delete via data entities), **form tools** (page operations), and **action tools** (invoke application logic), all scoped by the authenticated user's security role.[Learn: Use Model Context Protocol for finance and operations apps](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/copilot/copilot-mcp) The **Dynamics 365 Sales MCP server** exposes Sales Qualification Agent, Sales Opportunity Agent, and Copilot in Dynamics 365 Sales tools plus Dataverse CRUD operations, and can be consumed by assistants such as Claude; each AI tool consumes Copilot Studio credits based on the agent feature it uses.[Learn: Dynamics 365 Sales MCP server overview](https://learn.microsoft.com/dynamics365/sales/connect-to-model-context-protocol-sales) A **Customer Service MCP server** is likewise available for configuration in Copilot Studio.[Learn: Connect to Dynamics 365 Customer Service MCP Server](https://learn.microsoft.com/dynamics365/customer-service/administer/configure-customer-service-mcp-server)

## Key takeaways

- Embedded **Copilot in Dynamics 365 <app>** experiences are included with the qualifying application license.[LG p.51][LG p.26]
- **Dynamics 365 agents always require Copilot Credits**, plus a valid license for the underlying app.[LG p.58]
- The four **Premium** SKUs each include **1,000 Copilot Credits per user/month**, accrued at tenant level.[LG p.58]
- **Premium Sales agent features** and full Work IQ require a separate **Microsoft 365 Copilot** license.[Learn: Buy Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales)
- **MCP tool execution inside Copilot Studio carries no extra tool charge**; access from outside Copilot Studio depends on Premium / Microsoft 365 Copilot licensing or is billed per Copilot Credit rates.[LG p.59]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.10
- Dynamics 365 Licensing Guide (July 2026), p.26
- Dynamics 365 Licensing Guide (July 2026), p.51
- Dynamics 365 Licensing Guide (July 2026), p.58
- Dynamics 365 Licensing Guide (July 2026), p.59
- Dynamics 365 Licensing Guide (July 2026), p.65
- [Microsoft Learn — Copilot in Dynamics 365 Sales overview](https://learn.microsoft.com/dynamics365/sales/copilot-overview)
- [Microsoft Learn — Buy Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales)
- [Microsoft Learn — Use Microsoft 365 Copilot in Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/microsoft-365-copilot-chat-in-sales)
- [Microsoft Learn — FAQ about Copilot in Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/sales-copilot-faq)
- [Microsoft Learn — Manage Copilot Studio credits and capacity](https://learn.microsoft.com/power-platform/admin/manage-copilot-studio-messages-capacity)
- [Microsoft Learn — Manage consumption-based billing and capacity](https://learn.microsoft.com/dynamics365/customer-service/administer/setup-pay-as-you-go)
- [Microsoft Learn — Copilot Studio licensing](https://learn.microsoft.com/microsoft-copilot-studio/billing-licensing)
- [Microsoft Learn — Build agents for finance and operations with Model Context Protocol](https://learn.microsoft.com/dynamics365/release-plan/2025wave2/enterprise-resource-planning/finance-operations-crossapp-capabilities/build-agents-dynamics-365-finance-operations-model-context-protocol)
- [Microsoft Learn — Use Model Context Protocol for finance and operations apps](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/copilot/copilot-mcp)
- [Microsoft Learn — Dynamics 365 Sales Model Context Protocol (MCP) server overview](https://learn.microsoft.com/dynamics365/sales/connect-to-model-context-protocol-sales)
- [Microsoft Learn — Connect to Dynamics 365 Customer Service MCP Server](https://learn.microsoft.com/dynamics365/customer-service/administer/configure-customer-service-mcp-server)

---
[⬅ Back to Index](./Index.md)
