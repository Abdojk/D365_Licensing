# Dynamics 365 Customer Service Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Customer Service helps organizations manage customer relationships, empower service agents, and deliver branded self-service through a searchable knowledge base.[LG p.24] It is available in **Professional**, **Enterprise**, and **Premium** editions, with several optional add-ins. Customer Service Enterprise may also be **licensed by device**.[LG p.24]

> **Important environment rule:** Enterprise and Professional users may not be mixed on the same instance. If you keep Professional licenses, you must abide by the contractual requirement to separate them.[Learn: Move from CS Enterprise to CS Professional](https://learn.microsoft.com/dynamics365/customer-service/implement/move-cs-enterprise-cs-professional)

## The Customer Service SKUs at a glance

| SKU | Licensed by | What it is |
|---|---|---|
| **Customer Service Professional** | User | Basic resources for agents plus a self-service website and knowledge base, for less complex scenarios.[LG p.24] |
| **Customer Service Enterprise** | User or Device | Expands on Professional with scheduling/dispatch, teams, resource management, unified routing, embedded intelligence, Copilot, and integration with other Dynamics 365 apps.[LG p.24-25] |
| **Customer Service Premium** | User | Customer Service Enterprise **+** Contact Center (Digital + Voice), a Copilot-first contact center + CRM solution powered by generative AI.[LG p.25] |
| **Customer Service Device** | Device | Full-access license with the same rights as the Customer Service Enterprise user license, limited to the licensed device.[LG p.27] |

## Customer Service Professional

Customer Service Professional provides **basic resources** for customer service agents, plus a self-service customer website and access to a knowledge base for end customers. It is intended for **less complex scenarios** that need streamlined capabilities.[LG p.24] It includes case management, knowledge management, mobile, lead creation, Power BI, and Microsoft 365 interoperation, with limited (1) customization and extensibility.[LG p.28]

## Customer Service Enterprise

Customer Service Enterprise expands on Professional. In particular, the Enterprise license grants use rights to **schedule and dispatch service, create teams, and manage resources** through integration with other Dynamics 365 applications such as Field Service and Project Operations (when those are also licensed).[LG p.24] It adds capabilities not in Professional, including:[LG p.28]

- Unified service desk
- Embedded intelligence and context-driven suggestions
- Analytics and KPI reporting
- Multisession support
- Portals
- Copilot in Dynamics 365 Customer Service

**Unified Routing** provides intelligent, automated routing and assignment (multi-stage classification and assignment based on availability, capacity, or specialization). Routing records — excluding Chat and Digital Messaging conversation records — are subject to a licensed capacity, and Enterprise includes **50 record routes/user/month**.[LG p.25] **Customer Service Insights** (integrated analytics and AI, including topic clustering) is included with the Enterprise license.[LG p.25]

When you license Customer Service Enterprise, you automatically become entitled to **2,000 Customer Voice responses/user/month**.[LG p.24]

### Customer Service Enterprise capacity

| Capability | Included capacity | Add-on capacity |
|---|---|---|
| Record routing (excluding chats, calls, text messages) | 50 record routes/user/month | Unified Routing add-on: 10K record routes/tenant/month |

Source: [LG p.25]. Capacity is pooled at the tenant level.[LG p.25]

## Customer Service Premium

Customer Service Premium provides an **integrated Copilot-first contact center and CRM solution, powered by generative AI**. Licensed per user, it **includes Customer Service Enterprise and Contact Center (Digital + Voice)**, with additional capacity entitlements for both applications.[LG p.25] Microsoft Learn confirms Customer Service Premium as the SKU that supports the broadest contact center scenarios, infusing generative AI across the customer journey (voice + IVR, unified routing, Copilot agent assistance, and supervisor analytics).[Learn: Contact center using Customer Service Premium](https://learn.microsoft.com/dynamics365/guidance/reference-architectures/contact-center-dynamics-365-customer-service-premium)

> **Copilot / Contact Center capability — verified:** The guide's use-rights and entitlements tables confirm Customer Service Premium includes **Copilot in Dynamics 365 Customer Service** and **Dynamics 365 Contact Center (Digital + Voice)**, which Enterprise and Professional do not bundle.[LG p.26][LG p.28]

**Important capacity exception:** **Customer Voice is included with Customer Service Enterprise but is *not* included with Customer Service Premium.**[LG p.25][LG p.28] For the Contact Center capacity that Premium adds, see [Dynamics 365 Contact Center Licensing](./12-contact-center.md).

## Customer Service Device

Customer Service Device licenses are **full-access licenses** with the same rights as the equivalent Customer Service **Enterprise** user license, except access is limited to only the licensed device.[LG p.27] Customer Service Device supports **shared logins**; when users share a login their individual usage cannot be tracked.[LG p.7]

## Contact Center add-ons for Customer Service Enterprise

Customer Service **Enterprise** licensed users are eligible to purchase Contact Center add-on options for **Digital**, **Voice**, or **both (Digital + Voice)** in a single bundle.[LG p.27] (Customer Service **Premium** already includes Contact Center Digital + Voice, so it does not need these add-ons.[LG p.27])

- **Contact Center Digital Add-on** — licensed per user; customer engagement across digital messaging and chat channels. Includes unified routing with 50 record routes/user/month (excluding chats, calls, text messages). Copilot credits are purchased separately.[LG p.27]
- **Contact Center Voice Add-on** — licensed per user; native voice capabilities. Includes **2,000 Intelligent Voicebot (IVR) minutes/user/month**, **6,000 Call Intelligence minutes/user/month**, and **35 GB of Dataverse file storage**.[LG p.27]
- **Contact Center Add-on (Digital + Voice)** — a bundle that includes both Digital and Voice with all their capacity entitlements.[LG p.27]

Full details of the Contact Center offers and their capacities are in [Dynamics 365 Contact Center Licensing](./12-contact-center.md).

## Dynamics 365 Customer Service Agents

To use the prebuilt Dynamics 365 Customer Service Agents, a user must be licensed for Dynamics 365 Customer Service.[LG p.24] The agents are the **Case Management Agent**, **Customer Intent Agent**, **Knowledge Management Agent**, and **Quality Evaluation Agent**.[LG p.24] **1K Copilot Credits per user/month** are included with **Customer Service Premium**; for Professional and Enterprise, the agents require Copilot Credits purchased separately.[LG p.24][LG p.28]

## Base / Attach eligibility

Dynamics 365 uses a **Base and Attach** model for users needing more than one full-access application. Every full-access user must first have a **base license** (the highest-priced license for that user); additional qualifying applications can be added as lower-priced **attach licenses** for users who already hold a qualifying base license.[LG p.6] Base and attach licenses are identical in core capabilities and differ only in price; attach licenses do not add platform entitlements beyond the base.[LG p.6]

**Customer Service Enterprise** and **Customer Service Premium** are enterprise applications that can act as a base license or, for users with a qualifying base license, be added at attach pricing — see the guide's "Base applications and their qualifying products for attach licensing" table for exact combinations.[LG p.6] (As one documented exception, a user whose base license is Business Central Premium may add Customer Service Enterprise at the attach price.[LG p.6]) For the general model, see [The Dynamics 365 Licensing Model](./01-licensing-model.md).

## Seeded Power Platform rights and capacity

- **Power Apps / Power Automate:** Customer Service Enterprise and Premium are enterprise Dynamics 365 licenses that grant premium Power Apps and Power Automate usage rights within the app context.[Learn: Managed environment licensing](https://learn.microsoft.com/power-platform/admin/managed-environment-licensing) Dynamics 365 Professional and Enterprise licenses are allotted 40,000 Power Automate actions/day; flows must run within the Dynamics 365 application context.[Learn: Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs#dynamics-365-license-questions)
- **Customer Voice:** included with Customer Service Enterprise (2,000 responses per tenant/month per the entitlements table); **not** included with Customer Service Premium.[LG p.28]
- **Unified Routing:** Enterprise and Premium include 50 records per user/month (excluding chats, calls, and text messages); Professional includes none.[LG p.28]

### Included Dataverse capacity (default, per subscription)

| Capacity | Customer Service Professional | Customer Service Enterprise | Customer Service Premium |
|---|---|---|---|
| **Dataverse Database** | 30 GB | 30 GB | 30 GB |
| Accrued per USL | — | 250 MB | 250 MB |
| **Dataverse File** | 40 GB | 40 GB | 40 GB |
| Accrued per USL | — | 2 GB | 35 GB |
| **Dataverse Log** | 2 GB | 2 GB | 2 GB |

Source: [LG p.28]. Additional capacity is available for purchase.[LG p.28]

## Pricing

This knowledge base does not quote dollar figures because prices change. For current per-user pricing of each Customer Service SKU, see the official **[Dynamics 365 Customer Service pricing page](https://www.microsoft.com/dynamics-365/products/customer-service/pricing)**.[Learn: Can't install Customer Service apps](https://learn.microsoft.com/troubleshoot/dynamics-365/customer-service/customer-service-admin-center/cant-install-dynamics-365-customer-service-apps-in-existing-environment)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.7
- Dynamics 365 Licensing Guide (July 2026), p.24
- Dynamics 365 Licensing Guide (July 2026), p.25
- Dynamics 365 Licensing Guide (July 2026), p.26
- Dynamics 365 Licensing Guide (July 2026), p.27
- Dynamics 365 Licensing Guide (July 2026), p.28
- [Microsoft Learn — Move from Customer Service Enterprise to Professional](https://learn.microsoft.com/dynamics365/customer-service/implement/move-cs-enterprise-cs-professional)
- [Microsoft Learn — Contact center using Dynamics 365 Customer Service Premium](https://learn.microsoft.com/dynamics365/guidance/reference-architectures/contact-center-dynamics-365-customer-service-premium)
- [Microsoft Learn — Can't install Dynamics 365 Customer Service applications (licensing)](https://learn.microsoft.com/troubleshoot/dynamics-365/customer-service/customer-service-admin-center/cant-install-dynamics-365-customer-service-apps-in-existing-environment)
- [Microsoft Learn — Managed environment licensing](https://learn.microsoft.com/power-platform/admin/managed-environment-licensing)
- [Microsoft Learn — Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs#dynamics-365-license-questions)
- [Dynamics 365 Customer Service pricing page](https://www.microsoft.com/dynamics-365/products/customer-service/pricing)

---
[⬅ Back to Index](./Index.md)
