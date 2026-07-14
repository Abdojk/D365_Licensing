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
[⬅ Back to Index](./Index.md)
