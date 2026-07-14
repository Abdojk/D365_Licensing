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
[⬅ Back to Index](./Index.md)
