# Specialized & Add-on Dynamics 365 Apps

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

This page covers specialized and add-on Dynamics 365 applications that sit outside the main Sales, Customer Service, Finance, and Supply Chain families. Each app is licensed on its own model — per tenant, per user, per device, or as a capacity add-on. Only apps that can be cited from the Licensing Guide or Microsoft Learn are included.

## Dynamics 365 Intelligent Order Management

Intelligent Order Management (IOM) is an intelligent, multi-tenant standalone service that lets customers adapt quickly and fulfill orders efficiently at the fastest speed and lowest cost, with event-driven orchestration and AI rules-based fulfillment, including anomaly detection and inventory reallocation.[LG p.41]

- **Licensing model:** licensed **per tenant**. The base license comes with **1,000 (1K) order lines per tenant per month**.[LG p.41]
- **Adding capacity:** if more capacity is needed, customers buy multiple units of the same license; the add-on provides an additional **1K order lines per tenant per month**.[LG p.41]
- **Included Power Platform rights:** the IOM license includes limited Power Automate use rights, such as Power Platform requests and use of connectors.[LG p.41]
- **Teams integration:** users licensed with a Modern Workplace license, whose organization has an IOM license, can enable Microsoft Teams integration to collaborate on IOM records.[LG p.41]

| Application / Capacity | Included capacity | Add-on capacity |
|---|---|---|
| IOM — Order Lines | 1K order lines/tenant/month | 1K order lines/tenant/month |

Source: IOM capacities table.[LG p.41]

