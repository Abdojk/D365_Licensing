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
[⬅ Back to Index](./Index.md)
