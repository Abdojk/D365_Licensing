# Dynamics 365 Sales Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Sales lets sellers manage accounts and contacts, nurture deals from lead to order, and close faster with insights and AI.[Learn: Welcome to Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/overview) It is offered at several functionality levels so an organization can choose the tier that fits its sales process: **Sales Professional**, **Sales Enterprise**, **Sales Premium**, and **Microsoft Relationship Sales**.[LG p.46] Each Sales application option is licensed **per user**; Sales Enterprise may also be licensed **per device**.[LG p.46]

> **Important environment rule:** Customers using Sales Professional cannot combine Sales Premium, Enterprise, or Sales Insights within the same environment instance.[LG p.46] More broadly, Enterprise and Professional users may not be deployed in the same environment, though Professional and Enterprise may be deployed in separate environments on the same tenant (licensed users can only access the environment for which they are entitled).[LG p.51]

## The Sales SKUs at a glance

| SKU | Licensed by | What it is |
|---|---|---|
| **Sales Professional** | User | Essential sales force automation (SFA) for organizations without complex sales processes.[LG p.46] |
| **Sales Enterprise** | User or Device | SFA plus customization, extensibility, embedded intelligence, manual forecasting, Copilot in Dynamics 365 Sales, and selected Sales Premium features at limited capacity.[LG p.46-47] |
| **Sales Premium** | User | All Sales Enterprise capabilities plus the full Sales Insights automation and AI offerings.[LG p.47] |
| **Microsoft Relationship Sales (MRS)** | User | Sales Enterprise + LinkedIn Sales Navigator Advanced Plus. Not sold directly.[LG p.48] |
| **Sales Device** | Device | Full-access license with the same rights as the Sales Enterprise user license, limited to the licensed device.[LG p.48] |

## Sales Professional

A Sales Professional license provides essential **sales force automation (SFA)** for organizations that do not have complex sales processes.[LG p.46] It includes SFA, the mobile app, Microsoft 365 interoperation, and reporting and dashboards.[LG p.51] Sales Professional users are entitled only to the **Sales Professional application** — they are **not** entitled to the Sales Hub application, and they are **not** entitled to Sales Insights features.[LG p.47]

## Sales Enterprise

Sales Enterprise takes an organization beyond basic SFA to meet the needs of more complex sales processes. In addition to everything in Sales Professional, it adds **customization, extensibility, embedded intelligence, and manual forecasting**, and it includes **Copilot in Dynamics 365 Sales**.[LG p.46] Copilot capabilities include natural language insights, record updates, email and meeting assistance, and opportunity summaries.[LG p.51]

Sales Enterprise also includes **selected Sales Premium features** — assistant cards, email engagement, auto-capture of Outlook activity, plus Conversation Intelligence, Sales Accelerator, and Lead & Opportunity scoring — but with **limited capacity**:[LG p.47]

- **Conversation Intelligence** — activated users receive **unlimited hours/user/month**.[LG p.47-48]
- **Sales Accelerator** — up to **1,500 records connected to a sequence per environment per month**.[LG p.47-48]
- **Lead & Opportunity (Predictive) Scoring** — up to **1,500 records scored per environment per month**.[LG p.47-48]
- **Business Card Reader** — **10 scans/user/month**, pooled at the tenant level.[LG p.48-49]

To access all Sales Premium features or higher capacity, a Sales Enterprise user steps up to Sales Premium (or adds the Sales Insights capacity add-on).[LG p.47] Sales Enterprise users set these features up through the **Sales Hub** application.[LG p.47]

## Sales Premium

Sales Premium takes the Sales Enterprise capabilities and accelerates engagement and decision-making with prebuilt, embedded business insights. Licensed per user, it includes **all Sales Enterprise feature permissions plus the full Sales Insights automation and AI offerings**.[LG p.47] Microsoft Learn frames Sales Premium as Sales Enterprise **plus AI** — guided selling, relationship intelligence (sales assistant, who knows whom, conversation intelligence), and predictive models (predictive lead/opportunity scoring and predictive forecasting).[Learn: Welcome to Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/overview)