Architecturally, IOM is built as a Microsoft Dataverse / Power Platform model-driven application with **no dependency on other Dynamics 365 apps**, working with both Dynamics 365 and non-Dynamics 365 systems through its provider framework and the Power Platform connector ecosystem.[Learn: Intelligent Order Management overview](https://learn.microsoft.com/dynamics365/intelligent-order-management/overview)

## Dynamics 365 Customer Voice

Customer Voice is a feedback management solution that lets an organization build enterprise-grade surveys and collect timely feedback across channels.[LG p.29]

- **Licensing model:** licensed **per tenant**, with capacity allowances based on the **number of responses** that distributed surveys receive.[LG p.29]
- **Included with enterprise products:** customers of Dynamics 365 enterprise products (Sales Enterprise, Customer Service Enterprise, Customer Insights, Field Service, Marketing, and Human Resources) are automatically entitled to Customer Voice and **2,000 responses per tenant per month**.[LG p.29] Microsoft Learn confirms the 2,000 responses/month are included at the tenant level regardless of the number of seats.[Learn: Purchase Dynamics 365 Customer Voice](https://learn.microsoft.com/dynamics365/customer-voice/purchase)
- **Standalone purchase:** anyone can purchase Customer Voice separately; the standalone license also includes **2,000 responses per tenant per month**.[LG p.29] Sales Professional and Customer Service Professional customers may also buy it.[LG p.29]
- **Additional responses:** any customer can buy additional response packs in packs of **1,000 responses per tenant per month**, with no purchase limit.[LG p.29]
- **Respondents are not licensed:** survey respondents do not need a license — only the survey **designer/editor** must be licensed for the tenant.[LG p.29] When purchasing standalone, a **free User Subscription License (USL)** is also assigned to each user who needs access.[Learn: Purchase Dynamics 365 Customer Voice](https://learn.microsoft.com/dynamics365/customer-voice/purchase)

**Response capacity notes from Learn:** capacity is measured at the tenant level and calculated annually; sending survey invitations does **not** consume capacity — only responses received (anonymous and non-anonymous) count. Unused responses **do not carry forward** to the next year.[Learn: Purchase Dynamics 365 Customer Voice — response capacity consumption](https://learn.microsoft.com/dynamics365/customer-voice/purchase#response-capacity-consumption)

| Application / Capacity | Included capacity | Add-on capacity |
|---|---|---|
| Customer Voice — Responses | 2K responses/tenant/month | 1K responses/tenant/month (no purchase limit) |

Source: Customer Voice capacity table.[LG p.29]

## Dynamics 365 Electronic Invoicing

Electronic Invoicing is the process of creating, presenting, and exchanging structured, transactional invoice documents between businesses and governments (for tax reporting) or trading partners, in an integrated electronic format.[LG p.29]

- **Included with core Operations apps:** Dynamics 365 Commerce, Finance, Project Operations, and Supply Chain Management each include **100 electronic invoice transactions per tenant per month** and **100 invoice capture transactions per tenant per month**.[LG p.29]
- **Premium apps:** Finance Premium and Supply Chain Management Premium include **200 electronic invoice transactions** and **200 invoice capture transactions per tenant per month**.[LG p.29]
- **Capping and no rollover:** the included capacity does not roll over and is **capped at 100 transactions/tenant/month** (or 200 if licensed with Finance Premium or SCM Premium), regardless of how many Dynamics 365 licensed applications the tenant has.[LG p.30]
- **Add-on capacity:** the Electronic Invoicing additional capacity license provides **1,000 (1K) electronic invoice transactions and 1K invoice capture transactions per tenant per month**. The transaction capacity resets each month, so customers should purchase for peak monthly capacity.[LG p.30]

## Dynamics 365 Guides and Remote Assist (mixed reality)

Dynamics 365 **Guides** is a mixed-reality application for Microsoft HoloLens that provides holographic step-by-step instructions in the flow of work, and Dynamics 365 **Remote Assist** lets technicians collaborate with a remote expert over Microsoft Teams on HoloLens 2.[Learn: Welcome to Dynamics 365 Guides](https://learn.microsoft.com/dynamics365/mixed-reality/guides/overview)

> **End of support — December 31, 2026.** Dynamics 365 Guides and Dynamics 365 Remote Assist will reach **end of support on December 31, 2026**. Subscriptions could be purchased or renewed only until **November 1, 2025**. After December 31, 2026, these products will no longer receive security updates, non-security updates, bug fixes, or technical support.[Learn: Dynamics 365 Guides and Remote Assist reaching end of support on December 31, 2026](https://learn.microsoft.com/lifecycle/announcements/dynamics-365-guides-remote-assist-end-of-support)

The Licensing Guide's revision history reflects the same wind-down, recording Guides and Remote Assist as **End of Sale** in November 2025.[LG p.88]

**Migration guidance from Microsoft:** identify users and scenarios that rely on Guides or Remote Assist and plan to move before December 31, 2026; explore alternative mixed-reality solutions on the Microsoft Marketplace; and note that certain Remote Assist scenarios can be supported using the **spatial annotation** feature in Microsoft Teams Mobile.[Learn: Guides and Remote Assist end of support](https://learn.microsoft.com/lifecycle/announcements/dynamics-365-guides-remote-assist-end-of-support)

**Device vs. user notes:** Both apps run on HoloLens 2 (Remote Assist experts can also join from Teams on desktop or mobile).[Learn: Welcome to Dynamics 365 Remote Assist](https://learn.microsoft.com/dynamics365/mixed-reality/remote-assist/ra-overview) Remote Assist **mobile** was deprecated on March 25, 2025; existing customers get similar capabilities through Microsoft Teams mobile, where a user can collaborate with an external user using spatial annotations provided one user has a Dynamics 365 Field Service, Guides, or Remote Assist license.[Learn: Welcome to Dynamics 365 Remote Assist](https://learn.microsoft.com/dynamics365/mixed-reality/remote-assist/ra-overview) Device, licensing, and other requirements for Guides are documented on Learn, which also carries the end-of-support notice.[Learn: Device, licensing, and other requirements for Dynamics 365 Guides](https://learn.microsoft.com/dynamics365/mixed-reality/guides/requirements)

## Dynamics 365 Fraud Protection

Dynamics 365 Fraud Protection helps merchants combat fraud across three areas: **purchase protection** (payment fraud), **account protection** (account sign-in and creation fraud), and **loss prevention** (anomalous behavior at point-of-sale terminals).[Learn: Service FAQ](https://learn.microsoft.com/dynamics365/fraud-protection/faq/service-faq)

> **No longer available for purchase; support ended.** As of **February 3, 2025**, Dynamics 365 Fraud Protection is **no longer available for purchase**, and support for the product **ended February 3, 2026**.[Learn: Overview of Dynamics 365 Fraud Protection / How purchase protection works](https://learn.microsoft.com/dynamics365/fraud-protection/how-pp-works)

Because Fraud Protection is no longer sold or supported, it is not part of the current licensable Dynamics 365 catalog. It is not covered in the July 2026 Licensing Guide. The capability descriptions above are retained for reference only; new deployments are no longer possible.[Learn: End of support for Dynamics 365 Fraud Protection](https://learn.microsoft.com/dynamics365/fraud-protection/eos)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.29
- Dynamics 365 Licensing Guide (July 2026), p.30
- Dynamics 365 Licensing Guide (July 2026), p.41
- Dynamics 365 Licensing Guide (July 2026), p.88
- [Intelligent Order Management overview](https://learn.microsoft.com/dynamics365/intelligent-order-management/overview)
- [Purchase Dynamics 365 Customer Voice](https://learn.microsoft.com/dynamics365/customer-voice/purchase)
- [Purchase Dynamics 365 Customer Voice — response capacity consumption](https://learn.microsoft.com/dynamics365/customer-voice/purchase#response-capacity-consumption)
- [Dynamics 365 Guides and Remote Assist reaching end of support on December 31, 2026](https://learn.microsoft.com/lifecycle/announcements/dynamics-365-guides-remote-assist-end-of-support)
- [Welcome to Dynamics 365 Guides](https://learn.microsoft.com/dynamics365/mixed-reality/guides/overview)
- [Device, licensing, and other requirements for Dynamics 365 Guides](https://learn.microsoft.com/dynamics365/mixed-reality/guides/requirements)
- [Welcome to Dynamics 365 Remote Assist](https://learn.microsoft.com/dynamics365/mixed-reality/remote-assist/ra-overview)
- [Overview of Dynamics 365 Fraud Protection / How purchase protection works](https://learn.microsoft.com/dynamics365/fraud-protection/how-pp-works)
- [End of support for Dynamics 365 Fraud Protection](https://learn.microsoft.com/dynamics365/fraud-protection/eos)
- [Dynamics 365 Fraud Protection Service FAQ](https://learn.microsoft.com/dynamics365/fraud-protection/faq/service-faq)

---
[⬅ Back to Index](./Index.md)
