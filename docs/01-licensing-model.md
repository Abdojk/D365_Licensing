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
[⬅ Back to Index](./Index.md)
