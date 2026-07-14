# Security Roles, Compliance & Additional Licensing Requirements

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

In Dynamics 365, a paid subscription license grants legal access, but **security roles** determine what a user can actually do — and in the Operations (finance and operations) apps, those same security roles drive *which* license each user requires. This page explains how role-based security maps to license requirements, and then covers the "Additional Licensing Requirements" rules from the guide: minimum purchases, external users, multiplexing, dual-use rights vs. dual write, and customization licensing (Appendices F and G).

## How security roles drive license requirements

### Roles, duties, and privileges

You give users access to functionality by assigning each user one or more **security roles**. For Commerce, Finance, Finance Premium, Human Resources, Project Operations, Supply Chain Management, and Supply Chain Management Premium, each out-of-the-box security role combines a meaningful package of functionality and access rights, and the required license is defined in the guide's use-rights tables.[LG p.80] Assigning a security role to a user provides access to functionality; the licensing requirement for these applications is determined by the role-based security assigned to each user.[LG p.80]

Developers build security roles from a hierarchy of subroles, duties, privileges, and directly referenced securable objects. Because the security roles you assign to enabled users determine the licensing requirements, a licensing requirement is assigned to every securable object or resource included in a user role.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

### The "highest classification wins" rule

The finance and operations apps have over 10,000 securable objects, each mapped (classified) to a license type — full user, Operations – Activity, Team Members, or Human Resources Self Service. A user with a given license has access to each securable object classified **at or below** that license type. Therefore, the required license for a user is determined by the **highest classification of the securable object the user needs access to**.[LG p.81]

For example, if an accountant is assigned a role that includes access to a securable object classified as "Finance, SCM or Commerce App," that person needs a full user license. Full user licensing includes Team Members access, so securable objects classified at the Team Members level are available to any user with a Team Members license or higher.[LG p.81]

This is why a single "write" privilege can escalate a user into a higher license tier: the Team Members and Operations – Activity licenses are designed for light or read-only usage, but one write privilege can push a user up to a full app license.[Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)

### Customizing which actions a user can perform

The guide describes three ways to fine-tune actions — and their licensing consequences:[LG p.82]

- **Assigning multiple roles to a single user** — A user can hold several roles and still need only a single user license. The required license is the highest tier among the assigned roles. For example, a user with both the Buying agent role (Activity classification) and the Accounts payable role (Finance classification) needs only a full Finance user license.[LG p.82]
- **Changing the securable objects associated with a role** — If you customize a role (e.g., add "Approve vendor disbursement journal," a full-user-level object, to a Buying agent role), every user assigned that customized role then requires a full user license, because the license is set by the highest-level action allowed.[LG p.82]
- **Changing the securable objects associated with an individual** — You can assign specific actions to specific users. For example, if 20 employees hold the field technician role but only 5 must approve posting of service orders, you assign that securable object to those 5 individuals — who then need a full user license, while the other 15 need only the Team Members license.[LG p.82]

You and your partners may also **create securable objects** for specific scenarios; each new object must be mapped to the user license type that best matches its use, based on the guide's license definitions.[LG p.82]

### User Security Governance (finance and operations)

**User Security Governance (USG)** helps organizations align their security architecture with business processes and optimize licenses. It provides process-based roles, duties, and privileges; segregation-of-duties reporting; temporary and privileged-user access management; and reports that include **license indicators by role, duty, privilege, and entry point**.[Learn: User security governance overview](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/sysadmin/security-gov-overview)

To understand *why* a user needs a particular license, use the **License usage summary** page (System administration > Security > Security governance > License usage summary), which offers a layered view of how permissions are exercised and how responsibilities map to role types. Drill into the **Role → Duty → Privilege** chain to see each item's license status:[Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)

| License tag | Meaning |
|---|---|
| **Entitled** | The action or privilege is covered by the current license and doesn't trigger a higher license. |
| **Not Entitled** | The action or privilege isn't covered and requires a higher or different license to be compliant. |
| **Not Required** | The action or privilege is inherited in the system user and isn't included in license computation. |

_Source: [Learn: Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)_

The **Assign roles to user** dialog (System administration > Security > Users) shows the impact on licensing when you assign roles and gives an overview of the licensing requirement for each role; custom roles can require licenses for more than one application. If a role has unexpected licensing requirements, use the USG workspace to find the security roles and permissions driving them.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

To keep licensing compliant, disable inactive users so they don't distort license requirements, and regularly audit security settings after updates. The **System Administrator** role is special: it grants full access to manage system artifacts, and users with this role are **exempt from licensing requirements** — administrators don't need to purchase licenses to configure and administer Dynamics 365.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)

## Additional licensing requirements

### Minimum license purchase requirements

To activate a Dynamics 365 subscription, you must buy a minimum quantity of qualifying licenses for some products. See the Product Terms for the details of minimum purchase requirements.[LG p.66]

