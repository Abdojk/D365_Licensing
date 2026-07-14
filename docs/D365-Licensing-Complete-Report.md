# Dynamics 365 Licensing — Complete Report

> A single compiled report covering everything in this knowledge base, stitched
> from the per-topic files in reading order. **Every factual claim is cited to an
> official Microsoft source** — the *Dynamics 365 Licensing Guide (July 2026)*
> (cited as `[LG p.N]`) and *Microsoft Learn*. No third-party sources; no invented
> prices or numbers.
>
> **Last updated:** 2026-07-14 · **Licensing Guide version:** July 2026.
> This is a derived artifact — the individual files in this folder remain the
> source of truth. Microsoft refreshes the guide monthly and changes pricing
> often; re-verify against the [latest guide](https://aka.ms/dynamicslicensingguide)
> and the [Product Terms](https://www.microsoft.com/licensing/terms) before
> relying on anything commercially.

## Table of Contents

1. [The Dynamics 365 Licensing Model](#the-dynamics-365-licensing-model)
2. [Dynamics 365 License Types](#dynamics-365-license-types)
3. [Base vs Attach Licenses](#base-vs-attach-licenses)
4. [Dynamics 365 Team Members License](#dynamics-365-team-members-license)
5. [How to Buy Dynamics 365 (Purchasing Channels)](#how-to-buy-dynamics-365-purchasing-channels)
6. [Dynamics 365 Sales Licensing](#dynamics-365-sales-licensing)
7. [Dynamics 365 Customer Service Licensing](#dynamics-365-customer-service-licensing)
8. [Dynamics 365 Contact Center Licensing](#dynamics-365-contact-center-licensing)
9. [Dynamics 365 Field Service Licensing](#dynamics-365-field-service-licensing)
10. [Dynamics 365 Finance Licensing](#dynamics-365-finance-licensing)
11. [Dynamics 365 Supply Chain Management Licensing](#dynamics-365-supply-chain-management-licensing)
12. [Dynamics 365 Commerce Licensing](#dynamics-365-commerce-licensing)
13. [Dynamics 365 Human Resources Licensing](#dynamics-365-human-resources-licensing)
14. [Dynamics 365 Project Operations Licensing](#dynamics-365-project-operations-licensing)
15. [Dynamics 365 Business Central Licensing](#dynamics-365-business-central-licensing)
16. [Dynamics 365 Customer Insights Licensing](#dynamics-365-customer-insights-licensing)
17. [Specialized & Add-on Dynamics 365 Apps](#specialized--add-on-dynamics-365-apps)
18. [Copilot, Agents & AI Licensing in Dynamics 365](#copilot-agents--ai-licensing-in-dynamics-365)
19. [Power Platform Use Rights Included with Dynamics 365](#power-platform-use-rights-included-with-dynamics-365)
20. [Capacity & Storage Entitlements](#capacity--storage-entitlements)
21. [Security Roles, Compliance & Additional Licensing Requirements](#security-roles-compliance--additional-licensing-requirements)
22. [Assigning & Administering Licenses](#assigning--administering-licenses)
23. [Subscription Lifecycle & License Transition](#subscription-lifecycle--license-transition)
24. [Dynamics 365 On-Premises Licensing](#dynamics-365-on-premises-licensing)
25. [Glossary of Dynamics 365 Licensing Terms](#glossary-of-dynamics-365-licensing-terms)
26. [Sources Registry — Official Microsoft Only](#sources-registry--official-microsoft-only)

---

# The Dynamics 365 Licensing Model

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Microsoft Dynamics 365 is licensed as a cloud **subscription**. Rather than buying software outright, an organization subscribes to one or more Dynamics 365 cloud services and pays for the licenses it needs. This page explains the core principles that govern how those subscriptions work.

## Subscription-based, cloud use rights

Dynamics 365 cloud subscription licenses grant **non-perpetual** use rights to one or more specific Dynamics 365 cloud services — they do **not** grant rights to on-premises deployment.[LG p.5] Because the rights are non-perpetual, they last only while the subscription is active and paid: there are no buy-out rights, and access to the current licensed product continues only so long as subscription payments are up to date and the product terms are followed.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion) The definitive online service terms are set out in the Microsoft Product Terms.[LG p.5]

## Licensed per User, Device, or Tenant

Dynamics 365 applications are licensed by subscription per **User**, **Device**, or **Tenant**:[LG p.5]

- **User licenses** — Grant access for a named user with personal login credentials, from any device.[LG p.5]
- **Device licenses** — Grant access to a shared device using either assigned or shared logins.[LG p.5]
- **Tenant licenses** — Provide access to a feature or service at the tenant level, regardless of the user or device involved.[LG p.5]

An organization may have a mix of user, device, and tenant licenses.[LG p.5] Microsoft Learn describes the same structure as **assigned** licenses (user and device licenses) and **unassigned** licenses (tenant-level licenses such as additional capacity or add-on sandboxes).[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### The named-user model

A user license is tied to an individual **named user** who signs in with personal credentials. Once assigned, that named user can access the licensed product from any device.[LG p.5] This is distinct from device licensing, where the license is tied to a dedicated shared device that any number of users can operate.[LG p.7]

## Administrators do not need a license

Users who hold the **Power Platform Administrator** or **Dynamics 365 Administrator** role in Microsoft Entra do not require a license. In addition, the **System Administrator** role in Dataverse and in Finance and Operations does not require a license to configure and administer Dynamics 365 applications.[LG p.5] Microsoft Learn confirms that admins don't require any license to configure and administer Dynamics 365 applications, and that users with the finance and operations System Administrator role are exempt from licensing requirements.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

## A license grants legal access, not permissions

Assigning a license is only the first half of granting someone access to Dynamics 365. A license **allows a user to legally access the product**, but it **does not grant permissions inside Dynamics**. To actually use the application, the user (or group) must still be assigned the appropriate **security roles** in Dynamics 365.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) In the Power Platform customer engagement apps, this is stated explicitly: assigning a license adds the user to your environments, but users can't access any apps until they've been assigned at least one security role.[Learn: Grant users access](https://learn.microsoft.com/power-platform/admin/grant-users-access)

In short:

- **License** = the legal right to access the product (compliance).
- **Security role** = the in-product permissions that determine what the user can actually see and do.

## Enterprise and Professional users cannot be mixed

**Enterprise and Professional users may not be deployed in the same environment.**[LG p.5] If an organization needs both tiers, they must be kept in separate environments. See the guide's "Mixed deployments of Dynamics 365 services" section for full details.[LG p.5]

## Licensing is per-app and additive

Dynamics 365 is licensed **per application**, and licensing is **additive**: a user is licensed for the specific applications they need, and additional applications are added on top. When a single user needs more than one full-access application, the model uses **Base and Attach** licensing to keep the combined cost efficient:[LG p.6]

- Every full-access user must first have a **Base license** — when purchasing multiple applications for one user, the first (base) license must be the highest-priced license for that named user.[LG p.6]
- Additional qualifying applications for that same user can then be added as lower-priced **Attach licenses**, which may only be assigned to a user who already has an appropriate qualifying base license. A named user may hold more than one attach license.[LG p.6]

Base and attach licenses are identical in their core capabilities and differ only in price; attach licenses do not include additional platform entitlements beyond those of the assigned base license (with a Customer Insights exception).[LG p.6] The distinction between base, attach, and the various additional license types is covered in detail in [Dynamics 365 License Types](./02-license-types.md).

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.7
- [Microsoft Learn — Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)
- [Microsoft Learn — Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Microsoft Learn — Grant users access](https://learn.microsoft.com/power-platform/admin/grant-users-access)


---

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

# Base vs Attach Licenses

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 is licensed **per application**. When one named user needs the full functionality of more than one Dynamics 365 application, Microsoft uses a **Base and Attach** model so the customer does not pay full price for every app. This page explains how the model works, which products qualify, and how to assign the licenses correctly.

## The cost-saving idea in one sentence

The user's first (highest-value) full license is the **Base** license, and each additional qualifying application for that same user is added as a lower-priced **Attach** license.[LG p.6] Microsoft describes this as "a cost-effective way for a single Dynamics 365 user to obtain full user licensing for multiple Dynamics 365 products."[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

Base and attach licensing applies only to **full-access** user licenses — the users who require the full, feature-rich functionality of one or more Dynamics 365 applications.[LG p.5]

## Base license

- When purchasing multiple Dynamics 365 applications for a single user, the **first application license must be the highest-priced license** (the base license) for that named user.[LG p.6]
- **Every full-access user must have a base license.**[LG p.6]
- Only **user** licenses qualify for base license treatment.[LG p.74]

The guide (and Microsoft Learn) defines the base as "the first product licensed for a given user," sometimes called the first license.[LG p.74] Products that provide **core business functionality** qualify as base licenses — Microsoft Learn gives the examples of Finance, Supply Chain Management, Commerce, Project Operations, and Human Resources.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

## Attach license

- An **attach license** is lower-cost pricing for a product, available to users who require **multiple** Dynamics 365 applications.[LG p.6]
- Attach licenses may **only** be assigned to a user who already holds an **appropriate qualifying base license**.[LG p.6]
- A named user **may hold more than one** attach license.[LG p.6]
- **Not every** Dynamics 365 product qualifies for attach licensing.[LG p.74]

The guide also calls the attach license the "subsequent qualifying application" for a user already licensed for another base product — for example, a user licensed for Commerce might hold an attach license for Customer Service Professional.[LG p.74]

### Base and attach are functionally identical

Base and attach licenses are **identical in their core capabilities** and are differentiated **only in price**.[LG p.6] An attach license does **not** include additional platform entitlements of its own; it is licensed to access the platform entitlements included with the assigned **base** license.[LG p.6] Because default capacity is granted per tenant and is not cumulative, adding more base or attach licenses does not increase your capacity entitlements.[LG p.63]

**Exception — Customer Insights:** Customer Insights attach licenses include the **same default capacity entitlements** as the Customer Insights base license.[LG p.6][LG p.22]

## Which products qualify — Base to eligible Attach

The guide presents the full "Base applications and their qualifying products for attach licensing" matrix as a table on page 6, and directs readers to the Microsoft Product Terms for the authoritative list of availability, prerequisites, and purchase minimums.[LG p.6] The relationships **explicitly stated in the guide text** are:

| Base license | Eligible attach license(s) | Notes / source |
|---|---|---|
| Products providing core business functionality — e.g. Finance, Supply Chain Management, Commerce, Project Operations, Human Resources | One or more additional apps commonly used by the same role, at attach pricing | Base examples per Microsoft Learn.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion) |
| Commerce | Customer Service Professional | Guide's illustrative example.[LG p.74] |
| Business Central Premium | Customer Service Enterprise, Field Service, or Sales Enterprise (at attach pricing) | Stated exception — see below.[LG p.6] |
| Customer Insights (as an attach) | Attaches to Customer Service, Sales, Field Service, Finance, Supply Chain Management, or Commerce | Requires 10+ licenses of one of those apps.[LG p.22] |

> For any base/attach pairing not listed above, consult the page 6 matrix in the guide and the Microsoft Product Terms rather than assuming eligibility — not every product qualifies for attach.[LG p.6][LG p.74]

### Business Central Premium exception

Normally the base must be the highest-priced license for the user. As a stated exception, users who license **Business Central Premium** as their base license are eligible to add **Customer Service Enterprise, Field Service, or Sales Enterprise** at the attach price.[LG p.6] (The guide lists the specific per-user monthly figures; because prices change, see the [official Dynamics 365 pricing page](https://dynamics.microsoft.com/pricing/) for current amounts.)

### Customer Insights attach

Customer Insights attach pricing is available to organizations that have a **minimum of 10 or more** licenses of **one** of the following: Customer Service, Sales, Field Service, Finance, Supply Chain Management, or Commerce.[LG p.22] As noted above, Customer Insights is the exception where the attach license carries the same default capacity entitlements as the base.[LG p.22]

## Assignment sequencing: base first, then attach

The order of assignment matters. Microsoft's guidance is to follow **base-then-attach sequencing**: assign the **base** license (the highest-value app) first, then assign the specific attach license using the **"Attach to Qualifying Dynamics 365 Base Offer"** option if the user needs both.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) For users who span multiple apps, assign one base license (highest-value app) and then the necessary attach licenses.[Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)

Enforcement backs this up: the **system administrator cannot assign an attach license to a user who does not have the required base license**.[LG p.6] If a user still can't sign in after licensing, one of the three things to check is a **missing required attach license**.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

Remember that assigning a license only grants the **legal right** to access the product; the user still needs the appropriate **security roles** in Dynamics 365 to do anything.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

## Minimum license purchase requirements

To activate a Dynamics 365 subscription, you must buy a **minimum quantity of qualifying licenses for some products**. The guide directs customers to the **Microsoft Product Terms** for the details.[LG p.66] Specific minimums that appear in the sources include:

- **Finance and operations apps** — At least **20 base licenses** for Finance, Supply Chain Management, Commerce, Project Operations, or Human Resources are required to create an implementation project in Lifecycle Services; additional projects are added in factors of 20 (e.g. two projects need 40 licenses). If paid base licenses fall below 20, Lifecycle Services begins automated de-provisioning of environments.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)
- **Customer Insights attach** — a **10-seat** minimum of a qualifying app, as described above.[LG p.22]

Because minimums and prices change, treat the Microsoft Product Terms and the [official pricing page](https://dynamics.microsoft.com/pricing/) as the authoritative sources.[LG p.66]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.22
- Dynamics 365 Licensing Guide (July 2026), p.63
- Dynamics 365 Licensing Guide (July 2026), p.66
- Dynamics 365 Licensing Guide (July 2026), p.74
- [Microsoft Learn — Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)
- [Microsoft Learn — Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Microsoft Learn — Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)
- [Microsoft Dynamics 365 pricing](https://dynamics.microsoft.com/pricing/)


---

# Dynamics 365 Team Members License

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

The **Dynamics 365 Team Members** license is a low-cost, limited-use license for light, mostly read-only line-of-business users. This page covers who it is for, what it can and cannot do, the designated Team Member apps, the pre-approved use-right scenarios from Appendix D, and the separate **Business Central Team Members** license.

## Who it is for

Team Members is one of the **additional user** licenses. Additional users often represent a large percentage of an organization's total users: they may consume data or reports from line-of-business systems, complete light tasks like time or expense entry and HR record updates, or use the system without needing full-access capabilities.[LG p.6]

The Team Members license specifically is intended for users who **support multiple lines of business and are not tied to a specific business unit**. Licensed users are granted **read-only access to all Dynamics 365 data** and **basic Dynamics 365 capabilities for designated scenarios**, such as expense entry or updating contacts.[LG p.7] Microsoft Learn describes it as a license for users "whose jobs aren't necessarily tied to a function but who still need to use the basic functionality of a line-of-business system," giving lightweight access through **designated scenarios** built into the Team Member experience.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

## Named-user model

Team Members is a **named user subscription** — it is assigned to an individual user with personal login credentials, who can then access the licensed functionality from any device.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license) As with all named-user licenses, the rights are for that user's **own use** and **not** for activities performed for, or on behalf of, other people. For instance, the license does not grant managers the right to perform the same actions for their direct reports (except for the limited HR manager scenarios noted below).[LG p.60]

## Designated Team Member apps

For the customer engagement apps (Sales, Customer Service, Field Service, and Project Operations), the Team Member experience is delivered through a fixed set of **designated apps** rather than the full application:[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

- **Customer Service Team Member**
- **Sales Team Member**
- **Project Resource Hub** (Project Operations)

The licensing guide grants the Team Members rights through the **Customer Service Team Members, Sales Team Members, and Project Operations Team Members** application modules.[LG p.59]

A user with only a Team Members license sees only the Team Member app (for example, the **Customer Service Team Member** app), not the full hub (e.g. Customer Service Hub or Sales Hub). If such a user tries to reach an app they aren't entitled to — through a bookmark or shared link — they receive an "Invalid License" error once enforcement is applied.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

### What each designated app does

- **Customer Service Team Member** — create, read, and update your **own** cases; use the comments feature to interact with service representatives; and search and view knowledge base articles.[Learn: Customer Service Team Member app](https://learn.microsoft.com/dynamics365/customer-service/customer-service-team-member)
- **Sales Team Member** — customer management (work with contacts or see accounts); lead and opportunity management (see leads/opportunities linked with accounts or contacts); and add notes and activities such as tasks. Administrators can configure the app for additional scenarios, but **not beyond** those listed in the licensing guide.[Learn: Sales Team Member app](https://learn.microsoft.com/dynamics365/sales-enterprise/sales-team-member)

## What Team Members can do

The guide lists the rights granted through the license across two platforms. All rights are for the user's **own use**.[LG p.59][LG p.60]

**Through the Sales / Customer Service / Project Operations Team Member modules (Dataverse platform):**[LG p.59][LG p.60]

- Create, read, update, and delete **contacts, activities, and notes**
- Update their **own** employee information
- Record time, materials, and expenses
- Approve time, expenses, materials, and vendor invoices
- Use reporting and dashboards
- Participate as a **consumer** of Dynamics 365 services, such as responding to surveys

**Additional rights for Finance, Supply Chain, Commerce, Human Resources, and Project Operations (finance and operations platform)** — for the user's own use, or for limited HR use by managers:[LG p.60]

- Record any type of time or expense
- Approve time, expenses, and vendor invoices
- Create requisitions
- Create or edit items related to **quality control** and **departmental budgets**
- Manage their own employee information
- Manage human resources activities for direct employees or those reporting up through the user's reporting chain
- Use Human Resources Self Service functionality (when Human Resources is licensed by the organization)

### Customization limit: 15 tables

A Team Members license holder may customize a **maximum of 15 additional tables** (custom tables or standard Dataverse tables) available to licensed users, per the pre-approved scenarios in the guide's appendices.[LG p.60] Microsoft Learn states the same limit as a maximum of **15 entities** per Team Member app.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

## What Team Members cannot do

- **No custom apps beyond the designated scenarios.** The Team Members subscription does **not** provide access to custom applications and isn't intended for scenarios beyond those listed in the licensing guide.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license) Once enforcement is applied for an environment, Team Member users can only access the designated Team Member applications.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)
- **Not for acting on behalf of others.** Rights are for the user's own use, not for performing actions for other people (with the limited HR manager exception).[LG p.60]
- **Read-only for most data** beyond the pre-approved create/update scenarios.[LG p.7]

If a user needs a **custom app**, the appropriate license is a **Power Apps** per-app or per-user license.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license) If a user needs to access or update Dynamics 365 data **beyond** the Team Member use rights (for example, frequent edits to the Case entity outside self-service), Microsoft recommends assigning the appropriate full license, such as **Dynamics 365 Customer Service Enterprise**.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

## Appendix D: Team Members use-rights overview

Appendix D of the guide summarizes the use rights granted through a Dynamics 365 Team Members license (⚫ = included). It is split across two platforms: the **Dataverse platform** (with Sales, Customer Service, Field Service, Project Operations) and the **Finance and Operations platform** (with Finance, SCM, Commerce, HR, Project Operations). **Appendix D does not apply to Business Central Team Members.**[LG p.76]

### Access, read, and general system use

| Use right | Dataverse platform | F&O platform |
|---|---|---|
| Access anywhere: Web, Mobile, Tablet, Dynamics 365 App for Outlook | ⚫ | |
| Full read across Dynamics 365 applications | ⚫ | ⚫ |
| Activities: create, update, delete | ⚫ | |
| Announcements: create, update, delete | ⚫ | |
| Contacts: create, update, delete | ⚫ | |
| Dynamics 365 mobile client (iPad, Windows) except Field Service | ⚫ | |
| Microsoft Excel: export data, access user reports/charts/dashboards | ⚫ | |
| Notes: create, update, delete | ⚫ | |
| Yammer collaboration (needs Yammer license) | ⚫ | |
| Customization: additional tables (custom or standard Dataverse), 15 per app | ⚫ | |

*Source: [LG p.76]*

### Pre-approved application scenarios

| Scenario | Dataverse platform | F&O platform |
|---|---|---|
| **General** — Employee self-serve | | ⚫ |
| **General** — Manager: review team data, light actions (approve time, expenses, leave) | | ⚫ |
| **General** — Purchase requisitions: create, edit, approve | | ⚫ |
| **General** — Contractor: worker in contractor relationship with legal entities | | ⚫ |
| **Sales** — Employee self-serve: contacts/read accounts; read leads & opportunities linked with accounts (via Sales for Team Members, Power Pages, or API) | ⚫ | |
| **Customer Service** — Employee self-serve: create/update/delete own case; read knowledge articles (via Customer Service for Team Members, Power Pages, or API) | ⚫ | |
| **Field Service** — Work orders: create/update/delete for self-serve; internal create on behalf of customers (cannot resolve/close) | ⚫ | |

*Source: [LG p.76]*

### Finance, Supply Chain, Commerce, and HR scenarios (F&O platform)

| Area | Approved actions |
|---|---|
| **Finance** | View positive pay events; monitor assigned cost objects; create/edit department budget; employee self-serve (personal info, time & expense); approve vendor invoices; respond to inventory needs; manager self-serve; respond to/approve POs (when listed as contact); approve time and expense[LG p.77] |
| **Supply Chain Management** | Employee self-serve; create maintenance requests; approve time & attendance; monitor cost objects; confirm shipments/receipts and update delivery status; view BOM/product details; respond to production-line inventory needs; approve purchase orders; quality control create/edit/update; edit sales order (custom security role); monitor transportation[LG p.77] |
| **Commerce** | Employee self-serve; approve expense; approve invoice; manager self-serve; picking, receiving, stock counting in store/warehouse; approve time[LG p.77][LG p.78] |
| **Human Resources** | Approve absence and leave; employee self-serve (personal info, request leave/absence); manager self-serve (manage direct reports, record/update employee info)[LG p.78] |
| **Project Operations** | Approve time/expense/material usage; create and submit time, expense, and material usage entries; access assigned work for current/future periods; approve purchase order/request and project timesheet[LG p.78] |

*Note: the Project Operations Team Members app provides Dataverse capabilities only when Project Operations is installed in Dataverse; the sales-order edit right requires a custom security role.[LG p.78]*

## Business Central Team Members (separate license)

The **Dynamics 365 Business Central Team Members** license is **not to be confused** with the Dynamics 365 Team Members license, and it is **not** covered by Appendix D.[LG p.59][LG p.76] It is assigned to a named user and provides **read-only access to certain data and limited functionality** within Business Central deployments.[LG p.6]

It grants the named user the following rights, **for their own use only** (not for or on behalf of others):[LG p.59]

- Read data within Business Central
- Update **existing** data and entries (e.g. previously created customer, vendor, or item records; entries are specific accounting information such as a due date on customer ledger entries)
- Approve or reject tasks in all workflows assigned to that user (approvals/rejections can only update data in records the license can access)
- Create, edit, and delete a **sales or purchase quote**
- Create, edit, and delete **personal** information
- Edit **job time sheets** for approval
- Use the Power Apps / Power Automate use rights provided with a Dynamics 365 license
- Customize the Business Central Team Members application module with a **maximum of 15 additional tables** (custom or standard Dataverse tables)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.7
- Dynamics 365 Licensing Guide (July 2026), p.59
- Dynamics 365 Licensing Guide (July 2026), p.60
- Dynamics 365 Licensing Guide (July 2026), p.76
- Dynamics 365 Licensing Guide (July 2026), p.77
- Dynamics 365 Licensing Guide (July 2026), p.78
- [Microsoft Learn — Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)
- [Microsoft Learn — Customer Service Team Member app](https://learn.microsoft.com/dynamics365/customer-service/customer-service-team-member)
- [Microsoft Learn — Sales Team Member app](https://learn.microsoft.com/dynamics365/sales-enterprise/sales-team-member)


---

# How to Buy Dynamics 365 (Purchasing Channels)

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

There are three ways to buy Dynamics 365 products and services. All three offer flexible subscription lengths and support models; the right choice depends on how much implementation help you need, your eligibility, and the scale of your deployment.[LG p.5]

## The three purchasing channels

- **Microsoft Partners** — For customers who need a fully managed and tailored Dynamics 365 solution, connect with a partner.[LG p.5]
- **Microsoft Sales** — For customers who want to learn more about Dynamics 365, discuss use cases, or get pricing information, reach out to the Dynamics 365 Sales team.[LG p.5]
- **Microsoft Online** — Dynamics 365 subscriptions are available to buy directly online.[LG p.5]

## Overview of purchasing options

| | Microsoft Partners | Microsoft Sales | Microsoft Online |
|---|---|---|---|
| **Subscription length** | Monthly / Annual / Multi-Year | Monthly / Annual / Multi-Year | Monthly / Annual / Multi-Year |
| **Customer support** | Industry specific | Account specific | Product specific |
| **Eligibility** | All customers | Managed accounts | All customers |
| **Implementation** | Customized support | Upon request | Independently managed |
| **Scale** | Department / Enterprise-wide | Enterprise-wide | Department / Enterprise-wide |

Source: Dynamics 365 Licensing Guide (July 2026), p.5.[LG p.5]

## Subscription lengths

Regardless of channel, Dynamics 365 subscriptions are available in **monthly**, **annual**, and **multi-year** lengths, giving organizations flexibility to match commitment to need.[LG p.5]

## Choosing a channel

- Choose a **Microsoft Partner** when you want customized implementation support and industry-specific expertise; partners serve all customers and can scale from a single department to an enterprise-wide rollout.[LG p.5]
- Choose **Microsoft Sales** when you are a managed account seeking account-specific support and enterprise-wide scale, with implementation help available upon request.[LG p.5]
- Choose **Microsoft Online** when you prefer to purchase and manage subscriptions independently; it is open to all customers and scales from department to enterprise-wide.[LG p.5]

Microsoft Learn frames the same options from the buyer's side: you can buy through a **Cloud Solution Provider (CSP)** partner (cloud only), buy through a partner using **Volume Licensing** (cloud or on-premises), or — for finance and operations — buy on-premises through a Dynamics partner.[Learn: Before you buy](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/before-you-buy)

## Volume Licensing and CSP

For larger organizations, **Volume Licensing** is a common route. Microsoft Learn notes that organizations with 250 or more Dynamics 365 users may be interested in a Volume Licensing agreement, and that finance and operations applications are available through the Enterprise Agreement, Enterprise Agreement Subscription, Enrollment for Education Solutions, and the Microsoft Products and Services Agreement (MPSA).[Learn: Before you buy](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/before-you-buy) A **Microsoft Cloud Solution Provider** works closely with you to understand your business needs; you can find one through the Microsoft Partner Center portal.[Learn: Before you buy](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/before-you-buy)

## Government (GCC / GCC High / DoD) availability

Select Dynamics 365 products are available to qualified government and eligible private entities through Microsoft's US Government clouds.[Learn: Dynamics 365 US Government](https://learn.microsoft.com/power-platform/admin/microsoft-dynamics-365-government) Eligible customers can purchase available subscriptions and add-ons through these channels, which vary by cloud:[Learn: Dynamics 365 US Government](https://learn.microsoft.com/power-platform/admin/microsoft-dynamics-365-government)

- **GCC** — Volume Licensing (VL) and Cloud Solution Provider (CSP)
- **GCC High** — Volume Licensing (VL)
- **DoD** — Volume Licensing (VL)

## Pricing

Prices change frequently and this knowledge base does not reproduce specific figures. For current pricing, see the official Microsoft Dynamics 365 pricing page.[LG p.6] Microsoft Learn likewise directs buyers to the Dynamics 365 pricing page to explore subscription options and plans.[Learn: Before you buy](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/before-you-buy)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- [Microsoft Learn — Before you buy (finance and operations)](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/before-you-buy)
- [Microsoft Learn — Dynamics 365 US Government](https://learn.microsoft.com/power-platform/admin/microsoft-dynamics-365-government)


---

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

# Dynamics 365 Contact Center Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Contact Center is a **Copilot-first** contact center solution that brings intelligence, automation, and efficiency to every customer engagement channel.[LG p.17] It is a cloud-based product that works with the CRM solution of your choice, or with Dynamics 365 Customer Service Enterprise (as an add-on) or as part of Dynamics 365 Customer Service Premium.[LG p.17][Learn: Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)

## The three Contact Center offers

Contact Center is sold as three per-user offers:[LG p.17-19][LG p.20]

| Offer | Channels | What it includes |
|---|---|---|
| **Contact Center Digital** | Digital messaging + chat | Unified routing (50 record routes/user/month, excluding chats/calls/texts).[LG p.17] |
| **Contact Center Voice** | Native voice | 2,000 Intelligent Voicebot (IVR) min/user/month, 6,000 Call Intelligence min/user/month, 35 GB Dataverse file storage for call recording.[LG p.18] |
| **Contact Center (Digital + Voice)** | Digital + voice | A bundle of both, including all capacity entitlements of each.[LG p.19] |

All three are licensed **per user**.[LG p.17-19]

## Standalone vs. add-on to Customer Service

Contact Center can be consumed in three ways:

1. **Standalone with your own CRM** — Contact Center is built to work with your existing CRM solution.[LG p.17][Learn: Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)
2. **As an add-on to Customer Service Enterprise** — Customer Service Enterprise licensed users are eligible to purchase Contact Center add-ons for Digital, Voice, or both.[LG p.27]
3. **Bundled inside Customer Service Premium** — Customer Service Premium includes Customer Service Enterprise **and** Contact Center (Digital + Voice).[LG p.25][LG p.27]

For the Customer Service side of these combinations, see [Dynamics 365 Customer Service Licensing](./11-customer-service.md).

## Contact Center Digital

Contact Center Digital is licensed per user and provides customer engagement across **digital messaging and chat channels**.[LG p.17] Capacity entitlements include **Unified Routing with 50 record routes/user/month** (excluding chats, calls, and text messages). Copilot credits are purchased separately.[LG p.17]

### Contact Center Digital capacity

| Capability | Included capacity | Add-ons |
|---|---|---|
| Record routing (excluding chats, calls, text messages) | 50 record routes/user/month | Unified Routing add-on: 10K record routes/tenant/month; Copilot Studio: Copilot Credits |

Source: [LG p.17]. Capacity is pooled at the tenant level.[LG p.17]

## Contact Center Voice

Contact Center Voice is licensed per user and provides **native voice capabilities**.[LG p.18] Capacity entitlements include:[LG p.18]

- **2,000 Intelligent Voicebot (IVR) minutes/user/month** — usable as a conversational IVR bot authored in Microsoft Copilot Studio. Any generative AI capabilities require Copilot Credits, purchased separately.[LG p.18]
- **6,000 Call Intelligence (transcription) minutes/user/month** — covers call transcription, sentiment analysis, AI suggestions, call insights, and topic clustering.[LG p.18]
- **35 GB of Dataverse file storage** for call recording (accrued per USL, pooled at tenant level).[LG p.18]

### Contact Center Voice capacity

| Capability | Included capacity | Add-on capacity |
|---|---|---|
| Intelligent Voicebot minutes | 2,000 minutes/user/month | 500 minutes/tenant/month |
| Call Intelligence minutes | 6,000 minutes/user/month | 500 minutes/tenant/month |
| Dataverse File storage (call recording) | 35 GB | — |

Source: [LG p.19]. Capacity is pooled at the tenant level.[LG p.19]

### Microsoft Teams Phone extensibility (Voice)

Teams Phone extensibility lets you configure Teams Phone — with the Teams pay-as-you-go Calling Plan, Operator Connect, or Direct Routing — as a single integrated telephony solution with Contact Center.[LG p.18] Two sets of licenses are required: a **Contact Center service line** (a no-cost Teams Phone Resource Account license plus a PSTN connectivity option) and **Contact Center service reps** (each rep needs a Dynamics 365 Contact Center USL, a Microsoft Teams license, and a Microsoft Teams Phone license).[LG p.18] Teams Phone extensibility pricing is separate and not included in the Contact Center license.[LG p.20] Install/config prerequisites for the voice channel are described on Microsoft Learn.[Learn: Install the voice channel](https://learn.microsoft.com/dynamics365/customer-service/administer/voice-channel-install)

## Contact Center (Digital + Voice)

Contact Center is licensed per user and provides customer engagement across **digital and voice channels** for an all-in-one solution. It is a **bundle** that includes both Contact Center Digital and Contact Center Voice, with all their capacity entitlements.[LG p.19]

## Copilot capabilities

Contact Center is a **Copilot-first** product. Its key capabilities include AI-driven self-service and autonomous agents, AI-led proactive engagement, conversation summaries, IVR and AI agents, sentiment analysis, live transcription and translation, unified routing across voice and digital channels, and Copilot that summarizes conversations, drafts responses/emails, and surfaces knowledge.[Learn: Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)

### Dynamics 365 Contact Center Agents

To use the prebuilt Dynamics 365 Contact Center Agents, a user must be licensed with Dynamics 365 Contact Center.[LG p.17] The agents are the **Knowledge Management Agent**, **Quality Assurance Agent**, **Customer Assist Agent**, and **Customer Intent Agent**.[LG p.17][LG p.20] Across all three offers, the Contact Center Agents **require Copilot Credits, purchased separately**.[LG p.20] Generative AI features of the Intelligent Voicebot (IVR) also require Copilot Credits.[LG p.18]

## Included Dataverse capacity (default, per subscription)

| Capacity | Contact Center Digital | Contact Center Voice | Contact Center (Digital + Voice) |
|---|---|---|---|
| Unified Routing | 50 record routes/user/month | 50 record routes/user/month | 50 record routes/user/month |
| Intelligent Voicebot minutes | — | 2K/user/month | 2K/user/month |
| Call Intelligence minutes | — | 6K/user/month | 6K/user/month |
| **Dataverse Database** | 30 GB | 30 GB | 30 GB |
| Accrued per USL | 250 MB | 250 MB | 250 MB |
| **Dataverse File** | 40 GB | 40 GB | 40 GB |
| Accrued per USL | 2 GB | 35 GB | 35 GB |
| **Dataverse Log** | 2 GB | 2 GB | 2 GB |

Source: [LG p.20]. Unified Routing counts exclude chats, calls, and text messages, and additional capacity is available for purchase.[LG p.20]

## Pricing

This knowledge base does not quote dollar figures because prices change. For current per-user pricing of each Contact Center offer, see the official **[Dynamics 365 Contact Center pricing page](https://www.microsoft.com/dynamics-365/products/contact-center/pricing)**.[Learn: Provision channels in Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/provision-channels) Add-ins can also be purchased through the Microsoft 365 admin center.[Learn: System requirements for Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/system-requirements-contact-center)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.17
- Dynamics 365 Licensing Guide (July 2026), p.18
- Dynamics 365 Licensing Guide (July 2026), p.19
- Dynamics 365 Licensing Guide (July 2026), p.20
- Dynamics 365 Licensing Guide (July 2026), p.25
- Dynamics 365 Licensing Guide (July 2026), p.27
- [Microsoft Learn — Dynamics 365 Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)
- [Microsoft Learn — System requirements for Dynamics 365 Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/system-requirements-contact-center)
- [Microsoft Learn — Provision channels in Dynamics 365 Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/provision-channels)
- [Microsoft Learn — Install the voice channel](https://learn.microsoft.com/dynamics365/customer-service/administer/voice-channel-install)
- [Dynamics 365 Contact Center pricing page](https://www.microsoft.com/dynamics-365/products/contact-center/pricing)


---

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

# Dynamics 365 Finance Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Finance helps medium-sized organizations and enterprises monitor the performance of global financial operations in real time and predict future outcomes. It is **licensed per user** and is available in two editions: **Finance** and **Finance Premium**.[LG p.34] Refer to the Microsoft Product Terms for full details on minimum purchase requirements.[LG p.34]

## Finance vs. Finance Premium

### Finance

Finance provides intelligent, automated, and trusted **core financial management** capabilities, with deep data and process integrations across Dynamics 365, Office 365, and partner applications. Users who need access to **read-only** tasks in business performance planning can use a Finance license.[LG p.34]

### Finance Premium

Finance Premium **expands on the functionality of Finance** and adds **advanced business performance management capabilities**. The distinguishing capability is authoring: users who need to **create plans, budgets, forecasts, or financial analysis reports** require a Finance Premium license.[LG p.34] Finance Premium also includes **1K Copilot Credits per user/month**.[LG p.34]

### What Premium actually adds (verified against the guide)

It is worth being precise here, because several capabilities are commonly assumed to be Premium-only but are in fact included in **both** editions:

| Capability | Finance | Finance Premium |
| --- | --- | --- |
| Core financials | Included | Included |
| Business performance planning (FP&A / xP&A) | Read only | Admin / creator access & inputs |
| Business performance analytics (core reporting and insights) | Included | Included |
| AI and machine learning (AI capabilities within Dynamics 365 Finance) | Included | Included |
| Electronic Invoicing | Included | Included |
| Copilot Credits | — | 1K per user/month |

Source: Finance entitlements and Business Performance Management capabilities tables.[LG p.36][LG p.37]

The practical takeaway: what Premium uniquely unlocks is **admin/creator access to business performance planning** (the ability to build plans, budgets, and forecasts rather than just read them), plus Copilot Credits and larger included capacity.[LG p.36][LG p.37] **Subscription billing** roles and **business performance analytics** core reporting are available in *both* Finance and Finance Premium, not Premium only.[LG p.36]

## Base and Attach eligibility

Finance is a **full-access user license**, so it participates in Dynamics 365 **Base and Attach** licensing.[LG p.6] When a single user is licensed for multiple Dynamics 365 applications, the first (base) license must be the **highest-priced** license for that named user; additional qualifying applications can then be added as lower-priced **attach** licenses.[LG p.6] Attach licenses may only be assigned to a user who already holds an appropriate qualifying base license, and a named user may hold more than one attach license.[LG p.6]

Attach licenses are identical to base licenses in core capabilities and differ only in price; they do **not** add platform entitlements beyond those of the assigned base license.[LG p.6] When assigning licenses, follow **base-then-attach sequencing** — assign the base (e.g. Dynamics 365 Finance) first, then the attach license.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

See the guide's "Base applications and their qualifying products for attach licensing" table for the current list of which applications qualify as base and which qualify for attach pricing.[LG p.6]

## Light users: Team Members and Operations – Activity

Not every user who touches Finance needs a full Finance license. The Finance security-role tables mark many roles as satisfiable with a **Team Members** or **Operations – Activity** license instead:[LG p.34][LG p.35]

- **Team Members** — a named-user license granting **read-only** access to Dynamics 365 data plus basic capabilities for designated scenarios (e.g. approvals, expense entry).[LG p.5] In Finance, roles such as budget contributor, accounts payable positive payment clerk, and the C-suite review roles are available at the Team Members level.[LG p.34]
- **Operations – Activity** — a named-user license giving **limited access** to Finance (and Commerce, Human Resources, Project Operations, and Supply Chain Management). It includes all Team Members use rights plus the right to approve Operations – Activity transactions and create/edit certain items.[LG p.60] Roles such as Invoice Capture Operator are available at this level.[LG p.35]

Use these lighter licenses for users who review, approve, or perform limited financial tasks rather than working across the full application.

## Included capacity and entitlements

Both editions include default tenant and environment capacity; the amounts differ between Finance and Finance Premium:[LG p.37]

| Entitlement | Finance | Finance Premium |
| --- | --- | --- |
| Electronic invoice transactions | 100 per tenant/month | 200 per tenant/month |
| Invoice capture transactions | 100 per tenant/month | 200 per tenant/month |
| Copilot Credits | — | 1K per user/month |
| Dataverse or Operations Database | 90 GB (+5 GB accrued/USL) | 125 GB (+10 GB accrued/USL) |
| Dataverse or Operations File | 80 GB (+5 GB accrued/USL) | 110 GB (+10 GB accrued/USL) |
| Dataverse Log | 2 GB | 3 GB |
| Environments | 1 production (AOS) / 1 non-production (Sandbox Tier 2) | 1 production (AOS) / 1 non-production (Sandbox Tier 2) |

Source: Dynamics 365 Finance Entitlements table.[LG p.37] Additional capacity and environments are available for purchase; default capacity is granted once per tenant and is not increased by adding more base or attach licenses.[LG p.37]

> **Pricing:** Per-user prices change and are not reproduced here. See the official [Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview) for current Finance and Finance Premium pricing.

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.34
- Dynamics 365 Licensing Guide (July 2026), p.35
- Dynamics 365 Licensing Guide (July 2026), p.36
- Dynamics 365 Licensing Guide (July 2026), p.37
- Dynamics 365 Licensing Guide (July 2026), p.60
- [Microsoft Learn — Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Microsoft — Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview)


---

# Dynamics 365 Supply Chain Management Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Supply Chain Management (SCM) gives manufacturers, distributors, and retailers the real-time visibility and intelligence they need for proactive operations. It is **licensed per user** and available in two editions: **Supply Chain Management** and **Supply Chain Management Premium**.[LG p.52] Refer to the Microsoft Product Terms for full details on minimum purchase requirements.[LG p.52]

## SCM vs. SCM Premium

### Supply Chain Management

SCM unifies data and uses predictive insights from AI and IoT — across order fulfillment, planning, procurement, production, inventory, warehousing, and transportation — to maximize operational efficiency, product quality, and profitability.[LG p.52]

### Supply Chain Management Premium

SCM Premium **expands on the functionality of SCM** and adds **Demand Planning** capabilities. Users who need to **create plans, budgets, forecasts, or demand analysis reports** require an SCM Premium license.[LG p.52] SCM Premium also includes **1K Copilot Credits per user/month**.[LG p.52]

In the entitlements table, SCM lists Demand planning as **read only**, while the authoring (admin/creator) side of demand planning is the Premium differentiator.[LG p.57]

## Demand Planning license requirement

Demand Planning is a distinct capability with its own license requirement. To use **Demand planning in Supply Chain Management in a production environment, each relevant user must have a license for it.**[Learn: Demand planning license requirements](https://learn.microsoft.com/dynamics365/supply-chain/demand-planning/demand-planning-licensing) In the licensing guide this maps to the **SCM Premium** edition, which is what includes Demand Planning capabilities for users who create forecasts and demand analysis.[LG p.52][LG p.57]

The Demand Planning security roles reflect this split:[LG p.53]

- **Demand Planning Contributor** — view shared worksheets, save personal views, and collaborate via Teams and in-app comments (available with SCM Premium).
- **Demand Planning Manager** (incl. forecast analyst, market researcher, promotion planner) — configure the demand planning app, view and create planning data, forecasts, tables, transformations, and worksheets, and export plans to SCM (SCM Premium only).

After purchasing the required licenses, an administrator must assign one to each user who needs it.[Learn: Demand planning license requirements](https://learn.microsoft.com/dynamics365/supply-chain/demand-planning/demand-planning-licensing)

> Note: **Planning Optimization** (the master-planning engine) and **DDMRP** are included with standard SCM licenses at no extra cost — these are separate from the Demand Planning capability described above.[Learn: Get started with master planning](https://learn.microsoft.com/dynamics365/supply-chain/master-planning/planning-optimization/get-started)

## Base and Attach eligibility

SCM is a **full-access user license** and participates in Dynamics 365 **Base and Attach** licensing.[LG p.6] When a user is licensed for multiple applications, the first (base) license must be the **highest-priced** license for that named user, and additional qualifying applications may be added as lower-priced **attach** licenses.[LG p.6] Attach licenses may only be assigned to a user who already holds a qualifying base license, and a named user may hold more than one attach license.[LG p.6] Follow **base-then-attach sequencing** when assigning.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) See the guide's base/attach table for the current qualifying combinations.[LG p.6]

## Light and non-user licenses: Activity, Device, and Order Lines

SCM security roles are mapped to several license levels, so many users do not need a full SCM license:[LG p.52][LG p.53][LG p.54]

- **Team Members** — read-only access plus basic capabilities for designated scenarios; roles such as maintenance requester, cost object controller, waterspider, and time registration user are available at this level.[LG p.52]
- **Operations – Activity** — a named-user license giving **limited access** to SCM (and Finance, Commerce, HR, Project Operations). It includes all Team Members rights plus the right to approve Operations – Activity transactions; create or edit items related to warehousing, receiving, shipping, orders, vendor maintenance, and related budgets; and operate a POS, store manager, production floor, or warehouse device.[LG p.60] Roles such as warehouse worker, receiving/shipping clerk, machine operator, and field service technician are available at this level.[LG p.53][LG p.54]
- **Operations – Device** — a per-device license letting **multiple users** operate a shared **production floor device** or **warehouse device** (as well as POS and store manager devices). Where several limited-use users share devices, licensing the device is generally more cost-effective than licensing each user.[LG p.60] A warehouse device covers receiving, put-away, stock transfers, picking, packing, and shipping; a production floor device covers clock-in/out, starting and finishing production jobs, and reporting progress.[LG p.60]
- **Operations – Order Lines** — a **per-tenant** transactional license that extends SCM (and Commerce, Finance, Project Operations) to internal users, partners, customers, connected automated systems, IoT devices, and bots, based on the **number of order-line transactions** rather than named users or devices.[LG p.61] It includes an allowance of **100K transactions per month, enforced annually (1.2 million total)**; creating new order lines and updating existing ones count against the allowance, while deletions do not.[LG p.61] This alleviates licensing friction in multiplexing and IoT scenarios.[LG p.61]

## Included capacity and entitlements

Both editions include default capacity; several amounts differ between SCM and SCM Premium:[LG p.56][LG p.57]

| Entitlement | Supply Chain Management | SCM Premium |
| --- | --- | --- |
| Asset Management | 100 assets per tenant/month | 100 assets per tenant/month |
| Electronic invoice transactions | 100 per tenant/month | 200 per tenant/month |
| Invoice capture transactions | 100 per tenant/month | 200 per tenant/month |
| Order lines (Intelligent Order Management) | 1K order lines per tenant/month | 1K order lines per tenant/month |
| Copilot Credits | — | 1K per user/month |
| Dataverse or Operations Database | 90 GB (+5 GB accrued/USL) | 125 GB (+10 GB accrued/USL) |
| Dataverse or Operations File | 80 GB (+5 GB accrued/USL) | 110 GB (+10 GB accrued/USL) |
| Dataverse Log | 2 GB | 3 GB |
| Environments | 1 production (AOS) / 1 non-production (Sandbox Tier 2) | 1 production (AOS) / 1 non-production (Sandbox Tier 2) |

Source: SCM entitlements and additional-capacity tables.[LG p.56][LG p.57] Additional capacity and environments are available for purchase.[LG p.57]

**Asset Management** capacity is licensed per tenant: you must license enough capacity to meet or exceed the number of assets you manage (each add-on covers 100 assets). Once 50 additional Asset Management capacity licenses (5,000 assets) have been purchased, you may manage an **unlimited** number of assets with no further purchase. Active and inactive assets both count against the limit.[LG p.56][LG p.57]

> **Minimum purchase:** SCM has a **20-seat** minimum purchase requirement; SCM Premium has a **10-seat** minimum. See the Microsoft Product Terms for service-specific terms.[LG p.57]

> **Pricing:** Per-user prices change and are not reproduced here. See the official [Supply Chain Management pricing page](https://www.microsoft.com/dynamics-365/products/supply-chain-management/pricing) for current SCM and SCM Premium pricing.[Learn: Demand planning license requirements](https://learn.microsoft.com/dynamics365/supply-chain/demand-planning/demand-planning-licensing)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.52
- Dynamics 365 Licensing Guide (July 2026), p.53
- Dynamics 365 Licensing Guide (July 2026), p.54
- Dynamics 365 Licensing Guide (July 2026), p.56
- Dynamics 365 Licensing Guide (July 2026), p.57
- Dynamics 365 Licensing Guide (July 2026), p.60
- Dynamics 365 Licensing Guide (July 2026), p.61
- [Microsoft Learn — Demand planning license requirements](https://learn.microsoft.com/dynamics365/supply-chain/demand-planning/demand-planning-licensing)
- [Microsoft Learn — Get started with master planning (Planning Optimization licensing)](https://learn.microsoft.com/dynamics365/supply-chain/master-planning/planning-optimization/get-started)
- [Microsoft Learn — Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Microsoft — Supply Chain Management pricing](https://www.microsoft.com/dynamics-365/products/supply-chain-management/pricing)


---

# Dynamics 365 Commerce Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Commerce helps retailers manage operations, connect employees with data, and deliver shopping experiences that are unified across in-store, back office, and call center channels. It is **licensed per user**, with **e-commerce available as an option**, and it exposes an API-driven, headless commerce engine for integration into emerging channels.[LG p.12]

## The Commerce full user license

A full Commerce user license is intended for employees at the **headquarters and central operations** of a retail organization.[LG p.12] Employees in retail stores generally use lighter licenses instead — an **Operations – Device** or **Operations – Activity** license, or in some cases a **Team Members** license — depending on the scenario and their point-of-sale devices.[LG p.12] Refer to the Product Terms for minimum purchase requirements.[LG p.12]

The Commerce security-role table maps roles to suggested licenses: for example, retail warehouse clerk is available at the Team Members level; retail store manager and retail warehouse manager at Operations – Activity; and headquarters roles such as retail catalog manager, retail merchandising manager, and DOM administrator require the full Commerce license.[LG p.12][LG p.13]

## Base and Attach eligibility

Commerce is a **full-access user license** and participates in Dynamics 365 **Base and Attach** licensing.[LG p.6] When a user is licensed for multiple applications, the first (base) license must be the **highest-priced** license for that named user; additional qualifying applications may be added as lower-priced **attach** licenses, which can only be assigned to a user who already holds a qualifying base license.[LG p.6] Follow **base-then-attach sequencing** when assigning licenses.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) See the guide's base/attach table for the current qualifying combinations.[LG p.6]

## POS and devices: Operations – Device relevance

Because so much retail work happens on shared, in-store hardware, **device licensing** is central to Commerce:

- **Operations – Device** — a per-device license that lets **multiple users** operate a shared **point-of-sale (POS) device** or **store manager device** (as well as production floor and warehouse devices). Where several limited-use users share devices, licensing the device is generally more cost-effective than licensing each user.[LG p.60] A **POS device** is one device in a Commerce location or store, used by any individual, for completing customer-facing sales of goods or services. A **store manager device** is dedicated to store-management tasks such as managing and replenishing inventory, balancing cash registers, purchasing supplies, managing staff, and processing store reports.[LG p.60]
- **Operations – Activity** — a named-user license that also **includes Operations – Device use rights**, letting a user operate POS, store manager, production floor, or warehouse devices, along with the right to approve Operations – Activity transactions and edit certain items.[LG p.60] When a single user needs one or more dedicated personal devices, an Operations – Activity user license is more cost-effective than a device license.[LG p.60]

### Commerce Scale Units and device entitlements

E-commerce and device transactions run on **Commerce Scale Units**, licensed per tenant in three sizes, each including a different allowance of **Operations – Device** entitlements:[LG p.14][LG p.15]

| Commerce Scale Unit – Cloud size | Included Operations – Devices |
| --- | --- |
| Basic | 65 devices per tenant/month |
| Standard | 225 devices per tenant/month |
| Premium | 500 devices per tenant/month |

Source: Commerce Scale Unit – Cloud capacity table.[LG p.15] After the minimum Commerce purchase requirements are met, a default Commerce Scale Unit – Cloud is included with licenses that carry device use rights; these units may only be used to support device transactions.[LG p.14] A **self-hosted** Commerce Scale Unit and its use rights are included at no additional cost with a qualifying minimum purchase of Commerce licenses (it is not sold standalone), though all servers, users, devices, and any Windows/SQL Server licenses accessing it must be licensed separately.[LG p.14]

## E-commerce and transaction tiers

**Dynamics 365 e-Commerce is licensed per tenant** and is what enables Commerce to support e-commerce. Every **e-Commerce Tier** license comes with one **Commerce Scale Unit – Cloud** and includes a specified allowance of e-commerce **transactions** — a transaction being the final purchase of a shopping cart, regardless of item count.[LG p.13] Tiers (1–3, with corresponding overage tiers) are purchased based on anticipated B2B and B2C transaction volume and average order value (AOV) bands; if you need Commerce Scale Unit – Cloud for e-commerce you must buy the appropriate e-Commerce Tier license whether or not you use the Dynamics 365 e-Commerce storefront.[LG p.13][LG p.14] E-Commerce Tier licenses are billed per month, but transactions are **enforced annually**.[LG p.14]

The guide describes Commerce's intelligent forecasting and product recommendations, and lists e-commerce among the channels it unifies; it does not, in the pages reviewed, break out a separate "ratings and reviews" license line — that capability is delivered as part of the e-commerce experience rather than as a distinct SKU in the entitlements tables.[LG p.12][LG p.13]

## Included capacity and entitlements

When you license Commerce, you are automatically entitled to the following default capacity:[LG p.12][LG p.16]

| Entitlement | Commerce |
| --- | --- |
| Order lines (Intelligent Order Management) | 1K order lines per tenant/month |
| Electronic Invoicing | Included |
| Electronic invoice transactions | 100 per tenant/month |
| Invoice capture transactions | 100 per tenant/month |
| Dataverse or Operations Database | 90 GB (+5 GB accrued/USL) |
| Dataverse or Operations File | 80 GB (+5 GB accrued/USL) |
| Dataverse Log | 2 GB |
| Environments | 1 production (AOS) / 1 non-production (Sandbox Tier 2) |

Source: Dynamics 365 Commerce Entitlements table.[LG p.16] Additional capacity and environments are available for purchase.[LG p.16] The **Operations – Order Lines** per-tenant license can also extend Commerce transactionally for external users, partners, and automated systems.[LG p.61]

> **Minimum purchase:** Commerce has a **20-seat** minimum purchase requirement. See the Microsoft Product Terms for service-specific terms.[LG p.16]

> **Pricing:** Per-user and per-tenant prices change and are not reproduced here. See the official [Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview) for current Commerce pricing.

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.12
- Dynamics 365 Licensing Guide (July 2026), p.13
- Dynamics 365 Licensing Guide (July 2026), p.14
- Dynamics 365 Licensing Guide (July 2026), p.15
- Dynamics 365 Licensing Guide (July 2026), p.16
- Dynamics 365 Licensing Guide (July 2026), p.60
- Dynamics 365 Licensing Guide (July 2026), p.61
- [Microsoft Learn — Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Microsoft — Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview)


---

# Dynamics 365 Human Resources Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Human Resources helps organizations optimize compensation, benefits, leave and absence tracking, regulatory and policy compliance, performance feedback, standardized training, and self-service programs. It uses Dataverse and Power Platform to centralize people data and extend the solution, and it is **licensed per user**.[LG p.38] Refer to the Microsoft Product Terms for minimum purchase requirements.[LG p.38]

## The Human Resources full user license

HR professionals are typically licensed as **full-access users** with the Human Resources license.[LG p.38] The full-access license covers the HR-department roles — compensation and benefits manager, HR manager, payroll administrator/manager, recruiter, training manager, benefits management roles, and so on — that the security-role table marks as requiring the Human Resources license.[LG p.38][LG p.39]

Users **outside** the HR organization who only need self-serve access may instead be licensed through the **Team Members** license, the **Human Resources Self Service** license, or the **Operations – Activity** user license.[LG p.38]

## The Human Resources Self Service license

The Human Resources Self Service license enables employee and manager **self-serve** capabilities, such as:[LG p.38]

- Update personal employee information
- Manage the HR activities of direct employees or those reporting up through the user's reporting chain
- Report sick leave
- Submit vacation requests
- View employee benefits
- Approve employee leave as a manager
- View employee information as a manager

Two important limits define this license:[LG p.38]

- It grants access **only to Human Resources** — not to any other Dynamics 365 product.
- It does **not** include full user rights for Human Resources; it provides access to the functionality employees commonly need to manage themselves.

In the security-role table, the self-service roles — self-service contractor, self-service employee, pending worker, self-service manager, and leave and absence manager — are available at the **HR Self Service** level (and also to Team Members and Operations – Activity), whereas the HR-department roles require the full Human Resources license.[LG p.38][LG p.39] Microsoft Learn confirms the HR Self Service license as a valid entitlement to install and access HR apps: for example, the leave-and-absence app requires either a Dynamics 365 Human Resources or a Human Resources Self Service license, and the Recruiting solution requires at least the Human Resources Self Service license.[Learn: HR app for leave and absence](https://learn.microsoft.com/dynamics365/human-resources/hr-app) [Learn: HR recruiting app licensing overview](https://learn.microsoft.com/dynamics365/human-resources/recruit-license)

## Base and Attach eligibility

Human Resources is a **full-access user license** and participates in Dynamics 365 **Base and Attach** licensing.[LG p.6] When a user is licensed for multiple Dynamics 365 applications, the first (base) license must be the **highest-priced** license for that named user; additional qualifying applications may be added as lower-priced **attach** licenses, which can only be assigned to a user who already holds an appropriate qualifying base license.[LG p.6] Follow **base-then-attach sequencing** when assigning.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) See the guide's base/attach table for the current qualifying combinations.[LG p.6]

Note that the **Human Resources Self Service** license is an **additional-user** license, not a full-access base license, and is categorized alongside Team Members as one of the lighter licensing options for employees who need self-serve access.[LG p.5][LG p.38]

## Team Members relevance

The **Team Members** license — a named-user license granting read-only access to Dynamics 365 data plus basic capabilities for designated scenarios — is one of the options for employees outside the HR organization.[LG p.5][LG p.38] In the HR security-role table, the self-service roles (contractor, employee, pending worker, manager, leave and absence manager) are available at the Team Members level as well as at the HR Self Service and Operations – Activity levels.[LG p.38] Choose between Team Members, HR Self Service, and Operations – Activity based on exactly which self-serve tasks a given employee or manager needs to perform.

## Included capacity and entitlements

Licensing Human Resources automatically entitles the tenant to **2,000 Customer Voice responses per tenant/month**, along with the following default capacity:[LG p.38][LG p.40]

| Entitlement | Human Resources |
| --- | --- |
| Customer Voice | 2K responses per tenant/month |
| Dataverse or Operations Database | 90 GB (+1 GB accrued/USL) |
| Dataverse or Operations File | 80 GB (+2 GB accrued/USL) |
| Dataverse Log | 2 GB |
| Environments | 2 Dataverse + 2 AOS |

Source: Dynamics 365 Human Resources Entitlements table.[LG p.40] Additional capacity and environments are available for purchase.[LG p.40] Of the two environments, only one may be in production at any given time, though both may be non-production simultaneously.[LG p.40]

> **Pricing:** Per-user prices change and are not reproduced here. See the official [Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview) for current Human Resources pricing.

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.38
- Dynamics 365 Licensing Guide (July 2026), p.39
- Dynamics 365 Licensing Guide (July 2026), p.40
- [Microsoft Learn — Dynamics 365 Human Resources app for leave and absence](https://learn.microsoft.com/dynamics365/human-resources/hr-app)
- [Microsoft Learn — HR recruiting app licensing overview](https://learn.microsoft.com/dynamics365/human-resources/recruit-license)
- [Microsoft Learn — Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Microsoft — Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview)


---

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

# Dynamics 365 Customer Insights Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Customer Insights is licensed **per tenant** and includes rights to **two separate applications** under a single license.[LG p.21] Unlike most Dynamics 365 apps, Customer Insights uses **capacity-based (tenant-level) licensing** rather than per-user (seat) licensing.[Learn: Manage user accounts, user licenses, and security roles](https://learn.microsoft.com/dynamics365/customer-insights/journeys/admin-users-licenses-roles)

## The two applications

- **Customer Insights - Journeys** (formerly Dynamics 365 Marketing) — create and execute personalized customer journeys across multiple channels, including emails, SMS, push notifications, and more.[LG p.21]
- **Customer Insights - Data** (formerly Dynamics 365 Customer Insights) — unify and enrich customer data with the customer data platform (CDP) to gain deep insight into customer behavior, preferences, and interactions.[LG p.21]

The single Customer Insights license includes rights to install **both** applications in an **unlimited** number of production or sandbox environments.[LG p.21][LG p.23]

## How it is licensed — per tenant, capacity-based

Customer Insights is sold on a **prepaid capacity model**, where capacity is **pooled at the tenant level**.[Learn: Customer Insights FAQs](https://learn.microsoft.com/dynamics365/customer-insights/journeys/ci-faq) All customers must start with the base SKU (a minimum required quantity of capacity), and can then add capacity SKUs as needed.[Learn: Customer Insights FAQs](https://learn.microsoft.com/dynamics365/customer-insights/journeys/ci-faq)

Because it is capacity- (not seat-) based, you can add as many users to a Customer Insights - Journeys environment as you want at no extra charge — any user with an account on the tenant can use the app once they have the environment URL and appropriate security roles.[Learn: Manage user accounts, user licenses, and security roles](https://learn.microsoft.com/dynamics365/customer-insights/journeys/admin-users-licenses-roles) There are no per-user prerequisites for purchasing Customer Insights.[Learn: Customer Insights FAQs](https://learn.microsoft.com/dynamics365/customer-insights/journeys/ci-faq)

Capacity is measured by **two units**:[LG p.21]

- **Unified People** (formerly "Profiles") — a uniquely identified individual created through a collection of defined data source sets from multiple systems (a profile). This meter powers **Customer Insights - Data**. Unknown profiles the system creates using cookies are **not** counted.[LG p.21]
- **Interacted People** (formerly "Active Contacts" / "marketable contacts") — any Dataverse table (contact, lead, account, or an insights profile) interacted with via an inbound or outbound channel (email, SMS, form submission, etc.) in a twelve-month period. This meter powers **Customer Insights - Journeys**. A person stops counting toward the quota if they have not been contacted in the past twelve months; interacted status persists for 12 months after an interaction. People stored in Dataverse but never interacted with do not count.[LG p.21]

The two add-on capacity units are sold **standalone and separately** from one another, so a customer using only Customer Insights - Data (and not Journeys) needs only additional Unified People capacity.[Learn: Customer Insights FAQs](https://learn.microsoft.com/dynamics365/customer-insights/journeys/ci-faq)

## Included capacity

The base license includes the following default entitlements:[LG p.21][LG p.23]

| Entitlement | Included with Customer Insights |
| --- | --- |
| Unified People | 100K per tenant/month |
| Interacted People | 10K per tenant/month |
| Monthly interactions | Up to 10× the Interacted People quota (e.g. 100K interactions at 10K Interacted People) |
| Customer Voice | 2K responses per tenant/month |
| Data scheduled refreshes | 4 per day |
| Dataverse Database | 45 GB |
| Dataverse File | 60 GB |
| Dataverse Log | 4 GB |
| Environments | Unlimited (install both apps across production/sandbox) |

Sources: Customer Insights capacities and Entitlements tables.[LG p.21][LG p.23] The tenant is entitled to monthly interactions of up to **10×** the Interacted People quota; interactions can be sent through out-of-box Journeys channels (email, SMS, push) or custom channels, subject to fair-use limits per environment.[LG p.21] Interactions reset monthly and do **not** roll over; to raise the interaction ceiling you increase the Interacted People entitlement.[Learn: Customer Insights license guidance](https://learn.microsoft.com/dynamics365/customer-insights/journeys/license-setup)

All quota is counted and managed at the **tenant level** across all environment types (sandbox and production).[Learn: Customer Insights license guidance](https://learn.microsoft.com/dynamics365/customer-insights/journeys/license-setup)

## Add-on capacity

Additional capacity can be purchased independently for each application and is added on top of the base/attach included capacity.[LG p.21-22] Add-on packs are tiered:[LG p.22]

**Additional Interacted People packs** (added to the included 10K):[LG p.22]

| Tier | Pack size | Capacity threshold | Min–Max qty |
| --- | --- | --- | --- |
| T1 | 5K | 10K–50K | 1–8 |
| T2 | 10K | 50K–250K | 4–24 |
| T3 | 50K | 250K+ | 5+ |

**Additional Unified People packs** (added to the included 100K):[LG p.22]

| Tier | Pack size | Capacity threshold | Min–Max qty |
| --- | --- | --- | --- |
| T1 | 100K | 100K–500K | 1–4 |
| T2 | 100K | 500K–2M | 4–19 |
| T3 | 100K | 2M+ | 19+ |

Buying add-on capacity does **not** increase the allotment of segments, KPIs, or allowed data scheduled refreshes.[LG p.21] Incremental Dataverse storage is granted with each Unified People and Interacted People add-on pack.[LG p.23]

## Base and attach

Customer Insights is available at both **base** and **attach** pricing. Attach pricing is available for organizations that have a minimum of **10 or more licenses** of ONE of the following Dynamics 365 apps: **Customer Service, Sales, Field Service, Finance, Supply Chain Management, or Commerce** (see Product Terms for prerequisites).[LG p.22]

**Important exception:** Customer Insights **attach** licenses include the **same default capacity entitlements** as the base license.[LG p.22][LG p.23] This differs from the general Dynamics 365 rule, where attach licenses do not carry their own platform entitlements.[LG p.6] The Dataverse entitlements are the same on the full-price base and attach base offers, and can be received only **once** regardless of how many base offers you buy.[Learn: Customer Insights license guidance](https://learn.microsoft.com/dynamics365/customer-insights/journeys/license-setup)

## Notes and prerequisites

- **SMS / phone numbers not included.** Phone numbers and messaging services are **not** part of Customer Insights. Text messaging from within the app requires a separate provider subscription — for example Microsoft Azure Communication Services (ACS) or another third-party SMS provider — integrated with Journeys to actually send messages.[LG p.21][Learn: Purchase Dynamics 365 Customer Insights](https://learn.microsoft.com/dynamics365/customer-insights/journeys/purchase)
- **Legacy outbound marketing.** Adding the legacy outbound marketing application module is still limited by the legacy license model: Marketing standalone licenses are entitled to one installation of the outbound marketing module, while Customer Insights licenses are entitled to four installations.[LG p.22]
- **Legacy standalone SKUs.** As of September 2025 the legacy Dynamics 365 Marketing standalone license is no longer available for renewals; new customers purchase the combined Customer Insights offering.[Learn: Purchase Dynamics 365 Customer Insights](https://learn.microsoft.com/dynamics365/customer-insights/journeys/purchase)
- **Multi-tenant.** Customer Insights licenses are tenant-level; an organization with more than one tenant must purchase licenses for each tenant.[Learn: Customer Insights license guidance](https://learn.microsoft.com/dynamics365/customer-insights/journeys/license-setup)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6, p.21, p.22, p.23.
- [Learn: Purchase Dynamics 365 Customer Insights](https://learn.microsoft.com/dynamics365/customer-insights/journeys/purchase)
- [Learn: Dynamics 365 Customer Insights FAQs](https://learn.microsoft.com/dynamics365/customer-insights/journeys/ci-faq)
- [Learn: Customer Insights license guidance](https://learn.microsoft.com/dynamics365/customer-insights/journeys/license-setup)
- [Learn: Manage user accounts, user licenses, and security roles (Customer Insights - Journeys)](https://learn.microsoft.com/dynamics365/customer-insights/journeys/admin-users-licenses-roles)
- [Learn: Product overview for Dynamics 365 Customer Insights](https://learn.microsoft.com/dynamics365/customer-insights/overview)


---

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

# Capacity & Storage Entitlements

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 subscriptions include a defined amount of storage and environment capacity. This capacity is delivered in two ways: a one-time **default capacity per tenant** that comes with your first base license, plus **additional capacity accrued per user license**. This page presents the guide's capacity tables and explains how the entitlements are calculated and extended.

## How default capacity works

The **first base license (subscription)** for a Dynamics 365 product includes its **default capacity, shared per tenant**. Default capacity is **not cumulative** — additional licenses (base or attach) do **not** increase your initial default per-tenant capacity. However, **each user license accrues additional database and file capacities at no charge** per enterprise base license.[LG p.63]

Key rules:[LG p.63]

- **Attach licenses do not include additional capacity entitlements** (except Customer Insights, which includes the same default capacity as its base license). Attach licenses only let users access the default capacity included with the first base license.
- For bundled offers such as Sales Premium and Microsoft Relationship Sales, the capacity entitlements come with the **core application** (in that case, Sales Enterprise).

Microsoft Learn confirms the same model: the first subscription gives a one-time default capacity limit for the tenant, and Dataverse capacity (database, file, log, and add-ons) is **shared across the tenant and among all environments and workloads**.[Learn: Manage data for customer engagement apps](https://learn.microsoft.com/dynamics365/guidance/implementation-guide/data-management-product-specific-ce)

## Types of default capacity

The guide defines the capacity types as follows:[LG p.64]

- **Dataverse Database** — stores table definitions and data (relational). Increasable tenant-wide in **1 GB increments**.
- **Dataverse File** — stores attachments to notes/emails (documents, images, videos, PDFs, etc.). Increasable tenant-wide in **1 GB increments**.
- **Dataverse Log** — records table/attribute data changes over time (audit/tracing). Increasable tenant-wide in **1 GB increments**.
- **Operations database capacity** — relational database capacity for products with storage requirements outside Dataverse for Apps (inclusive of Production, Nonproduction, Reporting, and Entity Store databases).
- **Operations file capacity** — file/attachment storage for those same products outside Dataverse for Apps.
- **Business Central database storage** — structured database storage.

On the Microsoft side, **database and file entitlements are pooled**: the total Database entitlement covers Dataverse and Operations database usage combined, the total File entitlement covers Dataverse and Operations file usage combined, and **Log entitlement is tracked separately for Dataverse only**.[Learn: Dataverse capacity-based storage details](https://learn.microsoft.com/power-platform/admin/capacity-storage)

## Default & accrued capacity — Dataverse apps

Values below are **per the guide, p.63**. "Included Per Tenant" is the one-time default; "Accrued Per USL" is the additional capacity each user subscription license adds to the tenant pool.[LG p.63]

| License | Dataverse DB — Included/Tenant | Dataverse DB — Accrued/USL | Dataverse File — Included/Tenant | Dataverse File — Accrued/USL | Dataverse Log — Included/Tenant |
|---|---|---|---|---|---|
| Contact Center, Contact Center Voice, Customer Service Premium | 30 GB | 250 MB | 40 GB | see note⁵ | 2 GB |
| Contact Center Digital, Customer Service Enterprise, Field Service³, Sales Enterprise | 30 GB | 250 MB | 40 GB | 2 GB | 2 GB |
| Sales Premium | 45 GB | 500 MB | 60 GB | 2 GB | 2 GB |
| Customer Service Professional, Sales Professional | 30 GB | — | 40 GB | — | 2 GB |
| Intelligent Order Management | 30 GB | — | 40 GB | — | 2 GB |
| Customer Insights (CI)¹ | 45 GB | — | 60 GB | — | 4 GB |
| CI – Interacted People⁴ | — | 1 GB | — | 2 GB | — |
| CI – Unified People⁴ | — | 15 GB | — | 20 GB | — |

Notes: ¹ Customer Insights attach SLs include the same default capacity as CI base SLs; Dataverse entitlements are granted once per tenant, for the first CI base or attach SL; CI $0 user licenses do not accrue additional Dataverse entitlements.[LG p.63] ³ Field Service Contractor SLs do not include any Dataverse capacity entitlements.[LG p.63] ⁴ Per additional 100K Unified People or 50K Interacted People add-on pack.[LG p.63] ⁵ The per-USL Dataverse File accrual for this combined row is not legibly reproduced in the extracted source; refer to the guide, p.63, for the exact figure.

## Default & accrued capacity — Operations (F&O) apps

For the finance and operations applications, capacity is expressed as **Dataverse or Operations** database and file, plus Dataverse Log (per guide, p.63):[LG p.63]

| License | Dataverse Log — Included/Tenant | D. or Operations DB — Included/Tenant | D. or Operations DB — Accrued/USL | D. or Operations File — Included/Tenant | D. or Operations File — Accrued/USL |
|---|---|---|---|---|---|
| Commerce, Finance, Project Operations, Supply Chain Management | 2 GB | 90 GB | 5 GB | 80 GB | 5 GB |
| Finance Premium, Supply Chain Management Premium | 3 GB | 125 GB | 10 GB | 110 GB | 10 GB |
| Human Resources | 2 GB | 90 GB | 1 GB | 80 GB | 2 GB |
| Operations – Activity | — | — | 1 GB | — | 2 GB |
| Operations – Device | — | — | 2 GB | — | 3 GB |

## Business Central database capacity

Per guide, p.64:[LG p.64]

| License | BC Database — Included/Tenant | BC Database — Accrued/USL | Production env/Tenant | Nonproduction env/Tenant |
|---|---|---|---|---|
| BC Essentials | 80 GB | 3 GB | 1 BC | 3 |
| BC Premium | 80 GB | 5 GB | 1 BC | 3 |
| BC Device | — | 1.5 GB/device | — | — |

## Environment entitlements

Environments come in two forms:[LG p.65]

- **Production** — a service accessed by end users, designed and scaled to process live/real-time data for ongoing business operations, deployed within a single geographic region. For F&O apps this is an **Application Object Server (AOS)** environment; for customer engagement apps and Power Platform it is a **Dataverse environment**; for Business Central it is a **Business Central environment**.
- **Nonproduction** — user acceptance testing (UAT), sandbox, and testing environments; these **cannot** process live/real-time data for ongoing business operations.

Environment entitlements for the F&O and Customer Insights apps (guide, p.64):[LG p.64]

| License | Production env/Tenant | Nonproduction env/Tenant |
|---|---|---|
| Commerce, Finance, Project Operations, Supply Chain Management | 1 AOS | 1 Sandbox Tier 2 |
| Customer Insights | Unlimited¹ | — |
| Finance Premium, Human Resources², Supply Chain Management Premium | 1 AOS | 1 Sandbox Tier 2 |

Notes: ¹ Includes entitlements to install both the Customer Insights – Journeys and Customer Insights – Data applications in an unlimited number of production or sandbox environments.[LG p.64] ² Before May 1, 2025, for Human Resources only one environment may be in production at a time, but both may be nonproduction.[LG p.64]

> The AOS production environment for Finance, Supply Chain Management, Commerce, and Project Operations comes with disaster recovery and high availability and is monitored 24×7. Microsoft provisions it only after the implementation nears the operational phase, following completion of the required Lifecycle Services (LCS) activities.[LG p.65]

The Supply Chain Management entitlement page corroborates these figures — 1 production (AOS) / 1 non-production (Sandbox Tier 2) — and shows the Premium tier's higher storage: Dataverse or Operations Database 125 GB, File 110 GB, and Log 3 GB, versus 90 GB / 80 GB / 2 GB for the base tier.[LG p.57]

## Per-user (accrued) capacity from the Power Platform

Because Dynamics 365 runs on Dataverse, the same per-license accrual model documented for Power Platform applies. Microsoft Learn publishes the standalone accruals — for example a Power Apps per-user license adds **250 MB** Dataverse database and **2 GB** Dataverse file capacity to the tenant pool, and a Power Automate per-user license likewise adds **250 MB** database and **2 GB** file (log accrual is 0 in both cases).[Learn: Power Platform licensing FAQs](https://learn.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq) There are additional Microsoft subscriptions beyond Dynamics 365 that grant Dataverse capacity — see the Power Platform Licensing Guide for those entitlements.[LG p.64]

## Other metered capacity

- **Power Platform requests** (formerly API call requests): Power Apps and Power Automate usage counts against the Power Platform request entitlements provided by your license; exceeding daily limits can incur overage charges.[LG p.65]
- **Power Pages**: capacity is enforced monthly, based on authenticated users per website per month and anonymous users per website per month.[LG p.65]
- **Microsoft Copilot Studio**: capacity is enforced monthly, and unused Copilot Credits do **not** carry over month to month.[LG p.65] (See [Copilot, Agents & AI Licensing](./30-copilot-and-ai.md).)

## Capacity add-ons

If the default subscription capacity is not sufficient, **additional capacity is available for purchase** for Power Platform, Dataverse, Operations, and Business Central capacity, and for sandbox environments.[LG p.65] Power Platform add-ons include:[LG p.65]

- **Power Platform Requests add-on** — increases the daily service limits for Power Platform requests.
- **Power Pages capacity packs** — align with peak monthly anticipated usage.

Dataverse database, file, and log capacity add-ons are sold in **1 GB increments** and shared tenant-wide.[LG p.64] Microsoft Learn notes that database, log, and file capacity are enforced independently for overage purposes — excess capacity in one type (for example, file) **cannot** offset a deficit in another (for example, database or log).[Learn: Dataverse capacity-based storage details](https://learn.microsoft.com/power-platform/admin/capacity-storage) When capacity runs low, admins can free up storage, delete environments, purchase add-ons, or set up a pay-as-you-go plan billed through Azure.[Learn: Dataverse capacity-based storage details](https://learn.microsoft.com/power-platform/admin/capacity-storage)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.57
- Dynamics 365 Licensing Guide (July 2026), p.63
- Dynamics 365 Licensing Guide (July 2026), p.64
- Dynamics 365 Licensing Guide (July 2026), p.65
- [Microsoft Learn — Dataverse capacity-based storage details](https://learn.microsoft.com/power-platform/admin/capacity-storage)
- [Microsoft Learn — Power Platform licensing FAQs](https://learn.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq)
- [Microsoft Learn — Manage data for customer engagement apps](https://learn.microsoft.com/dynamics365/guidance/implementation-guide/data-management-product-specific-ce)


---

# Security Roles, Compliance & Additional Licensing Requirements

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

In Dynamics 365, a paid subscription license grants legal access, but **security roles** determine what a user can actually do — and in the Operations (finance and operations) apps, those same security roles drive *which* license each user requires. This page explains how role-based security maps to license requirements, and then covers the "Additional Licensing Requirements" rules from the guide: minimum purchases, external users, multiplexing, dual-use rights vs. dual write, and customization licensing (Appendices F and G).

## How security roles drive license requirements

### Roles, duties, and privileges

You give users access to functionality by assigning each user one or more **security roles**. For Commerce, Finance, Finance Premium, Human Resources, Project Operations, Supply Chain Management, and Supply Chain Management Premium, each out-of-the-box security role combines a meaningful package of functionality and access rights, and the required license is defined in the guide's use-rights tables.[LG p.80] Assigning a security role to a user provides access to functionality; the licensing requirement for these applications is determined by the role-based security assigned to each user.[LG p.80]

Developers build security roles from a hierarchy of subroles, duties, privileges, and directly referenced securable objects. Because the security roles you assign to enabled users determine the licensing requirements, a licensing requirement is assigned to every securable object or resource included in a user role.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

### The "highest classification wins" rule

The finance and operations apps have over 10,000 securable objects, each mapped (classified) to a license type — full user, Operations – Activity, Team Members, or Human Resources Self Service. A user with a given license has access to each securable object classified **at or below** that license type. Therefore, the required license for a user is determined by the **highest classification of the securable object the user needs access to**.[LG p.81]

For example, if an accountant is assigned a role that includes access to a securable object classified as "Finance, SCM or Commerce App," that person needs a full user license. Full user licensing includes Team Members access, so securable objects classified at the Team Members level are available to any user with a Team Members license or higher.[LG p.81]

This is why a single "write" privilege can escalate a user into a higher license tier: the Team Members and Operations – Activity licenses are designed for light or read-only usage, but one write privilege can push a user up to a full app license.[Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)

### Customizing which actions a user can perform

The guide describes three ways to fine-tune actions — and their licensing consequences:[LG p.82]

- **Assigning multiple roles to a single user** — A user can hold several roles and still need only a single user license. The required license is the highest tier among the assigned roles. For example, a user with both the Buying agent role (Activity classification) and the Accounts payable role (Finance classification) needs only a full Finance user license.[LG p.82]
- **Changing the securable objects associated with a role** — If you customize a role (e.g., add "Approve vendor disbursement journal," a full-user-level object, to a Buying agent role), every user assigned that customized role then requires a full user license, because the license is set by the highest-level action allowed.[LG p.82]
- **Changing the securable objects associated with an individual** — You can assign specific actions to specific users. For example, if 20 employees hold the field technician role but only 5 must approve posting of service orders, you assign that securable object to those 5 individuals — who then need a full user license, while the other 15 need only the Team Members license.[LG p.82]

You and your partners may also **create securable objects** for specific scenarios; each new object must be mapped to the user license type that best matches its use, based on the guide's license definitions.[LG p.82]

### User Security Governance (finance and operations)

**User Security Governance (USG)** helps organizations align their security architecture with business processes and optimize licenses. It provides process-based roles, duties, and privileges; segregation-of-duties reporting; temporary and privileged-user access management; and reports that include **license indicators by role, duty, privilege, and entry point**.[Learn: User security governance overview](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/sysadmin/security-gov-overview)

To understand *why* a user needs a particular license, use the **License usage summary** page (System administration > Security > Security governance > License usage summary), which offers a layered view of how permissions are exercised and how responsibilities map to role types. Drill into the **Role → Duty → Privilege** chain to see each item's license status:[Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)

| License tag | Meaning |
|---|---|
| **Entitled** | The action or privilege is covered by the current license and doesn't trigger a higher license. |
| **Not Entitled** | The action or privilege isn't covered and requires a higher or different license to be compliant. |
| **Not Required** | The action or privilege is inherited in the system user and isn't included in license computation. |

_Source: [Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)_

The **Assign roles to user** dialog (System administration > Security > Users) shows the impact on licensing when you assign roles and gives an overview of the licensing requirement for each role; custom roles can require licenses for more than one application. If a role has unexpected licensing requirements, use the USG workspace to find the security roles and permissions driving them.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

To keep licensing compliant, disable inactive users so they don't distort license requirements, and regularly audit security settings after updates. The **System Administrator** role is special: it grants full access to manage system artifacts, and users with this role are **exempt from licensing requirements** — administrators don't need to purchase licenses to configure and administer Dynamics 365.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

## Additional licensing requirements

### Minimum license purchase requirements

To activate a Dynamics 365 subscription, you must buy a minimum quantity of qualifying licenses for some products. See the Product Terms for the details of minimum purchase requirements.[LG p.66]

For the finance and operations apps specifically, you need at least **20 base licenses** for Finance, Supply Chain Management, Commerce, Project Operations, or Human Resources to create a Lifecycle Services implementation project. The number of projects you can create is a factor of 20 — two projects require 40 licenses, and so on.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### Licensing requirements for external users

**External users do not require user licenses** to access Dynamics 365 applications. However, custom applications that give external users access to Dynamics 365 are covered under Power Apps use rights for Dynamics 365, as defined in the Power Platform Licensing Guide.[LG p.66]

The guide defines **External Users** as users that are *not*: (a) employees of the customer or its affiliates; (b) contractors or agents who typically work for the customer or its affiliates for more than 30 hours on average per week; or (c) contractors or agents who typically work onsite for the customer or its affiliates on each working day.[LG p.67]

Key points:[LG p.67]

- Limited external user access is included with your internal user licenses, but the graphical interfaces for Business Central, Sales, Customer Service, Field Service, and Project Operations **may not** be accessed by external users. You may license **Power Pages** to provide external access to your business processes or data.
- Employees, onsite or independent contractors, vendors, agents, or affiliates who perform business processes on your (or your affiliate's) behalf are **internal users** and require licenses. (The Business Central "External Accountant" user is not an external user in this sense.)
- Neither internal nor external access extends to using your environment to provide **outsourced business services** (e.g., day-to-day managing of unaffiliated third-party sales orders, invoices, payroll, etc.). However, internal users may prepare periodic financial statements for your clients — that is not an outsourced business service.

For qualifying indirect transaction types, the **Operations – Order Lines** license may be used by internal or external users for indirect-access scenarios where a user or device license isn't required.[LG p.67]

### Multiplexing

**Multiplexing** refers to using hardware or software to pool connections, reroute information, or reduce the number of devices or users that directly access Dynamics 365. Multiplexing does **NOT** reduce the required number of licenses of any type. Any user or device that accesses Dynamics 365 — directly or indirectly — must be properly licensed or otherwise granted access (such as for external users).[LG p.67]

Licenses are required for users or devices that directly (or indirectly, through a pooling device) input, query, or view data from Dynamics 365. Pooled connections use a non-interactive Dynamics 365 user account (or application access in Business Central) that reaches the system only via the web service layer. Users and devices accessing data indirectly through a website or an API to a separate service (such as Microsoft Outlook) must also be licensed.[LG pp.67-68]

Additional rules:[LG p.68]

- Any user or device that accesses the service, files, data, or content provided by the service through an automated process requires a Dynamics 365 license.
- The number of tiers of hardware or software between Dynamics 365 and the ultimate user or device does not affect the number of licenses required.
- Power Apps users with a Power Apps license may access any **non-restricted** Dataverse table; but Power Apps users/devices that create, update, or delete data in Dynamics 365 **restricted tables** must be properly licensed for Dynamics 365.
- If a licensed user receives data from an unlicensed user and **manually** enters it into Dynamics 365, that is *not* multiplexing, because a licensed user performs the manual action.

For qualifying indirect transaction types, the **Operations – Order Lines** license may again be used for indirect access without a user or device license.[LG p.68]

### Dual-use rights

**Dual-use rights** let you deploy Dynamics applications either in Microsoft's cloud or in a private on-premises / partner-hosted cloud — including running both simultaneously (e.g., migrating an on-premises deployment while running private dev/test in Azure).[LG p.68]

- Properly licensed users do not need additional **client access licenses (CALs)** to access applications hosted on-premises. Dynamics 365 user licenses carry CAL-equivalent rights for equivalent on-premises workloads; device use rights equal the cloud device use rights; and any server licenses otherwise required on-premises are included.[LG p.68]
- Access to on-premises server software via dual-use rights is reserved for users assigned a qualifying Dynamics 365 license and for external users. For the online-to-on-premises license mapping, see the Dynamics 365 Dual Use Rights section in the Product Terms.[LG p.68]
- **Downgrade rights** are limited to Dynamics AX 2012 R3 (or later) for Operations on-premises server, Dynamics CRM 2016 (or later) for Dynamics 365 (On-Premises) Server, and Business Central on-premises (current version minus two).[LG p.69]
- Dual-use rights are **non-perpetual** and expire when the cloud subscription expires. Dynamics CALs have no reciprocal rights to Dynamics 365-only functionality. Licenses for supporting servers (e.g., Windows Server and any CALs) must be obtained separately. Microsoft technical support assists with resulting issues but does not include support for the on-premises deployment itself.[LG p.69]

See the **On-Premises Licensing** page for how the on-premises product and CAL model works.

### Dual write (not the same as dual-use rights)

**Dual write** synchronizes data from the AOS applications — Commerce, Finance, Supply Chain Management, and Project Operations — into Dataverse, configured at the table level so you choose which tables to sync.[LG p.69]

- **No specific license is required to enable dual write**, and no additional licensing is required to configure dual write against **unrestricted** tables.[LG p.69]
- When dual write is configured against a **restricted** table, users who make updates in Dynamics 365 that result in updates to those restricted tables must be appropriately licensed. For example, Finance users leveraging dual write to integrate the Invoice Process (a restricted Dataverse table) need appropriate licenses.[LG p.69]

> **Dual-use rights vs. dual write:** Dual-use rights are a *deployment* right (cloud license also covers equivalent on-premises access, no extra CAL). Dual write is a *data-integration* feature (syncing finance and operations tables into Dataverse). They are unrelated despite the similar names.[LG pp.68-69]

### Extensibility

Dynamics 365 extensibility is provided through **Power Platform**; the available functionality is detailed in the Power Platform Licensing Guide.[LG p.69] Some Dynamics 365 apps **embed Power BI** content (tables and charts) — this is a product feature and needs no Power BI license to view, but customizing the content requires a Power BI Pro or Power BI Premium per-user license; Dynamics 365 users get no standalone Power BI license.[LG pp.69-70] For applicable products, Dynamics 365 licenses also include the right to use custom tables (Appendix D) and to create custom security roles (Appendix F).[LG p.70]

### Field Service integrations

- **Field Service + Finance/Supply Chain Management:** This out-of-the-box integration lets Field Service-licensed users be assigned a security role in Finance and Supply Chain Management; work orders sync to projects and project journals, and Field Service reads inventory via virtual tables (Finance/SCM is the system of record). Integration is available to organizations licensed for D365 Field Service, D365 Finance, and D365 Supply Chain Management. **Direct access** to the Finance or Supply Chain Management application still requires a license.[LG p.70]
- **Field Service + Project Operations (Modern Project Operations):** This integration lets Field Service-licensed users transact against projects, aligning field service with project operations and finance and operations apps. It uses the Modern Project Operations integration to sync Field Service transactions to finance and operations. It does **not** license customers to use Project Operations functionality without a proper license (beyond the Microsoft-built data alignment). **Direct access** to Project Operations, Finance, or Supply Chain Management requires licenses.[LG p.70]

## Appendix G: Operations – Activity approval privileges

Enterprise product licenses include Operations – Activity use rights, and those rights cross applications. For the specific approval privileges below, the guide indicates whether an **Enterprise** or an **Operations – Activity** license is required. A user who needs to approve budget account entry through workflow needs only an Operations – Activity license; a user who also needs to approve a fixed assets journal needs an Enterprise license, which covers both tasks.[LG p.83]

The full table lists dozens of duty/privilege pairs. Most approval privileges require an **Enterprise** license, while a smaller set require only **Operations – Activity**. Examples:[LG pp.83-84]

| Duty | Privilege | License |
|---|---|---|
| Approve budget register entries | Approve budget account entry through workflow | Activity |
| Approve purchase agreement | Approve the purchase agreement through workflow | Activity |
| Maintain purchase order | Maintain purchase order | Activity |
| Maintain catalogs | Review and approve vendor catalogs | Activity |
| Maintain commitment documents | Approve commitment documents through workflow | Activity |
| Retail catalog approval workflow duty | Retail catalog approval workflow privilege | Activity |
| Approve customer invoices | Approve free text invoices | Enterprise |
| Approve vendor payment transactions | Approve vendor disbursement journal | Enterprise |
| Approve fixed assets transactions | Approve fixed assets journal | Enterprise |
| Approve ledger transactions | Approve ledger journal | Enterprise |
| Approve BOMs | Approve BOMs / Approve BOM versions | Enterprise |
| Approve routes | Approve routes / Approve route versions | Enterprise |

_Selected rows; these privileges apply when the relevant configuration key is on. See the guide for the complete list. Source: [LG pp.83-84]_

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.66 (Additional licensing requirements: minimum purchase, external users)
- Dynamics 365 Licensing Guide (July 2026), p.67 (External users, multiplexing)
- Dynamics 365 Licensing Guide (July 2026), p.68 (Multiplexing, dual-use rights)
- Dynamics 365 Licensing Guide (July 2026), p.69 (Dual-use rights, dual write, extensibility)
- Dynamics 365 Licensing Guide (July 2026), p.70 (Extensibility, Field Service integrations)
- Dynamics 365 Licensing Guide (July 2026), p.80 (Appendix F: security role assignment)
- Dynamics 365 Licensing Guide (July 2026), p.81 (Appendix F: customization licensing, highest-classification rule)
- Dynamics 365 Licensing Guide (July 2026), p.82 (Appendix F: multiple roles, changing securable objects)
- Dynamics 365 Licensing Guide (July 2026), pp.83-84 (Appendix G: Operations – Activity approval privileges)
- [Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [User security governance overview](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/sysadmin/security-gov-overview)
- [Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)
- [Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)


---

# Assigning & Administering Licenses

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Buying a Dynamics 365 subscription is only the first step. Each license must be **assigned** to a user (individually or through a group), and — separately — each user must be granted the right **security role** inside Dynamics 365. This page walks through assignment in the Microsoft 365 admin center, group-based licensing, the base-then-attach order, propagation delays, and how to view license consumption.

## Purchase, then assign

Customers must acquire and assign appropriate subscription licenses for their users in the **Microsoft 365 admin center**, following Microsoft's Product Terms. You can view available and assigned licenses under **Licenses** in the admin center.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

You need one user license per person with an active user record who signs in. When adding a new person, the account form shows how many user licenses are available; you can buy more from **Billing > Purchase Services**. Note that each invitation you issue also consumes a user license until the invitation expires (two weeks after issue), and each user license requires a unique Microsoft account.[Learn: Assign licenses (Power Platform)](https://learn.microsoft.com/power-platform/admin/assign-licenses)

## Assignment grants access, not permissions

This is the single most important administrative point: **assigning a license lets a user legally access the product, but it does not grant permissions inside Dynamics.** You must still assign the user (or their group) the appropriate **security role** in Dynamics 365.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

For customer engagement apps, licensed users must be assigned at least one security role to access the apps; roles can be assigned directly or indirectly through a group team. Certain default security roles are auto-assigned based on the license or solution installed, but these give only **Read** access to installed apps and grant no data-access permission — the administrator must still assign the appropriate role for the user to view and interact with data.[Learn: Assign licenses (Power Platform)](https://learn.microsoft.com/power-platform/admin/assign-licenses)

## Option 1 — Assign a license to an individual user

Sign in to the Microsoft 365 admin center as a **Global admin** or **License admin**, then:[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

1. In the left navigation, select **Users > Active users**.
2. Select the user's name.
3. Select **Licenses and apps**.
4. Toggle on the license you want (for example, Dynamics 365 Finance, Commerce, Supply Chain Management, or Team Members).

The license applies after a short **propagation delay of up to one hour**.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

## Option 2 — Assign licenses using groups (group-based licensing)

If you have security groups, mail-enabled groups, or Microsoft 365 groups, you can assign licenses to the group and every member inherits them automatically. When a user is added to or removed from the group, licenses are automatically assigned or unassigned. This is called **group-based licensing** (managed in Microsoft Entra ID).[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)[Learn: Assign Microsoft 365 licenses to user accounts](https://learn.microsoft.com/microsoft-365/enterprise/assign-licenses-to-user-accounts)

From the finance and operations guidance, to assign via a group: sign in to the Microsoft 365 admin center as Global admin or License admin, go to **Teams & groups > Active teams & groups > Security Groups**, open the group, go to **Licenses and apps**, and assign the license. The license applies after a propagation delay of up to one hour.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

Alternatively, from the **Billing > Licenses** page: select **Assign licenses**, search for and select the group, choose the subscription, optionally turn specific apps and services on or off, then select **Assign licenses**.[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)

Membership for licensing groups can be sourced from on-premises directories, from **dynamic membership** rules (attribute-based, e.g., Department equals "sales"), or from delegated-ownership cloud groups.[Learn: Microsoft Entra IAM operations reference guide](https://learn.microsoft.com/entra/architecture/ops-guide-iam)

### Things to know about group-based licensing

- You must be at least a **Groups Administrator, License Administrator, or User Administrator** to assign licenses.[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)
- **Set a usage location** before assigning: users without a specific location inherit the tenant's location; set the location as part of user creation, especially for multi-location tenants.[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)
- **Nested groups aren't supported** — if you assign licenses to a group containing other groups, only first-level members are licensed.[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)
- Make sure you have **enough licenses** for all group members; if you run out, new members aren't licensed until licenses free up.[Learn: Assign Microsoft 365 licenses to user accounts](https://learn.microsoft.com/microsoft-365/enterprise/assign-licenses-to-user-accounts)
- **Moving a user between licensed groups:** add the user to the destination group first, confirm the new license is applied on the user's Licenses page, then remove them from the original group — this avoids a temporary loss of access while processing completes.[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)
- Do **not** configure group-based licensing for groups containing Azure B2B accounts.[Learn: Assign Microsoft 365 licenses to user accounts](https://learn.microsoft.com/microsoft-365/enterprise/assign-licenses-to-user-accounts)

## Base-then-attach assignment order

When a user needs multiple full-user Dynamics 365 apps, follow **base-then-attach sequencing**: assign the **base** license first (for example, Dynamics 365 Finance), then assign the specific attach license — labeled **Attach to Qualifying Dynamics 365 Base Offer** — if the user needs both.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) The same order applies whether you assign to an individual or to a group.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

For users spanning multiple apps, assign a base license (the highest-value app) and then the necessary attach licenses. Where supported, you can deep-link from a Power Platform admin center user record to the Microsoft 365 admin center to speed assignments.[Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)

## Troubleshooting sign-in

If a user still can't sign in after assignment, check three things:[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

1. The user signed in **before the license finished propagating** (allow up to one hour).
2. The user **doesn't have the right security role** assigned in Dynamics.
3. The user is **missing a required attach license**.

Group-based licensing errors (insufficient licenses, conflicting service plans, missing dependencies, proxy-address issues, usage-location problems) appear on the product details page under **Billing > Licenses > Errors & issues**.[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)

## Viewing license consumption (Power Platform admin center)

To compare what you have against what you're using, the **Power Platform admin center** provides license consumption views.

For **finance and operations apps**, the User License Consumption reports compare **Required vs. Purchased vs. Assigned** licenses by product, showing total users requiring a license and base/attach licenses assigned vs. available per product (Finance, Supply Chain Management, Commerce, HR, Project Operations, Team Members, Operations – Activity). You can drill into "Users with unassigned licenses" to see exactly who is missing a license and which one they need, and export the data to CSV.[Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)

For **Power Apps**, a **preview** license consumption experience helps admins track licensing. To view it: sign in to the Power Platform admin center, select **Licensing**, under **Products** select **Power Apps**, then the **Summary** tab.[Learn: View license consumption for Power Apps (preview)](https://learn.microsoft.com/power-platform/admin/view-license-consumption-issues) It reports:[Learn: View license consumption for Power Apps (preview)](https://learn.microsoft.com/power-platform/admin/view-license-consumption-issues)

- **Per user licenses** — license name, licenses used (unique users who launched an app in the last 90 days), assigned licenses, and purchased licenses (including Dynamics 365 licenses that provide Power Apps entitlement).
- **Per app licenses** — allocated vs. purchased per-app licenses.
- **Pay-as-you-go plans** and **monthly consumption trend** charts.

You can also **Download Reports** (Active users; All licensed users; Users requiring licenses in Managed Environments) to find users who hold licenses but aren't using them. Power Platform admins and Dynamics 365 admins can access the summary and environment views and allocate app passes; environment admins can access the environment view.[Learn: View license consumption for Power Apps (preview)](https://learn.microsoft.com/power-platform/admin/view-license-consumption-issues)

> **Preview note:** The Power Apps license consumption experience is a preview feature — not intended for production use, subject to supplemental terms, and may have restricted functionality.[Learn: View license consumption for Power Apps (preview)](https://learn.microsoft.com/power-platform/admin/view-license-consumption-issues)

## Sources

- [Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)
- [Assign licenses (Power Platform)](https://learn.microsoft.com/power-platform/admin/assign-licenses)
- [View license consumption for Power Apps (preview)](https://learn.microsoft.com/power-platform/admin/view-license-consumption-issues)
- [Assign or unassign licenses to a group in the Microsoft 365 admin center](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)
- [Assign Microsoft 365 licenses to user accounts](https://learn.microsoft.com/microsoft-365/enterprise/assign-licenses-to-user-accounts)
- [Microsoft Entra identity and access management operations reference guide](https://learn.microsoft.com/entra/architecture/ops-guide-iam)


---

# Subscription Lifecycle & License Transition

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 licenses are cloud subscriptions with **non-perpetual** rights: they last only while payments are current and the product terms are followed. This page covers the subscription lifecycle, what happens when subscriptions expire (including the data retention/deletion timeline for finance and operations apps), and the Dynamics 365 License Transition Guide for moving from old to new licensing.

## The subscription lifecycle

Dynamics 365 licenses (subscriptions) fall into two broad categories:[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

- **Assigned licenses** — either **user licenses** (access for a named user, from any device) or **device licenses** (access through a specific device via assigned or shared sign-ins). For products with enterprise and professional tiers, user licenses may be referred to as enterprise/base and attach licenses.
- **Unassigned licenses** — provide access to a feature or service at the **tenant** level regardless of user or device, such as additional storage/file capacity or add-on sandboxes.

Licenses grant **non-perpetual** rights (with no buy-out rights) to use specific Dynamics 365 products in the cloud (not on-premises). As long as subscription payments are up to date and you adhere to the product terms, you have access to the current licensed product. Admins don't require any license to configure and administer Dynamics 365.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### Base vs. attach licenses

Microsoft provides a cost-effective way for a single user to get full user licensing across multiple products. Products offering core business functionality qualify as **base licenses** (for example, Finance, Supply Chain Management, Commerce, Project Operations, and Human Resources). Each has one or more additional applications that people in the same roles frequently use, which qualify as **attach licenses** (sometimes called subsequent qualifying applications).[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### Licenses required to create an implementation project

Admins do most of their Lifecycle Services (LCS) work inside an **implementation project**, where they can deploy a sandbox and a production environment plus purchased add-on sandboxes. You need at least **20 base licenses** for Finance, Supply Chain Management, Commerce, Project Operations, or Human Resources to create an implementation project. The number of projects you can create is a factor of 20 (two projects need 40 licenses, and so on).[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

## What happens when subscriptions expire

Customers regularly adjust their license counts. For finance and operations implementation projects, if the number of **paid base licenses falls below 20**, Lifecycle Services performs a series of automated actions on a business-day schedule.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

| Stage | Timing | What happens | Recoverable? |
|---|---|---|---|
| **1. Banners & notifications** | Immediately on detection | LCS shows banners on project pages and sends email + Message center posts to tenant admins that the project is below the minimum license count. | — |
| **2. Sandboxes disabled** | 4 business days after step 1 | Nonproduction (testing/training/debugging) environments are deallocated first, protecting production. | Yes — renew or show proof of intent |
| **3. Production disabled** | 3 business days after step 2 | The production environment is disabled, beginning downtime for mission-critical workloads. | Yes — renew or show proof of intent |
| **4. Sandboxes deleted** | 3 business days after step 3 | The disabled sandbox environments are deleted. | **No — non-recoverable** |
| **5. Project & production deleted** | 2 business days after step 4 | The project and production environment are deleted, removing all users, uploaded software assets, Azure connectors, and all associated environments. | **No — non-recoverable** |

_Source: [Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)_

**Disabled environments are not yet deleted.** You can recover them by renewing your licenses or by providing proof of intent to renew.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### Manual renewal process for long purchasing cycles

Because purchasing or renewing licenses can be lengthy, Microsoft can prevent the automated actions and re-enable environments if you show **proof of intent to renew**. Create a support ticket that details that you've started the renewal process with your license vendor and submit it to Microsoft Support.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### Cleaning up your Azure subscription

After an implementation project is deleted, LCS loses access to any customer-owned Azure subscription used for cloud-hosted environments, but some resources may remain. Delete resource groups prefixed with **DynamicsDeployments-** in the Azure portal (across all regions used), and remove the deployment service application from the Microsoft Entra tenant using the documented PowerShell cmdlets.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

## The Dynamics 365 License Transition Guide

The **Dynamics 365 License Transition Guide** supports the process of **migrating from old licensing to new licensing**. It offers considerations and recommendations to minimize potential impact and administrative overhead. The guide is available as a download from Microsoft.[Learn: Dynamics 365 license transition guide](https://learn.microsoft.com/dynamics365/get-started/license-transition)

The transition guide helps you:[Learn: Dynamics 365 license transition guide](https://learn.microsoft.com/dynamics365/get-started/license-transition)

- Understand the license subscription lifecycle.
- Understand **service plans and service plan conflicts**.
- Develop a license transition strategy.
- Determine the best license assignment approach.
- Comprehend **license reassignment options** and considerations.
- Find the resources that support the process.

### Service plans and conflicts

A license (SKU) is made up of **service plans** (its components). During a transition, service plan conflicts can arise when overlapping plans are assigned. Group-based licensing surfaces these as errors — conflicting service plans are one of the error types shown on the product details page — which you resolve by adjusting assignments. Administrators can also define which service plans to enable based on job function, so users only see the tools appropriate to their role.[Learn: Dynamics 365 license transition guide](https://learn.microsoft.com/dynamics365/get-started/license-transition)[Learn: Microsoft Entra identity and access management operations reference guide](https://learn.microsoft.com/entra/architecture/ops-guide-iam)

### Reassignment options

License reassignment is a core part of transition planning: the transition guide covers reassignment options and considerations, and the assign/administer workflows let you unassign licenses from users or groups and reassign them to users who need them. When moving users between licensed groups, add them to the destination group before removing them from the source to avoid a gap in access.[Learn: Dynamics 365 license transition guide](https://learn.microsoft.com/dynamics365/get-started/license-transition)[Learn: Assign or unassign licenses to a group](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)

## Related concepts

- For assigning and reassigning licenses, base-then-attach order, and consumption reporting, see **Assigning & Administering Licenses**.
- For how expired cloud subscriptions end dual-use (on-premises) rights, see **Security Roles, Compliance & Additional Licensing Requirements** and **Dynamics 365 On-Premises Licensing**.

## Sources

- [Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)
- [Dynamics 365 license transition guide](https://learn.microsoft.com/dynamics365/get-started/license-transition)
- [Assign or unassign licenses to a group in the Microsoft 365 admin center](https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses)
- [Microsoft Entra identity and access management operations reference guide](https://learn.microsoft.com/entra/architecture/ops-guide-iam)


---

# Dynamics 365 On-Premises Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

While Dynamics 365 is fundamentally a cloud subscription service, Microsoft still supports **on-premises** deployments for some products. These use a traditional server-plus-CAL licensing model rather than per-user cloud subscriptions. This page focuses on **Dynamics 365 Customer Engagement (on-premises)** and contrasts it with the cloud model.

> **Legacy / limited note:** On-premises licensing is a legacy model with limited scope. Cloud Dynamics 365 licenses grant non-perpetual rights to use products **in the cloud, not on-premises**.[LG p.5 — see The Licensing Model page] On-premises access is generally reached through **dual-use rights** (below) attached to cloud licenses, and Dynamics CALs have no reciprocal rights to cloud-only functionality.[LG p.69]

## Dynamics 365 Customer Engagement (on-premises) editions

Dynamics 365 Customer Engagement (on-premises) offers a licensing option that scales from small, to mid-level, to very large deployments.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

- **Dynamics 365 Server** — There is no user limit for this edition. Features include support for multiple organizations, multiple server instances, and separate **role-based service installation**, which lets you increase performance by installing Dynamics 365 Server features on different computers.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

## The server license and product key model

A Dynamics 365 Customer Engagement (on-premises) deployment operates using a **single product key**. However, **each Dynamics 365 Server in a deployment requires a server license**.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

You can view and upgrade a license using the `Get-CrmAccessLicense` and `Set-CrmProductKey` Windows PowerShell commands, or through **Deployment Manager** — a Microsoft Management Console (MMC) snap-in that system administrators use to manage organizations, servers, and licenses for on-premises deployments.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

## Client Access Licenses (CALs)

In addition to the server license, users or devices accessing the on-premises deployment need **Client Access Licenses (CALs)**. You can view and modify client access license types for each user in the **Users** area of the **Settings** area in the Dynamics 365 Customer Engagement (on-premises) web client.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

## Dual-use rights: reaching on-premises from cloud licenses

**Dual-use rights** let properly licensed cloud users access equivalent on-premises workloads without buying additional CALs:[LG p.68]

- Dynamics 365 cloud **user** licenses carry rights equivalent to a **CAL** for accessing equivalent on-premises workloads; **device** use rights equal the cloud device use rights.[LG p.68]
- Any **server licenses** that would otherwise be required for an on-premises deployment are **included** with the Dynamics 365 (cloud) licenses.[LG p.68]
- Access to the on-premises server software via dual-use rights is reserved for users assigned a qualifying Dynamics 365 license and for external users. For the online-to-on-premises license mapping, see the Dynamics 365 Dual Use Rights section in the Product Terms.[LG p.68]

### Downgrade rights

You may use downgrade rights to deploy an earlier version of a server, limited to:[LG p.69]

- **Dynamics AX 2012 R3** (or later) for the Dynamics 365 for Operations on-premises server.
- **Dynamics CRM 2016** (or later) for the Dynamics 365 (On-Premises) Server.
- **Dynamics 365 Business Central, on-premises** server — current released version with downgrade rights of minus two versions.

### Important limitations

- Dual-use rights included with Dynamics 365 licenses are **non-perpetual** and **expire when the cloud subscription expires**.[LG p.69]
- Dynamics CALs have **no reciprocal rights** to functionality provided exclusively to Dynamics 365 (cloud) licenses, nor do dual-use rights imply equivalent capabilities between Dynamics CALs and Dynamics 365 licenses.[LG p.69]
- Licenses for **all supporting servers** (such as Windows Server and any CALs) must be obtained separately.[LG p.69]
- If you deploy with dual-use rights, Microsoft technical support assists with resulting issues, but **support is not included for the on-premises deployment** itself.[LG p.69]

### On-premises support options

If you choose to deploy on-premises, your technical support options are: seek support from your partner; buy professional support incidents from Microsoft; use support incidents from an existing Software Assurance (SA) contract (note: after transitioning from SA, those incidents are no longer available for on-premises); or buy/use Premier or Unified Support resources.[LG p.69]

## Contrast with the cloud subscription model

| Aspect | On-premises | Cloud subscription |
|---|---|---|
| Licensing unit | Server license per server + CALs per user/device | Non-perpetual per-user, per-device, or per-tenant subscription[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion) |
| Activation | Single **product key**; Deployment Manager / PowerShell[Learn: CE on-premises editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing) | License assignment in the Microsoft 365 admin center[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) |
| Rights duration | Server licenses managed locally; dual-use rights end with the cloud subscription[LG p.69] | Non-perpetual — access continues only while payments are current[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion) |
| Supporting infrastructure | Customer provides and licenses Windows Server, SQL, etc. separately[LG p.69] | Managed by Microsoft |
| Microsoft support | Not included for the on-premises deployment; partner/paid options[LG p.69] | Included per the online service terms |

## Where to find the on-premises licensing guides

The guide notes that Dynamics 365 on-premises licensing guides — for **Business Central (on-premises)**, **Dynamics 365 (On-Premises)**, and **Dynamics 365 for Operations on-premises** — are published separately by Microsoft, and that registration may be required to obtain product activation and key information.[LG p.69]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.68 (Dual-use rights, CAL-equivalent and server rights)
- Dynamics 365 Licensing Guide (July 2026), p.69 (Downgrade rights, dual-use limitations, on-premises support, on-premises guides)
- [Microsoft Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)
- [Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)
- [Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)


---

# Glossary of Dynamics 365 Licensing Terms

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Definitions below are taken from the official **Dynamics 365 Licensing Guide
(July 2026), Appendix C: Definitions** (pages 74–75) and other cited sections of
the guide. Quotations are condensed for readability; consult the guide for the
exact legal wording, and the [Product Terms](https://www.microsoft.com/licensing/terms)
for binding use rights.

| Term | Definition |
| --- | --- |
| **Base product / Base license** | The first product licensed for a given user (for example, Commerce). Sometimes called the *first* license. **Only user licenses qualify for base license treatment.** [LG p.74] |
| **Attach license** | A lower-cost license for a product — sometimes called the *subsequent qualifying application* — for a user who is **already licensed for another base product**. Example: a user licensed for Commerce may add a Customer Service Professional attach license. Not every Dynamics 365 product qualifies for attach licensing. [LG p.74] |
| **User license (User SL)** | Grants access to a Dynamics 365 product for a **named user** with personal sign-in credentials, from any device. Each user needs their own license; user licenses **cannot be shared**, but one user may access the product from any number of devices. [LG p.5, p.75] |
| **Device license (Device SL)** | An alternative to user licensing that lets **any number of users** access a product through a **single licensed device** (assigned or shared sign-ins), without separate user licenses. Only the user *or* the device needs a license, not both; you may mix user and device licenses. [LG p.74] |
| **Tenant license** | Some products (such as Customer Insights) are licensed at the **tenant level** instead of per user or device. Confers access to the default environment(s) in the subscription. In some cases admins must assign a no-cost user license to individuals who need access. [LG p.7, p.75] |
| **Capacity license** | A tenant-level license that provides additional capacity or a service (for example, extra storage, add-on environments, or sandbox tiers) regardless of the user or device involved. [LG p.7] |
| **Full-access user** | A user who requires the full, feature-rich functionality of one or more Dynamics 365 applications. Full-access options include **Base** and **Attach** licenses. [LG p.5] |
| **Additional user license** | Lower-cost user licenses with limited functionality — for example **Team Members**, **Operations – Activity**, and app-specific limited licenses. [LG p.6] |
| **Tenant** | A container of uniquely identified domains, users, security groups, and licenses. A single tenant can hold multiple Dynamics 365 (online) environments; an organization may have multiple tenants (e.g., per region). A licensed user in one tenant can only access environments in that same tenant. [LG p.74] |
| **Environment** | A space to store, manage, and share an organization's business data, apps, and flows; also a container that separates apps with different roles, security requirements, or audiences. Each environment belongs to exactly one tenant. [LG p.74] |
| **Workload** | A defined set of business functionality (such as Sales, Customer Service, Finance, or Business Central Essentials) applied to a specific application. [LG p.75] |
| **Privileges** | The level of access required to perform a task; privileges are made up of permissions (e.g., cancel payments, process deposits). [LG p.74] |
| **Securable objects** | Items such as tables (entities), forms, fields, and reports. Access is controlled by assigning security roles that define which actions (create, read, update, delete) a user can perform. [LG p.74] |
| **Multiplexing** | Using hardware or software to pool connections, reroute information, or reduce the number of users/devices that directly access Dynamics 365. Multiplexing does **NOT** reduce the number of licenses required — every user or device that directly or indirectly inputs, queries, or views Dynamics 365 data must be licensed. [LG p.67–68] |
| **External users** | Users who are **not** employees, and not contractors/agents who typically work for you >30 hours/week or on-site each working day. Limited external user access is included with internal user licenses, but the GUIs of Business Central, Sales, Customer Service, Field Service, and Project Operations **may not** be accessed by external users. [LG p.66–67] |
| **Dual use rights** | Rights that allow deploying Dynamics applications in Microsoft's cloud **or** in a private on-premises / partner-hosted cloud, and in some cases simultaneously (e.g., during migration). [LG p.68] |
| **Seeded license (Power Platform)** | Power Apps / Power Automate use rights **included** with qualifying Dynamics 365 licenses, usable **within the context** of the licensed Dynamics 365 application. See Appendix H of the guide. [LG p.85] · [Learn: Power Platform licensing](https://learn.microsoft.com/power-platform/admin/pricing-billing-skus#power-apps-and-power-automate-for-dynamics-365) |
| **Operations – Activity** | An additional (limited) user license for finance and operations apps for users performing a defined set of activity-level tasks. [LG p.60] |
| **Operations – Device** | A device license for finance and operations scenarios (for example, warehouse or shop-floor shared devices). [LG p.60] |
| **Operations – Order Lines** | A tenant/consumption license that may be used by internal or external users for qualifying **indirect** transaction types where a user or device license isn't required. [LG p.61, p.67] |
| **Restricted tables** | Dataverse tables that require a Dynamics 365 license (not just a Power Apps license) to create, update, or delete data in them. [LG p.68] |

## Sources
- Dynamics 365 Licensing Guide (July 2026), Appendix C: Definitions, p.74–75; also p.5–7, p.60–61, p.66–68, p.85.
- [Microsoft Product Terms](https://www.microsoft.com/licensing/terms)
- [Power Platform licensing overview — Power Apps and Power Automate for Dynamics 365 (Microsoft Learn)](https://learn.microsoft.com/power-platform/admin/pricing-billing-skus#power-apps-and-power-automate-for-dynamics-365)


---

# Sources Registry — Official Microsoft Only

> Every source cited anywhere in this knowledge base. **Microsoft-official
> domains only** (`learn.microsoft.com`, `www.microsoft.com`, `go.microsoft.com`,
> `aka.ms`, `dynamics.microsoft.com`, `admin.cloud.microsoft`). No third-party
> blogs, resellers, or aggregators are used. Last updated 2026-07-14.

## Primary authoritative documents

| Source | URL | Notes |
| --- | --- | --- |
| **Dynamics 365 Licensing Guide (July 2026)** | <https://aka.ms/dynamicslicensingguide> (fwlink `LinkId=866544`) | The backbone document. Cited throughout as `[LG p.N]`. Refreshed monthly — always check the latest. |
| **Microsoft Product Terms** | <https://www.microsoft.com/licensing/terms> | Binding use rights; supersedes the guide where they differ. |
| **Dynamics 365 licensing documents hub** | <https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365> | Official repository of licensing guides/briefs. |
| **Dynamics 365 pricing overview** | <https://www.microsoft.com/dynamics-365/pricing-overview> | Current pricing (prices intentionally not reproduced in this KB). |
| **Dynamics 365 documentation (Microsoft Learn)** | <https://learn.microsoft.com/dynamics365/> | Product + licensing technical docs. |

## About the "[LG p.N]" citations

`[LG p.N]` = **Dynamics 365 Licensing Guide, July 2026 edition, page N.** Because
the guide is republished monthly, page numbers are valid for the July 2026
edition only; re-locate the section by heading in newer editions.

## Microsoft Learn & microsoft.com pages cited

### Fundamentals, base/attach, compliance
- <https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion>
- <https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement>
- <https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation>
- <https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/sysadmin/security-gov-overview>
- <https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/before-you-buy>
- <https://learn.microsoft.com/dynamics365/get-started/team-members-license>
- <https://learn.microsoft.com/dynamics365/get-started/license-transition>

### Purchasing, assignment & administration
- <https://learn.microsoft.com/power-platform/admin/grant-users-access>
- <https://learn.microsoft.com/power-platform/admin/assign-licenses>
- <https://learn.microsoft.com/power-platform/admin/view-license-consumption-issues>
- <https://learn.microsoft.com/power-platform/admin/microsoft-dynamics-365-government>
- <https://learn.microsoft.com/microsoft-365/admin/manage/manage-group-licenses>
- <https://learn.microsoft.com/microsoft-365/enterprise/assign-licenses-to-user-accounts>
- <https://learn.microsoft.com/entra/architecture/ops-guide-iam>

### Sales
- <https://learn.microsoft.com/dynamics365/sales/overview>
- <https://learn.microsoft.com/dynamics365/sales/buy-dynamics-365-sales>
- <https://learn.microsoft.com/dynamics365/sales/upgrade-sales-license>
- <https://learn.microsoft.com/dynamics365/sales-enterprise/sales-team-member>
- <https://www.microsoft.com/dynamics-365/products/sales/pricing>

### Customer Service & Contact Center
- <https://learn.microsoft.com/dynamics365/customer-service/customer-service-team-member>
- <https://learn.microsoft.com/dynamics365/customer-service/implement/move-cs-enterprise-cs-professional>
- <https://learn.microsoft.com/dynamics365/customer-service/administer/voice-channel-install>
- <https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center>
- <https://learn.microsoft.com/dynamics365/contact-center/implement/system-requirements-contact-center>
- <https://learn.microsoft.com/dynamics365/contact-center/implement/provision-channels>
- <https://learn.microsoft.com/dynamics365/guidance/reference-architectures/contact-center-dynamics-365-customer-service-premium>
- <https://learn.microsoft.com/troubleshoot/dynamics-365/customer-service/customer-service-admin-center/cant-install-dynamics-365-customer-service-apps-in-existing-environment>
- <https://www.microsoft.com/dynamics-365/products/customer-service/pricing>
- <https://www.microsoft.com/dynamics-365/products/contact-center/pricing>

### Field Service, Project Operations, Customer Insights
- <https://learn.microsoft.com/dynamics365/field-service/buy-fs>
- <https://learn.microsoft.com/dynamics365/field-service/users-licenses-permissions>
- <https://learn.microsoft.com/dynamics365/project-operations/environment/determine-deployment-type>
- <https://learn.microsoft.com/dynamics365/project-operations/environment/lite-deployment>
- <https://learn.microsoft.com/dynamics365/project-operations/team-member/project-operations-team-member>
- <https://learn.microsoft.com/dynamics365/customer-insights/overview>
- <https://learn.microsoft.com/dynamics365/customer-insights/journeys/purchase>
- <https://learn.microsoft.com/dynamics365/customer-insights/journeys/ci-faq>
- <https://learn.microsoft.com/dynamics365/customer-insights/journeys/license-setup>
- <https://learn.microsoft.com/dynamics365/customer-insights/journeys/admin-users-licenses-roles>

### Finance & Operations apps (Finance, SCM, Commerce, HR)
- <https://learn.microsoft.com/dynamics365/supply-chain/demand-planning/demand-planning-licensing>
- <https://learn.microsoft.com/dynamics365/supply-chain/master-planning/planning-optimization/get-started>
- <https://learn.microsoft.com/dynamics365/human-resources/hr-app>
- <https://learn.microsoft.com/dynamics365/human-resources/recruit-license>
- <https://www.microsoft.com/dynamics-365/products/supply-chain-management/pricing>

### Business Central
- <https://learn.microsoft.com/dynamics365/business-central/dev-itpro/deployment/licensing>
- <https://learn.microsoft.com/dynamics365/business-central/ui-experiences>
- <https://learn.microsoft.com/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access>
- <https://learn.microsoft.com/dynamics365/business-central/admin-access-with-m365-license-faq>
- <https://learn.microsoft.com/dynamics365/business-central/finance-accounting>
- <https://learn.microsoft.com/dynamics365/business-central/dev-itpro/administration/get-started-online>
- <https://www.microsoft.com/dynamics-365/products/business-central/>

### Specialized & add-on apps
- <https://learn.microsoft.com/dynamics365/intelligent-order-management/overview>
- <https://learn.microsoft.com/dynamics365/customer-voice/purchase>
- <https://learn.microsoft.com/lifecycle/announcements/dynamics-365-guides-remote-assist-end-of-support>
- <https://learn.microsoft.com/dynamics365/mixed-reality/guides/overview>
- <https://learn.microsoft.com/dynamics365/mixed-reality/guides/requirements>
- <https://learn.microsoft.com/dynamics365/mixed-reality/remote-assist/ra-overview>
- <https://learn.microsoft.com/dynamics365/fraud-protection/how-pp-works>
- <https://learn.microsoft.com/dynamics365/fraud-protection/eos>
- <https://learn.microsoft.com/dynamics365/fraud-protection/faq/service-faq>

### Copilot, Agents, AI & MCP
- <https://learn.microsoft.com/dynamics365/sales/copilot-overview>
- <https://learn.microsoft.com/dynamics365/sales/microsoft-365-copilot-chat-in-sales>
- <https://learn.microsoft.com/dynamics365/sales/sales-copilot-faq>
- <https://learn.microsoft.com/dynamics365/sales/connect-to-model-context-protocol-sales>
- <https://learn.microsoft.com/dynamics365/customer-service/administer/setup-pay-as-you-go>
- <https://learn.microsoft.com/dynamics365/customer-service/administer/configure-customer-service-mcp-server>
- <https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/copilot/copilot-mcp>
- <https://learn.microsoft.com/dynamics365/release-plan/2025wave2/enterprise-resource-planning/finance-operations-crossapp-capabilities/build-agents-dynamics-365-finance-operations-model-context-protocol>
- <https://learn.microsoft.com/microsoft-copilot-studio/billing-licensing>
- <https://learn.microsoft.com/power-platform/admin/manage-copilot-studio-messages-capacity>

### Power Platform overlap & capacity
- <https://learn.microsoft.com/power-platform/admin/pricing-billing-skus>
- <https://learn.microsoft.com/power-platform/admin/managed-environment-licensing>
- <https://learn.microsoft.com/power-platform/admin/power-automate-licensing/faqs>
- <https://learn.microsoft.com/power-platform/admin/power-automate-licensing/deep-dive-on-specific-license>
- <https://learn.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq>
- <https://learn.microsoft.com/power-platform/admin/capacity-storage>
- <https://learn.microsoft.com/dynamics365/guidance/implementation-guide/data-management-product-specific-ce>

### On-premises
- <https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing>

## Excluded (deliberately not used)
Third-party licensing summaries — including reseller and consultancy sites and
social posts — were **excluded by policy**, even where they surfaced in search,
to keep this knowledge base traceable to Microsoft alone.


---

