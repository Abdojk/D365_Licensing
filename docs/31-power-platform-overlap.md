# Power Platform Use Rights Included with Dynamics 365

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Every Dynamics 365 application is built on **Microsoft Dataverse** and extended through the **Power Platform**. Because of this, qualifying Dynamics 365 licenses come with *seeded* (limited) Power Apps and Power Automate use rights so that users can customize and extend the Dynamics 365 experience without buying standalone Power Platform licenses. The catch is that those rights are **restricted to the context of the Dynamics 365 application** — step outside that context and a standalone license is required.

## What Appendix H covers

Appendix H of the Licensing Guide states that **select Dynamics 365 applications include limited Power Apps, Power Automate, Power Pages, and Microsoft Copilot Studio use rights**, and directs readers to the Power Platform Licensing Guide and the Microsoft Copilot Studio Licensing Guide for the full details.[LG p.85] The detail below draws the specifics from Microsoft Learn, which publishes the seeded-rights matrix.

## Dataverse: the shared platform

Dynamics 365 applications use **Dataverse** capacity and features to store and secure data.[LG p.68] Dataverse structures data and business logic to support interconnected applications, and entitlement to its features is included in many (but not all) Dynamics 365 licenses. Critically, **access to Dataverse through one product does not grant access to unrelated products, features, or data** for which the user is not licensed — users only have rights to the data, services, features, and app components within Dataverse for the Dynamics 365 product they are properly licensed for.[LG p.65]