Sales Premium also uniquely includes **AI-Powered Data Enrichment** and **advanced sales engagement**, which are not part of Sales Enterprise.[LG p.51]

## Sales Insights (part of Sales Premium; add-on to Sales Enterprise / MRS)

Sales Insights is included in Sales Premium and can also be **added onto a Sales Enterprise or MRS license**. Sales Professional users are **not** entitled to these features.[LG p.47] A full Sales Insights license enables:[LG p.47]

- Predictive Scoring (lead and opportunity)
- Predictive Forecasting
- Business Card Reader
- Relationship Analytics
- Assistant Studio
- Sales Accelerator
- Pipeline Intelligence
- Notes Analysis
- Conversation Intelligence
- Connection Insights (who knows whom)

### Sales Insights capacity

| Capability | Included with **Sales Enterprise** | With **Sales Insights / Sales Premium** users |
|---|---|---|
| Business Card Reader | 10 scans/user/month | 200/user/month (pooled at tenant level) |
| Conversation Intelligence | Activated users: unlimited hours/user/month | Unlimited hours/user/month |
| Sales Accelerator | 1,500 records connected to a sequence per environment/month | Full access |
| Lead & Opportunity Scoring | 1,500 records scored per environment/month | Full access |

Source: [LG p.48]. Unused capacity rolls over for up to 12 months.[LG p.48] Business Card Reader has full access under Sales Insights **except** it is capped at 200/user/month; additional Sales Insights capacity licenses increase this pooled amount.[LG p.47] When Sales Insights is licensed within Sales Premium, additional capacity is bought by purchasing additional Sales Premium licenses.[LG p.47]

## Microsoft Relationship Sales (MRS)

Microsoft Relationship Sales helps sellers build relationships using the power of relationship selling. **MRS includes Sales Enterprise and LinkedIn Sales Navigator Advanced Plus**, and is licensed per user.[LG p.48] All components, software, and entitlements of MRS are limited for use with Dynamics 365 Sales environments only.[LG p.48]

- **Not sold directly:** MRS is **not available for direct purchase** — to buy it, contact a Microsoft representative or a partner.[Learn: Buy Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales)
- **Minimum purchase:** a **10-seat minimum** applies; see the Microsoft Product Terms for service-specific terms, and contact a Dynamics 365 sales specialist for pricing.[LG p.51]

## Sales Device

Sales Device licenses are **full-access licenses** that include the same rights as the equivalent Sales **Enterprise** user license, except that access is limited to only the licensed device.[LG p.48] Sales Device licenses support **shared logins** (any number of users can access Sales through the licensed shared device); note that when users share a login their individual usage cannot be tracked.[LG p.7]

## Dynamics 365 Sales Agents

To use the prebuilt Dynamics 365 Sales Agents, a user must hold a Dynamics 365 Sales license (Sales Professional, Enterprise, or Premium).[LG p.46] The agents are the **Sales Qualification Agent**, **Sales Opportunity Agent**, and **Sales Research Agent**.[LG p.46][LG p.51] **1K Copilot Credits per user/month** are included with **Sales Premium**; for Sales Professional and Sales Enterprise, the Sales Agents require Copilot Credits purchased separately.[LG p.46][LG p.51]

## Base / Attach eligibility

Dynamics 365 uses a **Base and Attach** model for users who need more than one full-access application. Every full-access user must have a **base license** — when purchasing multiple applications for one user, the first license must be the highest-priced (base) license. Additional qualifying applications can then be added as lower-priced **attach licenses**, which may only be assigned to a user who already holds an appropriate qualifying base license.[LG p.6] Base and attach licenses are identical in core capabilities and differ only in price; attach licenses do not add platform entitlements beyond those of the base license.[LG p.6]

