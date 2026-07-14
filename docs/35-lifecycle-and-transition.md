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
[⬅ Back to Index](./Index.md)
