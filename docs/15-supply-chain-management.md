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
[⬅ Back to Index](./Index.md)
