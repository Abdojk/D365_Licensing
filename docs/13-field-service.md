# Dynamics 365 Field Service Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Field Service connects and empowers field-based service teams. It leverages tight integration between Customer Service case management and field service work orders to deliver business-process-driven management of field service operations. Field Service is licensed **per user and/or per device**.[LG p.30]

## Field Service license types

There are four licensing components in the Field Service family:

- **Dynamics 365 Field Service** — the full user license.[LG p.30]
- **Dynamics 365 Field Service Contractor** — a lower-cost per-user license for non-employees.[LG p.30]
- **Dynamics 365 Field Service Device** — a full-access device license.[LG p.32]
- **Dynamics 365 Field Service Resource Scheduling Optimization** — an add-on licensed per resource.[LG p.32]

Microsoft Learn confirms two user license types are available to purchase — the standard Field Service license (all core features) and the Field Service Contractor license (a subset of features for third-party technicians).[Learn: Buy Dynamics 365 Field Service licenses](https://learn.microsoft.com/dynamics365/field-service/buy-fs)

## Dynamics 365 Field Service (full user)

The Field Service user license is the full-access license for the application. It includes:

- Access from the web, on mobile, and through Microsoft 365.[LG p.33]
- Access to the latest version of **Field Service Mobile** (a Microsoft product designed specifically for Field Service and distinct from the Dynamics 365 Mobile Client).[LG p.30]
- Vendor and contractor management, scheduling and resource dispatching, AI assistance from Copilot in Field Service (work-order creation and updates, scheduling, summarization), technician performance analysis, planned maintenance agreements, and returns processing.[LG p.33]
- An automatic entitlement to **2,000 Customer Voice responses per tenant per month** when you license Field Service.[LG p.30][LG p.33]

A **Bing Maps Developer license** is included with limitations (billable transactions) as described at Microsoft's maps licensing page; the Bing Maps Notices apply.[LG p.30]

Every user who needs to access Field Service needs a user account, a Field Service license, and appropriate security roles — the license grants legal access, and security roles grant in-product permissions.[Learn: Set up users, licenses, and security roles](https://learn.microsoft.com/dynamics365/field-service/users-licenses-permissions)

## Dynamics 365 Field Service Contractor

Field Service Contractor extends field operations to **non-employees** by providing essential work order management functionality, making it easier to scale service operations to meet demand. It is licensed per user and includes the latest version of Field Service Mobile.[LG p.30]

**Prerequisite:** Organizations must already have a Field Service license before they are eligible to purchase and use Field Service Contractor licenses.[LG p.30]

The Contractor license is a reduced-capability license. Compared with the full Field Service license, it does **not** include (among other things): Copilot AI assistance, technician performance analysis, planned maintenance agreements, returns processing, dispatch/scheduling administration, and the included Customer Voice or Dataverse capacity entitlements.[LG p.33] Contractors are limited to their own resources and manual scheduling only, and can create quotes and leads only (not manage the full sales/dispatch surface).[LG p.31]

> **Note:** The Field Service Contractor SL does **not** include any Dataverse capacity entitlements.[LG p.33]

Contractors are commonly onboarded as Microsoft Entra B2B collaboration (guest) users so they can sign in to the Field Service mobile app.[Learn: Set up users, licenses, and security roles](https://learn.microsoft.com/dynamics365/field-service/users-licenses-permissions)

## Dynamics 365 Field Service Device

Field Service Device licenses are **full-access** licenses. They include the same rights as the equivalent Enterprise user license, except that access is limited to only the licensed device.[LG p.32] Field Service Device supports **shared logins** (for example a shared warehouse device and password); note that when individual users share a login, their individual usage cannot be tracked.[LG p.7] With a device license, any number of users can access the application through the licensed dedicated shared device.[LG p.7]

## Resource Scheduling Optimization (add-on)

Resource Scheduling Optimization (RSO) is an **add-in capability** for Field Service that automatically builds a schedule for the appropriate resource — a person or a non-human asset — while simultaneously optimizing appointments for travel time, mileage, and other constraints.[LG p.32]

- RSO is **licensed per resource**.[LG p.32]
- It is typically used by a scheduler or dispatcher who holds a Field Service user license and who designates any number of resources to be included.[LG p.32]
- The add-in license allows **unlimited use** of schedule optimization, whether on a regular cadence (daily, weekly) or ad-hoc.[LG p.32]

RSO appears in Appendix A as a distinct license, **Dynamics 365 Resource Scheduling Optimization**.[LG p.71]

## Base and attach eligibility

Field Service is a per-user full license, so it participates in Dynamics 365 **base and attach** licensing. Every full-access user must hold a base license (the highest-priced license for that user); attach licenses may be added to a user who already holds a qualifying base license, at a lower price, with identical core capabilities.[LG p.6] As a specific example, a user whose base license is **Business Central Premium** is eligible to add Field Service (as well as Customer Service Enterprise or Sales Enterprise) at the attach price.[LG p.6]

Field Service is also a **qualifying base** for a Customer Insights attach license: organizations with 10+ licenses of Field Service (among other qualifying apps) can buy Customer Insights at attach pricing.[LG p.22]

## Included capacity

The following default capacity is included with the Field Service (full) license. The Contractor license includes **none** of the Dataverse capacity entitlements.[LG p.33]

| Entitlement | Field Service | Field Service Contractor |
| --- | --- | --- |
| Customer Voice | 2K responses per tenant/month | — |
| Dataverse Database | 30 GB (+250 MB accrued/USL) | — |
| Dataverse File | 40 GB (+2 GB accrued/USL) | — |
| Dataverse Log | 2 GB | — |

Source: Field Service Entitlements table.[LG p.33] Additional capacity is available for purchase (see the Appendix / Capacity section of the guide).[LG p.33] Dataverse capacities are pooled and shared across a single tenant among Sales, Customer Service, Field Service, Finance, Supply Chain Management, Commerce, Human Resources, Project Operations, and Business Central.[LG p.7-8]

## Integration with Finance and Supply Chain Management (cross-app)

Field Service has an out-of-the-box integration with **Dynamics 365 Finance** and **Dynamics 365 Supply Chain Management**. When active, transactions performed by Field Service technicians (licensed with Field Service) automatically sync data with Finance and Supply Chain Management. Covered use cases:[LG p.70]

- Creating or updating work orders in Field Service creates and updates **projects and project journals** in Finance and Supply Chain Management.[LG p.70]
- Reading **inventory levels** in Field Service via virtual tables that expose inventory from Finance and Supply Chain Management (the system of record for inventory).[LG p.70]

> **Cross-app licensing note:** This integration is available for organizations licensed with Field Service, Finance, **and** Supply Chain Management. **Direct access** to the Finance or Supply Chain Management application still requires a separate license for those apps.[LG p.70]

Field Service also participates in the **Field Service + Project Operations + Modern Project Operations** integration, which lets Field Service users transact against projects in the course of their field operations. Direct access to Project Operations, Finance, or Supply Chain Management still requires the appropriate licenses. See the Project Operations page for details.[LG p.70]

## Related Team Members access

The Field Service use-rights table shows that a **Team Members** license grants limited, self-serve work-order rights (create/update/delete work orders for employee self-serve purposes only) plus read access, but not the full technician or dispatcher rights of a Field Service license.[LG p.30-32] Team Members also includes the Project Operations Team Members app, subject to a Project Operations deployment being present.[LG p.32]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6, p.7, p.8, p.22, p.30, p.31, p.32, p.33, p.70, p.71.
- [Learn: Buy Dynamics 365 Field Service licenses](https://learn.microsoft.com/dynamics365/field-service/buy-fs)
- [Learn: Set up users, licenses, and security roles (Field Service)](https://learn.microsoft.com/dynamics365/field-service/users-licenses-permissions)

---
[⬅ Back to Index](./Index.md)
