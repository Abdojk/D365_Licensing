# Dynamics 365 Project Operations Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Project Operations connects sales, resourcing, project management, and finance teams within a single product to help organizations win more deals, accelerate project delivery, and maximize profitability. It is licensed **per user**, with a **minimum number of users required** (refer to the Microsoft Product Terms).[LG p.41]

## Project Operations full license

The Project Operations full user license is the primary license for the application. Account managers, project managers, project assistants, and project accountants are typically licensed as full Project Operations users.[LG p.41]

Project Operations licenses have **no roles at the Operations – Activity level**, but full Project Operations users have rights to Operations – Activity roles for **other** Dynamics 365 products such as Finance and Supply Chain Management.[LG p.41]

The full license covers the complete project lifecycle surface, including (per the security-role and use-rights tables): project sales and opportunity management, project contracts, quotes, price lists and multi-dimensional pricing, project estimates, resource management and scheduling, time/expense/material entry and approval, project invoicing (including recurring and corrective invoices), and project accounting/administration roles such as project billing administrator, project accountant, and project supervisor.[LG p.41-44] It also includes **Project for the Web** (Microsoft's cloud-based work and project management offering built on the Power Platform).[LG p.44]

## Team Members access for project use

Users who only need to **create and approve project timesheets** (for example a user with a Project Timesheet security role) need only a **Team Members** license rather than a full Project Operations license.[LG p.41]

The Project Operations use-rights and security-role tables show that a Team Members license supports:[LG p.41-44]

- Time and expense entry and submission for Project Operations.[LG p.44]
- Approval of time, expenses, materials, and invoices.[LG p.42]
- Project resource, project timesheet, project approver, and project timesheet delegate security roles.[LG p.41]
- Updating project task status, applying for open project positions, and updating own resource competencies/forecast.[LG p.43-44]
- Read access to all Dynamics 365 application data and custom table data.[LG p.42]

Team Members access is delivered through the **Project Operations Team Members app** (formerly the Project Resource Hub), which includes time entry, expense entry (Core deployment), material usage, approvals, and up to 15 custom entities of extensibility.[Learn: Project Operations Team Member app](https://learn.microsoft.com/dynamics365/project-operations/team-member/project-operations-team-member) Microsoft Learn confirms that using the Team Members app requires either a full Project Operations license or a Dynamics Team Members license, **and** an existing Project Operations deployment.[Learn: Project Operations Team Member app](https://learn.microsoft.com/dynamics365/project-operations/team-member/project-operations-team-member) The guide states the app requires a Project Operations Core (deal to proforma invoicing) or Project Operations Integrated with ERP deployment.[LG p.44]

## Deployment models

Microsoft Learn documents that Project Operations supports **multiple deployment types**, and organizations use a guided deployment questionnaire after purchase to choose the right one:[Learn: Determine your deployment type](https://learn.microsoft.com/dynamics365/project-operations/environment/determine-deployment-type)

1. **Project Operations Core** ("deal to proforma invoicing") — a **Dataverse-only** deployment covering the project sales process, project planning via Project for the Web, multi-dimensional pricing, unified resource management, time tracking, basic expense, material usage, budgeting/forecasting, subcontracting, and proforma invoicing.[Learn: Deploy Project Operations Core](https://learn.microsoft.com/dynamics365/project-operations/environment/lite-deployment)[Learn: Determine your deployment type](https://learn.microsoft.com/dynamics365/project-operations/environment/determine-deployment-type)
2. **Project Operations Integrated with ERP** — adds finance and operations (ERP) capabilities such as full expense with receipt OCR, customer-facing invoicing, and revenue recognition, using **dual-write** to synchronize between finance and operations apps and Dataverse.[Learn: Determine your deployment type](https://learn.microsoft.com/dynamics365/project-operations/environment/determine-deployment-type)
3. **Project Operations for manufacturing** — for stocked/production-order scenarios (project planning with WBS, resource management, time tracking).[Learn: Determine your deployment type](https://learn.microsoft.com/dynamics365/project-operations/environment/determine-deployment-type)

The licensing guide references both the **Core (deal to proforma invoicing)** and **Integrated with ERP** deployments as valid deployments that satisfy the Project Operations Team Members app requirement.[LG p.44] The choice of deployment does not change the per-user license itself; it determines which capabilities and environments are provisioned.

## Base and attach eligibility

Project Operations is a per-user license that provides **core business functionality**, so it qualifies as a **base license**. Microsoft Learn explicitly lists Project Operations among the products (with Finance, Supply Chain Management, Commerce, and Human Resources) whose licenses qualify as base licenses, each having additional applications that qualify as attach licenses for the same user.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion) Under the general base/attach rule, the first (highest-priced) license for a user is the base, and qualifying additional applications can be attached at a lower price with identical core capabilities.[LG p.6]

Project Operations is also a **qualifying app for a Customer Insights attach** license (10+ licenses of a qualifying app entitle attach pricing).[LG p.22] Only user licenses qualify for base-license treatment.[LG p.74]

## Included capacity and minimums

Project Operations carries a **20-seat minimum purchase requirement**; see the Microsoft Product Terms for service-specific terms.[LG p.45] The full license includes the following default entitlements:[LG p.45]

| Entitlement | Project Operations |
| --- | --- |
| Electronic Invoicing — electronic invoice transactions | 100 per tenant/month |
| Electronic Invoicing — invoice capture transactions | 100 per tenant/month |
| Dataverse or Operations Database | 90 GB (+5 GB accrued/USL) |
| Dataverse or Operations File | 80 GB (+5 GB accrued/USL) |
| Dataverse Log | 2 GB |
| Environments | 1 production (AOS) / 1 non-production (Sandbox Tier 2) |

Additional capacity and environments are available for purchase (see the Appendix / Capacity section).[LG p.45] Both the Dataverse capacities and the Operations Database/file storage capacities are pooled across the tenant; Operations Database and file storage are shared only among Finance, Supply Chain Management, Commerce, Human Resources, and Project Operations.[LG p.8]

## Field Service + Project Operations + Modern Project Operations integration

An out-of-the-box integration enables **Field Service** licensed users to transact against projects during their field operations, aligning field service with project operations and the finance and operations apps. When enabled, the Field Service application automatically syncs data with Project Operations and with Finance and Supply Chain Management. Covered use cases:[LG p.70]

- Creating or updating **projects** in Field Service so that work orders can be created against a project, allowing estimates, actuals, and materials usage lines to be recorded against the project.[LG p.70]
- Reading **inventory levels** in Field Service from Finance and Supply Chain Management (the system of record for inventory).[LG p.70]

This integration pattern uses the **Modern Project Operations** integration between Project Operations and the Finance and Operations apps to ensure Field Service transactions sync to those apps.[LG p.70]

> **Cross-app licensing note:** This integration does **not** license customers to use Project Operations functionality without a proper license, except through the data alignment Microsoft has built. **Direct access** to Project Operations, Finance, or Supply Chain Management still requires the respective licenses.[LG p.70]

The Field Service use-rights table reflects this limited project access: Field Service and Field Service Contractor users can create a Project Operations project to link to a work order, manage project estimate lines linked to work-order estimates, and record time/expense/material actuals and invoices on projects **linked to work orders** — but this access does **not** include the core Project Operations modules (project planning, budgeting, scheduling, pricing, costing, subcontracting, project-based management, etc.).[LG p.31-32]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6, p.8, p.41, p.42, p.43, p.44, p.45, p.70, p.74.
- [Learn: Determine your deployment type (Project Operations)](https://learn.microsoft.com/dynamics365/project-operations/environment/determine-deployment-type)
- [Learn: Deploy Project Operations Core](https://learn.microsoft.com/dynamics365/project-operations/environment/lite-deployment)
- [Learn: Project Operations Team Member app](https://learn.microsoft.com/dynamics365/project-operations/team-member/project-operations-team-member)
- [Learn: Expired subscriptions and data deletion (base vs. attach)](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

---
[⬅ Back to Index](./Index.md)
