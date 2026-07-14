# Dynamics 365 License Types

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 licenses fall into three families based on what they are assigned to — **User**, **Device**, or **Tenant** — and within each family there are full-access and additional (limited) options.[LG p.5] This page walks through the full taxonomy and then details the Operations family of licenses.

## Summary of license types

| Family | Category | License type | What it is for |
|---|---|---|---|
| **User** | Full-access | Base license | The first, highest-priced full-access license for a named user; every full-access user must have one.[LG p.6] |
| **User** | Full-access | Attach license | A lower-priced full-access license for a qualifying additional application, assignable only to a user who already has a qualifying base license.[LG p.6] |
| **User** | Additional | Team Members | Read-only access to Dynamics 365 data plus basic capabilities for designated light-task scenarios.[LG p.7] |
| **User** | Additional | Operations – Activity | For users needing more than Team Members but not full-access rights across the Operations apps.[LG p.7][LG p.60] |
| **User** | Additional | App-specific limited licenses | Limited licenses tied to a specific product (e.g., Business Central Team Members, Human Resources Self Service).[LG p.6] |
| **Device** | Full-access | Full-access device | A dedicated shared device with full functionality; any number of users can access the app through it.[LG p.7] |
| **Device** | Additional | Operations – Device | Limited device access to a subset of Finance, Supply Chain, Commerce, and Project Operations capabilities.[LG p.7][LG p.61] |
| **Tenant** | Full-access | Full-access tenant | Primary licensing mechanism for products licensed only per tenant (e.g., Electronic Invoicing, Customer Insights).[LG p.7] |
| **Tenant** | Capacity | Capacity (add-on) licenses | Add-on capacity for components subject to limits, such as Dataverse storage.[LG p.7] |
| **Tenant** | Transactional | Operations – Order Lines | Per-tenant transactional licensing for qualifying order-line updates as an alternative to user/device licensing.[LG p.61] |

## User licenses

User licenses grant a **named user** full or limited access to specific products.[LG p.5] Full-access user licenses are the most common, but there are also several **additional user** options, usually with limited functionality.[LG p.5]

> **Note:** Enterprise and Professional users may not be deployed in the same environment.[LG p.5]

### Full-access user licenses (Base and Attach)

Full-access users are those who need the full, feature-rich functionality of one or more Dynamics 365 applications. The options are **Base** and **Attach** licenses:[LG p.5]

- **Base license** — When purchasing multiple applications for a single user, the first application license must be the highest-priced license (the base license). Every full-access user must have a base license.[LG p.6]
- **Attach license** — Lower-priced licensing for users who need additional applications. Attach licenses may only be assigned to users with an appropriate qualifying base license, and a named user may hold more than one attach license.[LG p.6]

Base and attach licenses are identical in core capabilities and differ only in price. Attach licenses do not include additional platform entitlements — they access the platform entitlements included with the assigned base license (the exception being Customer Insights attach licenses, which include the same default capacity entitlements as the Customer Insights base license).[LG p.6] Microsoft Learn describes this same base-vs-attach model as the cost-effective way for a single user to obtain full licensing across multiple Dynamics 365 products.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### Additional user licenses

Additional users often represent a large share of an organization's total users. They may consume data or reports, complete light tasks (such as time or expense entry and HR record updates), or use the system more heavily without needing full-access capabilities.[LG p.6] Options include:

- **Team Members license** — A user license for those who support multiple lines of business and aren't tied to a specific business unit. It grants read-only access to all Dynamics 365 data plus basic capabilities for designated scenarios such as expense entry or updating contacts (see the guide's Appendix D).[LG p.7] Team Members use rights and the 15-additional-tables customization allowance are detailed on guide page 60.[LG p.60]
- **Operations – Activity license** — A named-user license for users who need more Dynamics 365 capabilities than Team Members but still don't require full-access user rights.[LG p.7] (Detailed below.)
- **App-specific limited licenses** — Additional licenses scoped to a particular product, including:
  - **Business Central Team Members** — Read-only access to certain data and limited functionality within Business Central deployments.[LG p.6]
  - **Human Resources Self Service** — Access to employee and manager self-serve capabilities such as absence/vacation entry or benefits look-up.[LG p.6]

## Device licenses

Device licenses grant a **dedicated shared device** full or limited access to specific products.[LG p.7] Full-access device licenses are the most common, but there are also additional device options with limited functionality.[LG p.7]

### Full-access device licenses

For dedicated shared devices that require the full functionality of one or more Dynamics 365 applications. With a device license, any number of users can access the application through the licensed shared device.[LG p.7] Depending on the application and license, these may use:

