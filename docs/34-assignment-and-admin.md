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
[⬅ Back to Index](./Index.md)
