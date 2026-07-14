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
[⬅ Back to Index](./Index.md)
