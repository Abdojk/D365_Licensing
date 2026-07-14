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
[⬅ Back to Index](./Index.md)