In practice, **Sales Enterprise** and **Sales Premium** are enterprise applications that can serve as a base license or, for users who already hold a qualifying base license, be added at attach pricing — refer to the guide's "Base applications and their qualifying products for attach licensing" table for the exact qualifying combinations.[LG p.6] (As one documented exception, a user whose base license is Business Central Premium is eligible to add Sales Enterprise at the attach price.[LG p.6]) For the general model, see [The Dynamics 365 Licensing Model](./01-licensing-model.md).

## Seeded Power Platform rights and capacity

Dynamics 365 Sales runs on **Microsoft Dataverse** and uses Power Apps model-driven app design.[Learn: Welcome to Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/overview) Sales licenses include seeded Power Platform use rights:

- **Power Apps / Power Automate:** Enterprise Dynamics 365 licenses (including Sales Enterprise and Sales Premium) grant premium Power Apps and Power Automate usage rights within the app context.[Learn: Managed environment licensing](https://learn.microsoft.com/power-platform/admin/managed-environment-licensing) Power Automate flows must run within the context of the Dynamics 365 application; standalone use requires separate licenses.[Learn: Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs#dynamics-365-license-questions) Dynamics 365 Professional and Enterprise licenses are allotted 40,000 Power Automate actions/day.[Learn: Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs#dynamics-365-license-questions)
- **Customer Voice:** Sales Enterprise, Sales Premium, and MRS include **2,000 Customer Voice responses per tenant per month**.[LG p.46][LG p.51]
- **Unified Routing:** Sales Enterprise, Sales Premium, and MRS include **50 records per user/month** (excluding Chat and Digital Messaging conversation records); Sales Professional includes none.[LG p.51]

### Included Dataverse capacity (default, per subscription)

| Capacity | Sales Professional | Sales Enterprise | Sales Premium | Microsoft Relationship Sales |
|---|---|---|---|---|
| **Dataverse Database** | 30 GB | 30 GB | 45 GB | 10 GB |
| Accrued per USL | — | 250 MB | 500 MB | 250 MB |
| **Dataverse File** | 40 GB | 40 GB | 60 GB | 20 GB |
| Accrued per USL | — | 2 GB | 2 GB | 2 GB |
| **Dataverse Log** | 2 GB | 2 GB | 2 GB | 2 GB |

Source: [LG p.51]. The first base license for a product includes its default capacity (shared per tenant); default capacity is not cumulative and attach licenses do not add capacity beyond the base.[LG p.6] Additional capacity is available for purchase.[LG p.51]

## Pricing

This knowledge base does not quote dollar figures because prices change. For current per-user pricing of each Sales SKU, see the official **[Dynamics 365 Sales pricing page](https://www.microsoft.com/dynamics-365/products/sales/pricing)**.[Learn: Buy Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales) Sales Professional, Enterprise, and Premium can be bought directly, through Microsoft 365, or through a partner; MRS must be bought through a Microsoft representative or partner.[Learn: Buy Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.7
- Dynamics 365 Licensing Guide (July 2026), p.46
- Dynamics 365 Licensing Guide (July 2026), p.47
- Dynamics 365 Licensing Guide (July 2026), p.48
- Dynamics 365 Licensing Guide (July 2026), p.49
- Dynamics 365 Licensing Guide (July 2026), p.51
- [Microsoft Learn — Welcome to Dynamics 365 Sales (overview)](https://learn.microsoft.com/dynamics365/sales/overview)
- [Microsoft Learn — Buy Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales)
- [Microsoft Learn — Upgrade your Dynamics 365 Sales license](https://learn.microsoft.com/dynamics365/sales/upgrade-sales-license)
- [Microsoft Learn — Managed environment licensing](https://learn.microsoft.com/power-platform/admin/managed-environment-licensing)
- [Microsoft Learn — Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs#dynamics-365-license-questions)
- [Dynamics 365 Sales pricing page](https://www.microsoft.com/dynamics-365/products/sales/pricing)

---
[⬅ Back to Index](./Index.md)