Power Apps users who hold a Power Apps license may use custom applications to create, read, update, or delete any **non-restricted** Dynamics 365 table in Dataverse. However, users and devices that need to create, update, or delete data in Dynamics 365 **restricted tables** must be properly licensed for Dynamics 365.[LG p.68] (See the guide's *Restricted tables requiring Dynamics 365 licenses* reference.)

## Qualifying Dynamics 365 licenses

Microsoft Learn lists the Dynamics 365 Enterprise licenses that grant **premium** Power Apps and Power Automate usage rights:[Learn: Managed environment licensing](https://learn.microsoft.com/power-platform/admin/managed-environment-licensing)

- Dynamics 365 Sales Enterprise, Sales Premium
- Dynamics 365 Customer Service Enterprise, Customer Service Premium
- Dynamics 365 Field Service
- Dynamics 365 Finance, Finance Premium
- Dynamics 365 Supply Chain Management, Supply Chain Management Premium
- Dynamics 365 Project Operations
- Dynamics 365 Commerce
- Dynamics 365 Human Resources
- Dynamics 365 Business Central
- Dynamics 365 Team Members
- Dynamics 365 Intelligent Order Management

The Licensing Guide corroborates this at the app level: Business Central Team Members explicitly includes the right to *"use the Dynamics 365 Power Apps/Power Automate use rights provided with a Dynamics 365 license,"*[LG p.59] and Intelligent Order Management *"includes limited Power Automate use rights, such as Power Platform requests, and use of connectors."*[LG p.41]

## What the seeded Power Automate / Power Apps rights include

Dynamics 365 licenses include the following Power Automate capabilities:[Learn: Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs)

1. Create and execute **automated, scheduled, or button flows**
2. Access to **standard connectors**
3. Access to **premium connectors within app context**
4. **Business process flows** within app context
5. **Custom connectors** within app context
6. **On-premises gateways** within app context
7. **Action (daily request) limits**: Dynamics 365 Enterprise gets 40,000 actions/day, Dynamics 365 Professional gets 40,000 actions/day, and Dynamics 365 Team Member gets 6,000 actions/day

The following are **not** included with Dynamics 365 licenses and require additional purchase: **Robotic Process Automation (RPA)** and **AI Builder capacity**.[Learn: Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs)

Power Apps is the platform to customize and extend applications in Dynamics 365 (such as Sales and Customer Service) in the context of the use rights, and Power Automate is the platform to customize and extend automations — again in context of the use rights.[Learn: Licensing overview for Microsoft Power Platform](https://learn.microsoft.com/power-platform/admin/pricing-billing-skus)

## What "within the context of use rights" means

This is the single most important limitation. When you use a Dynamics 365 license with Power Automate, **your flows must run within the context of the Dynamics 365 application** — meaning they use the same data sources for triggers or actions as the Dynamics 365 application. If a flow consumes standalone Power Automate actions that aren't related to the Dynamics 365 applications, you need to purchase a standalone Power Automate license.[Learn: Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs)

Microsoft Learn illustrates the boundary:[Learn: Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs)

- **In context (included):** A flow connects Azure DevOps with Dynamics 365 CRM to escalate support cases and create work items — reading/writing to Azure DevOps while using a built-in Dataverse trigger or action.
- **Out of context (needs standalone license):** The same user builds a flow that updates an Oracle database, is unrelated to the Dynamics 365 app, and doesn't interact in any way with the app or its data sources.

The seeded model also uses the concept of the flow being *"in-context & associated to a Dynamics 365 app"* — premium connectors, custom connectors, business process flows, and on-premises gateways are only included when the cloud flow meets that association test.[Learn: Deep dive on specific licenses](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/deep-dive-on-specific-license)

## Power Platform requests and Power Pages

Power Apps and Power Automate usage counts against the **Power Platform request** entitlements provided by your license (formerly "API call requests"). Microsoft enforces limits on the number of requests users can make each day across their Dynamics 365 products; exceeding them can incur overage charges.[LG p.65] **Power Pages** capacity is enforced monthly, based on authenticated users per website per month and anonymous users per website per month.[LG p.65]

## External users

External users do **not** require Dynamics 365 user licenses to access Dynamics 365 applications, but custom applications that provide external users access to Dynamics 365 are **covered under Power Apps use rights for Dynamics 365**, as defined in the Power Platform Licensing Guide.[LG p.66] Note that limited external user access is included with internal user licenses, but the graphical interfaces for Business Central, Sales, Customer Service, Field Service, and Project Operations may **not** be accessed by external users — Power Pages is the licensed option for external access to business processes or data.[LG p.67]

## Dual use rights (on-premises)

**Dual use rights** allow you to deploy Dynamics applications either in Microsoft's cloud or in a private on-premises / partner-hosted cloud.[LG p.68] Key points:

- Properly licensed users **do not need additional client access licenses (CALs)** to access applications hosted on-premises; users with Dynamics 365 licenses have use rights equivalent to a CAL for accessing equivalent on-premises workloads, and device use rights are equivalent to cloud device use rights.[LG p.68]
- Any **server licenses** otherwise required for an on-premises deployment are included with the Dynamics 365 licenses; access to that on-premises server software is reserved for users assigned a qualifying Dynamics 365 license and external users.[LG p.68]
- Dual use rights are **non-perpetual** and expire when the cloud subscription expires.[LG p.69]
- Dynamics CALs have **no reciprocal rights** to functionality provided exclusively to Dynamics 365 licenses, and licenses for supporting servers (such as Windows Server and any CALs) must be obtained separately.[LG p.69]
- **Downgrade rights** are limited to Dynamics AX 2012 R3 (or later) for Operations on-premises, Dynamics CRM 2016 (or later) for Dynamics 365 On-Premises, and Business Central on-premises (current version, minus 2 versions).[LG p.69]

## Extensibility rules

Dynamics 365 **extensibility is provided through Power Platform**; the Power Platform functionality available to Dynamics users is detailed in the Power Platform Licensing Guide.[LG p.69] Additional extensibility rules:

- **Power BI:** Some Dynamics 365 applications embed Power BI content (tables and charts) in their UI. This is simply a product feature — no Power BI license is required to *view* it. Dynamics 365 users receive **no** standalone or general-purpose Power BI license; a **Power BI Pro or Power BI Premium per-user** license is required to **customize** the content.[LG p.69]
- **Custom tables and security roles:** For applicable products, Dynamics 365 licenses include the right to use **custom tables** (per Appendix D) and create **custom security roles** (per Appendix F).[LG p.70] Custom-table allowances vary by license — for example, Sales Professional, Customer Service Professional, and Operations – Activity may create and modify up to **15 custom tables per application**, while enterprise-level licenses have **no limit** on the number of custom tables.[LG p.79]
- **Dual write:** Synchronizing AOS application data (Commerce, Finance, Supply Chain Management, Project Operations) into Dataverse does **not** require a specific license, nor does configuring dual write against **unrestricted** tables. When dual write is configured against a **restricted** table, users making updates that result in updates to those restricted tables must be appropriately licensed.[LG p.69]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.41
- Dynamics 365 Licensing Guide (July 2026), p.59
- Dynamics 365 Licensing Guide (July 2026), p.65
- Dynamics 365 Licensing Guide (July 2026), p.66
- Dynamics 365 Licensing Guide (July 2026), p.67
- Dynamics 365 Licensing Guide (July 2026), p.68
- Dynamics 365 Licensing Guide (July 2026), p.69
- Dynamics 365 Licensing Guide (July 2026), p.70
- Dynamics 365 Licensing Guide (July 2026), p.79
- Dynamics 365 Licensing Guide (July 2026), p.85 (Appendix H)
- [Microsoft Learn — Licensing overview for Microsoft Power Platform](https://learn.microsoft.com/power-platform/admin/pricing-billing-skus)
- [Microsoft Learn — Managed environment licensing](https://learn.microsoft.com/power-platform/admin/managed-environment-licensing)
- [Microsoft Learn — Power Automate licensing FAQ](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs)
- [Microsoft Learn — Deep dive on specific licenses (seeded Power Automate)](https://learn.microsoft.com/power-platform/admin/power-automate-licensing/deep-dive-on-specific-license)

---
[⬅ Back to Index](./Index.md)