- **Shared logins** (e.g., "Warehouse Computer" with a shared password) — enabled for Sales Device, Customer Service Device, Field Service Device, Operations – Device, and Business Central Device licenses. When users share a login, their individual usage cannot be tracked.[LG p.7]
- **Individual logins** (each user's personal credentials) — enabled for Business Central Device and Operations – Device licenses, with no separate user license required.[LG p.7]

### Additional device licenses

For shared devices used only to consume data/reports or complete light tasks without full-access capabilities.[LG p.7] The primary example is the **Operations – Device** license, which provides limited access to a subset of Finance, Supply Chain Management, Commerce, and Project Operations capabilities.[LG p.7]

## Tenant licenses

Tenant licenses provide tenant-level access to Dynamics 365 applications and resources. They are **not** assigned to specific named users or dedicated shared devices.[LG p.7]

### Full-access tenant licenses

The primary licensing mechanism for certain products that are licensed **only per tenant**, such as Dynamics 365 Electronic Invoicing and Customer Insights.[LG p.7]

### Capacity licenses

Many Dynamics 365 subscriptions come with capacity entitlements or allowances — for data storage, transaction volume, case routing requests, customer profiles, and so on — with the exact entitlement depending on the product and agreement. **Capacity add-on licenses** provide more flexibility for components that are subject to capacity limits.[LG p.7] Default subscription capacities leverage the same tenant and infrastructure and accrue across the single tenant; for example, Dataverse capacities are shared across products such as Sales and Customer Service.[LG p.7] Dataverse capacity add-ons are sold in 1 GB increments for Dataverse Database and 1 GB for Dataverse File or Log capacity, pooled at the tenant level.[LG p.66]

## The Operations family

Three related licenses extend the Operations applications (Commerce, Finance, Human Resources, Project Operations, and Supply Chain Management) at the user, device, and tenant levels respectively.

### Operations – Activity (additional user license)

The Operations – Activity user license provides **limited access** to the Commerce, Finance, Human Resources, Project Operations, and Supply Chain Management applications. Its use rights include **all Team Members use rights**, plus the right to:[LG p.60]

- Approve all Operations – Activity related transactions (see the guide's Appendix G).[LG p.60]
- Create or edit items related to warehousing, receiving, shipping, orders, vendor maintenance, and related budgets.[LG p.60]
- Operate a point-of-sale (POS) device, store manager device, production floor device, or warehouse device.[LG p.60]

### Operations – Device (additional device license)

Operations – Device licenses provide limited access to a subset of Finance, Supply Chain Management, Commerce, and Project Operations capabilities.[LG p.60] They let multiple users operate a licensed **point-of-sale, production floor, warehouse, or store manager** device.[LG p.60] When several users who need only these limited rights work exclusively on shared devices, licensing the devices is generally more cost-effective than licensing the users.[LG p.60]

Operations – Device use rights are also available to Operations – Activity users, but an Operations – Device license does **not** include all the capabilities of the Operations – Activity user license. When a single user works on one or more dedicated personal devices, an Operations – Activity user license is more cost-effective.[LG p.60] A single device can combine any of these functions:[LG p.61]

- **Point of Sale** — customer-facing sales of goods/services at a Commerce location or store.[LG p.61]
- **Store Manager** — managing inventory, cash registers, menus, purchasing, staff, reports, and master data for one location.[LG p.61]
- **Production Floor** — clock-in/out, starting/finishing production jobs, reporting progress, materials consumption, and viewing job documents.[LG p.61]
- **Warehouse Device** — receiving, put-away, internal stock transfers, picking/packing, attribute capture, shipping, and inventory counts.[LG p.61]

### Operations – Order Lines (tenant / transactional license)

Operations – Order Lines is licensed **per tenant** and offers an alternative to user- and device-based licensing. It extends the use of the Commerce, Finance, Project Operations, or Supply Chain Management applications by enabling internal users, partners, customers, connected automated systems, IoT devices, and bots to update specific tables, with **transactional licensing** based on the number of transactions updated.[LG p.61]

It is designed to support external-user scenarios, ease common multiplexing friction, enable licensing of automated/IoT systems without users, and improve cost transparency.[LG p.61] To qualify, a transaction must be **indirect access** (direct use of the application does not qualify) and must only update data in the designated qualifying tables; access to any other tables or user actions requires a user license.[LG p.62] Qualifying order-line types map to specific Operations tables — for example, Sales Order Lines (SALESLINE), Free Text Invoice (CUSTINVOICELINE), Purchase Order (PURCHLINE), and General Journal (LEDGERJOURNALTRANS), among others.[LG p.62]

**Capacity:** Operations – Order Lines is licensed by tenant per month with an annual commitment, and includes an allowance of 100K transactions per month, enforced annually for a total of 1.2 million transactions. Creating new order lines and updating existing ones count against the allowance; deletions do not. Reaching the limit early triggers warnings rather than blocking orders, and the difference can be addressed at the subscription anniversary by purchasing additional capacity.[LG p.62]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.7
- Dynamics 365 Licensing Guide (July 2026), p.60
- Dynamics 365 Licensing Guide (July 2026), p.61
- Dynamics 365 Licensing Guide (July 2026), p.62
- Dynamics 365 Licensing Guide (July 2026), p.66
- [Microsoft Learn — Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

---
[⬅ Back to Index](./Index.md)