For the finance and operations apps specifically, you need at least **20 base licenses** for Finance, Supply Chain Management, Commerce, Project Operations, or Human Resources to create a Lifecycle Services implementation project. The number of projects you can create is a factor of 20 — two projects require 40 licenses, and so on.[Learn: Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

### Licensing requirements for external users

**External users do not require user licenses** to access Dynamics 365 applications. However, custom applications that give external users access to Dynamics 365 are covered under Power Apps use rights for Dynamics 365, as defined in the Power Platform Licensing Guide.[LG p.66]

The guide defines **External Users** as users that are *not*: (a) employees of the customer or its affiliates; (b) contractors or agents who typically work for the customer or its affiliates for more than 30 hours on average per week; or (c) contractors or agents who typically work onsite for the customer or its affiliates on each working day.[LG p.67]

Key points:[LG p.67]

- Limited external user access is included with your internal user licenses, but the graphical interfaces for Business Central, Sales, Customer Service, Field Service, and Project Operations **may not** be accessed by external users. You may license **Power Pages** to provide external access to your business processes or data.
- Employees, onsite or independent contractors, vendors, agents, or affiliates who perform business processes on your (or your affiliate's) behalf are **internal users** and require licenses. (The Business Central "External Accountant" user is not an external user in this sense.)
- Neither internal nor external access extends to using your environment to provide **outsourced business services** (e.g., day-to-day managing of unaffiliated third-party sales orders, invoices, payroll, etc.). However, internal users may prepare periodic financial statements for your clients — that is not an outsourced business service.

For qualifying indirect transaction types, the **Operations – Order Lines** license may be used by internal or external users for indirect-access scenarios where a user or device license isn't required.[LG p.67]

### Multiplexing

**Multiplexing** refers to using hardware or software to pool connections, reroute information, or reduce the number of devices or users that directly access Dynamics 365. Multiplexing does **NOT** reduce the required number of licenses of any type. Any user or device that accesses Dynamics 365 — directly or indirectly — must be properly licensed or otherwise granted access (such as for external users).[LG p.67]

Licenses are required for users or devices that directly (or indirectly, through a pooling device) input, query, or view data from Dynamics 365. Pooled connections use a non-interactive Dynamics 365 user account (or application access in Business Central) that reaches the system only via the web service layer. Users and devices accessing data indirectly through a website or an API to a separate service (such as Microsoft Outlook) must also be licensed.[LG pp.67-68]

Additional rules:[LG p.68]

- Any user or device that accesses the service, files, data, or content provided by the service through an automated process requires a Dynamics 365 license.
- The number of tiers of hardware or software between Dynamics 365 and the ultimate user or device does not affect the number of licenses required.
- Power Apps users with a Power Apps license may access any **non-restricted** Dataverse table; but Power Apps users/devices that create, update, or delete data in Dynamics 365 **restricted tables** must be properly licensed for Dynamics 365.
- If a licensed user receives data from an unlicensed user and **manually** enters it into Dynamics 365, that is *not* multiplexing, because a licensed user performs the manual action.

For qualifying indirect transaction types, the **Operations – Order Lines** license may again be used for indirect access without a user or device license.[LG p.68]

### Dual-use rights

**Dual-use rights** let you deploy Dynamics applications either in Microsoft's cloud or in a private on-premises / partner-hosted cloud — including running both simultaneously (e.g., migrating an on-premises deployment while running private dev/test in Azure).[LG p.68]

- Properly licensed users do not need additional **client access licenses (CALs)** to access applications hosted on-premises. Dynamics 365 user licenses carry CAL-equivalent rights for equivalent on-premises workloads; device use rights equal the cloud device use rights; and any server licenses otherwise required on-premises are included.[LG p.68]
- Access to on-premises server software via dual-use rights is reserved for users assigned a qualifying Dynamics 365 license and for external users. For the online-to-on-premises license mapping, see the Dynamics 365 Dual Use Rights section in the Product Terms.[LG p.68]
- **Downgrade rights** are limited to Dynamics AX 2012 R3 (or later) for Operations on-premises server, Dynamics CRM 2016 (or later) for Dynamics 365 (On-Premises) Server, and Business Central on-premises (current version minus two).[LG p.69]
- Dual-use rights are **non-perpetual** and expire when the cloud subscription expires. Dynamics CALs have no reciprocal rights to Dynamics 365-only functionality. Licenses for supporting servers (e.g., Windows Server and any CALs) must be obtained separately. Microsoft technical support assists with resulting issues but does not include support for the on-premises deployment itself.[LG p.69]

See the **On-Premises Licensing** page for how the on-premises product and CAL model works.

### Dual write (not the same as dual-use rights)

**Dual write** synchronizes data from the AOS applications — Commerce, Finance, Supply Chain Management, and Project Operations — into Dataverse, configured at the table level so you choose which tables to sync.[LG p.69]

- **No specific license is required to enable dual write**, and no additional licensing is required to configure dual write against **unrestricted** tables.[LG p.69]
- When dual write is configured against a **restricted** table, users who make updates in Dynamics 365 that result in updates to those restricted tables must be appropriately licensed. For example, Finance users leveraging dual write to integrate the Invoice Process (a restricted Dataverse table) need appropriate licenses.[LG p.69]

> **Dual-use rights vs. dual write:** Dual-use rights are a *deployment* right (cloud license also covers equivalent on-premises access, no extra CAL). Dual write is a *data-integration* feature (syncing finance and operations tables into Dataverse). They are unrelated despite the similar names.[LG pp.68-69]

### Extensibility

Dynamics 365 extensibility is provided through **Power Platform**; the available functionality is detailed in the Power Platform Licensing Guide.[LG p.69] Some Dynamics 365 apps **embed Power BI** content (tables and charts) — this is a product feature and needs no Power BI license to view, but customizing the content requires a Power BI Pro or Power BI Premium per-user license; Dynamics 365 users get no standalone Power BI license.[LG pp.69-70] For applicable products, Dynamics 365 licenses also include the right to use custom tables (Appendix D) and to create custom security roles (Appendix F).[LG p.70]

### Field Service integrations

- **Field Service + Finance/Supply Chain Management:** This out-of-the-box integration lets Field Service-licensed users be assigned a security role in Finance and Supply Chain Management; work orders sync to projects and project journals, and Field Service reads inventory via virtual tables (Finance/SCM is the system of record). Integration is available to organizations licensed for D365 Field Service, D365 Finance, and D365 Supply Chain Management. **Direct access** to the Finance or Supply Chain Management application still requires a license.[LG p.70]
- **Field Service + Project Operations (Modern Project Operations):** This integration lets Field Service-licensed users transact against projects, aligning field service with project operations and finance and operations apps. It uses the Modern Project Operations integration to sync Field Service transactions to finance and operations. It does **not** license customers to use Project Operations functionality without a proper license (beyond the Microsoft-built data alignment). **Direct access** to Project Operations, Finance, or Supply Chain Management requires licenses.[LG p.70]

## Appendix G: Operations – Activity approval privileges

Enterprise product licenses include Operations – Activity use rights, and those rights cross applications. For the specific approval privileges below, the guide indicates whether an **Enterprise** or an **Operations – Activity** license is required. A user who needs to approve budget account entry through workflow needs only an Operations – Activity license; a user who also needs to approve a fixed assets journal needs an Enterprise license, which covers both tasks.[LG p.83]

The full table lists dozens of duty/privilege pairs. Most approval privileges require an **Enterprise** license, while a smaller set require only **Operations – Activity**. Examples:[LG pp.83-84]

| Duty | Privilege | License |
|---|---|---|
| Approve budget register entries | Approve budget account entry through workflow | Activity |
| Approve purchase agreement | Approve the purchase agreement through workflow | Activity |
| Maintain purchase order | Maintain purchase order | Activity |
| Maintain catalogs | Review and approve vendor catalogs | Activity |
| Maintain commitment documents | Approve commitment documents through workflow | Activity |
| Retail catalog approval workflow duty | Retail catalog approval workflow privilege | Activity |
| Approve customer invoices | Approve free text invoices | Enterprise |
| Approve vendor payment transactions | Approve vendor disbursement journal | Enterprise |
| Approve fixed assets transactions | Approve fixed assets journal | Enterprise |
| Approve ledger transactions | Approve ledger journal | Enterprise |
| Approve BOMs | Approve BOMs / Approve BOM versions | Enterprise |
| Approve routes | Approve routes / Approve route versions | Enterprise |

_Selected rows; these privileges apply when the relevant configuration key is on. See the guide for the complete list. Source: [LG pp.83-84]_

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.66 (Additional licensing requirements: minimum purchase, external users)
- Dynamics 365 Licensing Guide (July 2026), p.67 (External users, multiplexing)
- Dynamics 365 Licensing Guide (July 2026), p.68 (Multiplexing, dual-use rights)
- Dynamics 365 Licensing Guide (July 2026), p.69 (Dual-use rights, dual write, extensibility)
- Dynamics 365 Licensing Guide (July 2026), p.70 (Extensibility, Field Service integrations)
- Dynamics 365 Licensing Guide (July 2026), p.80 (Appendix F: security role assignment)
- Dynamics 365 Licensing Guide (July 2026), p.81 (Appendix F: customization licensing, highest-classification rule)
- Dynamics 365 Licensing Guide (July 2026), p.82 (Appendix F: multiple roles, changing securable objects)
- Dynamics 365 Licensing Guide (July 2026), pp.83-84 (Appendix G: Operations – Activity approval privileges)
- [Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [User security governance overview](https://learn.microsoft.com/dynamics365/fin-ops-core/fin-ops/sysadmin/security-gov-overview)
- [Prepare for finance and operations apps user license validation](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/prepare-for-user-validation)
- [Expired subscriptions and data deletion](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/expired-subscription-data-deletion)

---
[⬅ Back to Index](./Index.md)
