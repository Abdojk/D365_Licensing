# Dynamics 365 Business Central Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Business Central connects teams across an organization with tools to help them work more efficiently, collaborate better, and respond more quickly to change. Business Central Essentials and Premium are **licensed per user** (named-user model).[LG p.8] This page covers the Essentials, Premium, Team Members, and Device licenses, the Business Central Agents, and the environment and capacity model.

## Named-user model and Microsoft 365 read access

Business Central Essentials and Premium are licensed per named user.[LG p.8] Licenses are purchased through the Cloud Solution Provider (CSP) program, and Business Central online generates permissions from **entitlements** tied to each user's Microsoft Entra service plan rather than from classic license files.[Learn: Licensing in Dynamics 365 Business Central](https://learn.microsoft.com/dynamics365/business-central/dev-itpro/deployment/licensing)

Internal users licensed with Microsoft 365 Business/Enterprise and select other plans, whose organization has one or more Business Central licenses, are granted **read-only** access to Business Central data from within Microsoft Teams at no additional cost.[LG p.8] This provides no new functionality to Microsoft 365 customers that do not have a Business Central plan.[Learn: Access with Microsoft 365 Licenses FAQ](https://learn.microsoft.com/dynamics365/business-central/admin-access-with-m365-license-faq)

## Business Central Essentials

Business Central Essentials provides a wide range of operational and management capabilities, including:[LG p.8]

- Financial Management
- AI-Supported Forecasting
- Customer Relationship Management
- Project Management
- E-Services
- Human Resources Management
- Supply Chain Management
- Warehouse Management and Inventory

The Essentials functional areas break down into detailed capabilities such as basic general ledger, bank reconciliation, fixed assets, and consolidation (Financial Management); cost accounting and intercompany postings (Advanced Financial Management); contact and campaign management and Dynamics 365 Sales integration (CRM); purchase and sales order management, requisition and demand forecasting (Supply Chain); and warehouse receipt/shipment and pick management (Warehouse Management).[LG p.9] Dynamics 365 Sales integration itself requires a separate Dynamics 365 Sales license, and some AI capabilities require an Intelligent Edge or Azure Machine Learning subscription.[LG p.9]

## Business Central Premium

Business Central Premium includes **all license capabilities of Essentials, plus Service Order Management and Manufacturing**.[LG p.10] Microsoft Learn confirms the same distinction: the Essentials experience shows all common business functionality, while the Premium experience additionally shows all actions and fields for **Manufacturing and Service Management**.[Learn: Change which features are displayed](https://learn.microsoft.com/dynamics365/business-central/ui-experiences)

The Premium-only functional areas are:[LG p.10]

- **Service Order Management** — Planning and Dispatching, Service Contract Management, Service Item Management, Service Order Management, Service Price Management.
- **Manufacturing** — Agile Manufacturing, Basic Capacity Planning, Basic Supply Planning, Finite Loading, Machine Centers, Production Bill of Materials, Production Orders, Sales and Inventory Forecasting, Version Management.

### Essentials vs. Premium at a glance

| Capability area | Essentials | Premium |
|---|---|---|
| Finance management | Yes | Yes |
| Sales and marketing | Yes | Yes |
| Fulfillment and delivery | Yes | Yes |
| Purchasing and payables | Yes | Yes |
| Inventory | Yes | Yes |
| Supply planning and availability | Yes | Yes |
| Project management | Yes | Yes |
| Warehouse management | Yes | Yes |
| Customization and extensibility | Yes | Yes |
| Multiple environments / multiple companies | Yes | Yes |
| **Manufacturing** | No | Yes |
| **Service management** | No | Yes |

Source: Business Central entitlements table.[LG p.11]

### How Premium and Essentials coexist in a tenant

Premium functionality is enabled at the **company** level through the **User Experience** setting on the Company Information page. A tenant can contain multiple environments, and each environment can contain multiple companies.[Learn: Manage Access to Environments](https://learn.microsoft.com/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access) An Essentials user can only open companies set to the Essentials experience; a Premium user can sign in to any company, but when working in an Essentials-configured company cannot use Premium-only features.[Learn: Change which features are displayed](https://learn.microsoft.com/dynamics365/business-central/ui-experiences) Customers may deploy Business Central Essentials and Premium in **separate environments on the same tenant**, but licensed users can only access the environment for which they are entitled.[LG p.11]

## Included rights for Essentials and Premium users

Both Essentials and Premium user licenses include:[LG p.10]

- **Unrestricted Business Central Team Members access.**
- The option to procure up to **3 External Accountant licenses** per customer tenant for third-party accountants to connect to Business Central, with the same use rights as an assigned Business Central license except access to user setup or administrative tasks.[LG p.10] External Accountant licenses are free but must be procured like other licenses.[Learn: Accountant experiences in Business Central](https://learn.microsoft.com/dynamics365/business-central/finance-accounting)
- **Multiple companies** (a limited number of companies per environment).
- Use of **Microsoft Copilot in Dynamics 365 Business Central**.
- For other AI-powered features, **1,800 seconds (30 minutes) per tenant** of access to Azure AI.

Business Central licenses also include configuration components, and customers exercising dual-use rights receive the full custom objects range numbered **50,000 – 99,999**.[LG p.10]

## Business Central Team Members

The **Business Central Team Members** license (distinct from the Dynamics 365 Team Members license) grants a named user the following rights, for their own use only:[LG p.59]

- Read data within Business Central.
- Update existing data and entries (for example, previously created customer, vendor, or item records; entries such as a due date on customer ledger entries).
- Approve or reject tasks in all workflows assigned to that user, limited to updating records that Team Members can access.
- Create, edit, and delete a sales or purchase quote.
- Create, edit, and delete personal information.
- Edit job time sheets for approval.
- Use the Power Apps / Power Automate use rights provided with a Dynamics 365 license.
- The Team Members application module may be customized with a maximum of **15 additional tables** (custom tables or standard Dataverse tables).[LG p.59]

Team Members are typically assigned to users who require limited write access rather than full Essentials or Premium functionality.[Learn: Access with Microsoft 365 Licenses FAQ](https://learn.microsoft.com/dynamics365/business-central/admin-access-with-m365-license-faq)

## Business Central Device

Business Central **Device** licenses are available and provide limited access to a subset of Business Central capabilities.[LG p.10] The device license type is one of the core Business Central license options alongside Essentials, Premium, and Team Members.[Learn: Get started as a reseller of Business Central online](https://learn.microsoft.com/dynamics365/business-central/dev-itpro/administration/get-started-online)

## Business Central Agents

Prebuilt Dynamics 365 Business Central **Agents** became generally available in November 2025.[LG p.88] To use any prebuilt Business Central Agent, a user must have a Business Central license, and agent usage consumes **Copilot Credits**, which are sold separately.[LG p.8][LG p.11] The available agents are:[LG p.8][LG p.11]

- **Sales Order Agent** — uses AI to analyze customer requests received via email, locate the customer in Business Central, engage in multi-turn email conversations to clarify requests, check item availability, and follow up with a sales quote.
- **Payables Agent** — captures, validates, and matches invoices against purchase orders and receipts, routes invoices to approvers with configurable rules, and provides dashboards and alerts for outstanding payables.

## Environments and capacity

Business Central Essentials and Premium user licenses include the following per-tenant capacity and environment allowances:[LG p.11]

| Item | Essentials | Premium |
|---|---|---|
| Business Central Database (included) | 80 GB | 80 GB |
| Business Central Database: Accrued per user (USL) | 3 GB | 5 GB |
| Environments included | 1 production / 3 non-production | 1 production / 3 non-production |

Additional database capacity and additional environments are available for purchase.[LG p.11] In Business Central online, customers do not pay for objects; instead the main add-on costs are for extra production environments and storage capacity, which do not apply to the on-premises model.[Learn: Get started as a reseller of Business Central online](https://learn.microsoft.com/dynamics365/business-central/dev-itpro/administration/get-started-online)

## Pricing

Business Central Essentials, Premium, and Device are billed annually and priced per the official pricing page. This guide does not reproduce prices, which change over time — see the official **[Business Central pricing page](https://www.microsoft.com/dynamics-365/products/business-central/)** for current amounts.[LG p.11]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.8
- Dynamics 365 Licensing Guide (July 2026), p.9
- Dynamics 365 Licensing Guide (July 2026), p.10
- Dynamics 365 Licensing Guide (July 2026), p.11
- Dynamics 365 Licensing Guide (July 2026), p.59
- Dynamics 365 Licensing Guide (July 2026), p.88
- [Licensing in Dynamics 365 Business Central](https://learn.microsoft.com/dynamics365/business-central/dev-itpro/deployment/licensing)
- [Change which features are displayed (Essentials vs. Premium experiences)](https://learn.microsoft.com/dynamics365/business-central/ui-experiences)
- [Manage Access to Environments](https://learn.microsoft.com/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)
- [Access with Microsoft 365 Licenses FAQ](https://learn.microsoft.com/dynamics365/business-central/admin-access-with-m365-license-faq)
- [Accountant experiences in Business Central](https://learn.microsoft.com/dynamics365/business-central/finance-accounting)
- [Get started as a reseller of Business Central online](https://learn.microsoft.com/dynamics365/business-central/dev-itpro/administration/get-started-online)
- [Business Central product/pricing page](https://www.microsoft.com/dynamics-365/products/business-central/)

---
[⬅ Back to Index](./Index.md)
