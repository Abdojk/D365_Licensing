# Dynamics 365 On-Premises Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

While Dynamics 365 is fundamentally a cloud subscription service, Microsoft still supports **on-premises** deployments for some products. These use a traditional server-plus-CAL licensing model rather than per-user cloud subscriptions. This page focuses on **Dynamics 365 Customer Engagement (on-premises)** and contrasts it with the cloud model.

> **Legacy / limited note:** On-premises licensing is a legacy model with limited scope. Cloud Dynamics 365 licenses grant non-perpetual rights to use products **in the cloud, not on-premises**.[LG p.5 — see The Licensing Model page] On-premises access is generally reached through **dual-use rights** (below) attached to cloud licenses, and Dynamics CALs have no reciprocal rights to cloud-only functionality.[LG p.69]

## Dynamics 365 Customer Engagement (on-premises) editions

Dynamics 365 Customer Engagement (on-premises) offers a licensing option that scales from small, to mid-level, to very large deployments.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

- **Dynamics 365 Server** — There is no user limit for this edition. Features include support for multiple organizations, multiple server instances, and separate **role-based service installation**, which lets you increase performance by installing Dynamics 365 Server features on different computers.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

## The server license and product key model

A Dynamics 365 Customer Engagement (on-premises) deployment operates using a **single product key**. However, **each Dynamics 365 Server in a deployment requires a server license**.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

You can view and upgrade a license using the `Get-CrmAccessLicense` and `Set-CrmProductKey` Windows PowerShell commands, or through **Deployment Manager** — a Microsoft Management Console (MMC) snap-in that system administrators use to manage organizations, servers, and licenses for on-premises deployments.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

## Client Access Licenses (CALs)

In addition to the server license, users or devices accessing the on-premises deployment need **Client Access Licenses (CALs)**. You can view and modify client access license types for each user in the **Users** area of the **Settings** area in the Dynamics 365 Customer Engagement (on-premises) web client.[Learn: Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)

## Dual-use rights: reaching on-premises from cloud licenses

**Dual-use rights** let properly licensed cloud users access equivalent on-premises workloads without buying additional CALs:[LG p.68]

- Dynamics 365 cloud **user** licenses carry rights equivalent to a **CAL** for accessing equivalent on-premises workloads; **device** use rights equal the cloud device use rights.[LG p.68]
- Any **server licenses** that would otherwise be required for an on-premises deployment are **included** with the Dynamics 365 (cloud) licenses.[LG p.68]
- Access to the on-premises server software via dual-use rights is reserved for users assigned a qualifying Dynamics 365 license and for external users. For the online-to-on-premises license mapping, see the Dynamics 365 Dual Use Rights section in the Product Terms.[LG p.68]

### Downgrade rights

You may use downgrade rights to deploy an earlier version of a server, limited to:[LG p.69]

- **Dynamics AX 2012 R3** (or later) for the Dynamics 365 for Operations on-premises server.
- **Dynamics CRM 2016** (or later) for the Dynamics 365 (On-Premises) Server.
- **Dynamics 365 Business Central, on-premises** server — current released version with downgrade rights of minus two versions.

### Important limitations

- Dual-use rights included with Dynamics 365 licenses are **non-perpetual** and **expire when the cloud subscription expires**.[LG p.69]
- Dynamics CALs have **no reciprocal rights** to functionality provided exclusively to Dynamics 365 (cloud) licenses, nor do dual-use rights imply equivalent capabilities between Dynamics CALs and Dynamics 365 licenses.[LG p.69]
- Licenses for **all supporting servers** (such as Windows Server and any CALs) must be obtained separately.[LG p.69]
- If you deploy with dual-use rights, Microsoft technical support assists with resulting issues, but **support is not included for the on-premises deployment** itself.[LG p.69]

### On-premises support options

If you choose to deploy on-premises, your technical support options are: seek support from your partner; buy professional support incidents from Microsoft; use support incidents from an existing Software Assurance (SA) contract (note: after transitioning from SA, those incidents are no longer available for on-premises); or buy/use Premier or Unified Support resources.[LG p.69]

## Contrast with the cloud subscription model

| Aspect | On-premises | Cloud subscription |
|---|---|---|
| Licensing unit | Server license per server + CALs per user/device | Non-perpetual per-user, per-device, or per-tenant subscription[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion) |
| Activation | Single **product key**; Deployment Manager / PowerShell[Learn: CE on-premises editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing) | License assignment in the Microsoft 365 admin center[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) |
| Rights duration | Server licenses managed locally; dual-use rights end with the cloud subscription[LG p.69] | Non-perpetual — access continues only while payments are current[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion) |
| Supporting infrastructure | Customer provides and licenses Windows Server, SQL, etc. separately[LG p.69] | Managed by Microsoft |
| Microsoft support | Not included for the on-premises deployment; partner/paid options[LG p.69] | Included per the online service terms |

## Where to find the on-premises licensing guides

The guide notes that Dynamics 365 on-premises licensing guides — for **Business Central (on-premises)**, **Dynamics 365 (On-Premises)**, and **Dynamics 365 for Operations on-premises** — are published separately by Microsoft, and that registration may be required to obtain product activation and key information.[LG p.69]

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.68 (Dual-use rights, CAL-equivalent and server rights)
- Dynamics 365 Licensing Guide (July 2026), p.69 (Downgrade rights, dual-use limitations, on-premises support, on-premises guides)
- [Microsoft Dynamics 365 Customer Engagement (on-premises) editions and licensing](https://learn.microsoft.com/dynamics365/customerengagement/on-premises/deploy/microsoft-dynamics-365-editions-and-licensing)
- [Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)
- [Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

---
[⬅ Back to Index](./Index.md)
