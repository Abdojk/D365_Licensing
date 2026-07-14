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
[⬅ Back to Index](./Index.md)
