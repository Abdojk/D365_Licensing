# Dynamics 365 Human Resources Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Human Resources helps organizations optimize compensation, benefits, leave and absence tracking, regulatory and policy compliance, performance feedback, standardized training, and self-service programs. It uses Dataverse and Power Platform to centralize people data and extend the solution, and it is **licensed per user**.[LG p.38] Refer to the Microsoft Product Terms for minimum purchase requirements.[LG p.38]

## The Human Resources full user license

HR professionals are typically licensed as **full-access users** with the Human Resources license.[LG p.38] The full-access license covers the HR-department roles — compensation and benefits manager, HR manager, payroll administrator/manager, recruiter, training manager, benefits management roles, and so on — that the security-role table marks as requiring the Human Resources license.[LG p.38][LG p.39]

Users **outside** the HR organization who only need self-serve access may instead be licensed through the **Team Members** license, the **Human Resources Self Service** license, or the **Operations – Activity** user license.[LG p.38]

## The Human Resources Self Service license

The Human Resources Self Service license enables employee and manager **self-serve** capabilities, such as:[LG p.38]

- Update personal employee information
- Manage the HR activities of direct employees or those reporting up through the user's reporting chain
- Report sick leave
- Submit vacation requests
- View employee benefits
- Approve employee leave as a manager
- View employee information as a manager

Two important limits define this license:[LG p.38]

- It grants access **only to Human Resources** — not to any other Dynamics 365 product.
- It does **not** include full user rights for Human Resources; it provides access to the functionality employees commonly need to manage themselves.

In the security-role table, the self-service roles — self-service contractor, self-service employee, pending worker, self-service manager, and leave and absence manager — are available at the **HR Self Service** level (and also to Team Members and Operations – Activity), whereas the HR-department roles require the full Human Resources license.[LG p.38][LG p.39] Microsoft Learn confirms the HR Self Service license as a valid entitlement to install and access HR apps: for example, the leave-and-absence app requires either a Dynamics 365 Human Resources or a Human Resources Self Service license, and the Recruiting solution requires at least the Human Resources Self Service license.[Learn: HR app for leave and absence](https://learn.microsoft.com/dynamics365/human-resources/hr-app) [Learn: HR recruiting app licensing overview](https://learn.microsoft.com/dynamics365/human-resources/recruit-license)

## Base and Attach eligibility

Human Resources is a **full-access user license** and participates in Dynamics 365 **Base and Attach** licensing.[LG p.6] When a user is licensed for multiple Dynamics 365 applications, the first (base) license must be the **highest-priced** license for that named user; additional qualifying applications may be added as lower-priced **attach** licenses, which can only be assigned to a user who already holds an appropriate qualifying base license.[LG p.6] Follow **base-then-attach sequencing** when assigning.[Learn: Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement) See the guide's base/attach table for the current qualifying combinations.[LG p.6]

Note that the **Human Resources Self Service** license is an **additional-user** license, not a full-access base license, and is categorized alongside Team Members as one of the lighter licensing options for employees who need self-serve access.[LG p.5][LG p.38]

## Team Members relevance

The **Team Members** license — a named-user license granting read-only access to Dynamics 365 data plus basic capabilities for designated scenarios — is one of the options for employees outside the HR organization.[LG p.5][LG p.38] In the HR security-role table, the self-service roles (contractor, employee, pending worker, manager, leave and absence manager) are available at the Team Members level as well as at the HR Self Service and Operations – Activity levels.[LG p.38] Choose between Team Members, HR Self Service, and Operations – Activity based on exactly which self-serve tasks a given employee or manager needs to perform.

## Included capacity and entitlements

Licensing Human Resources automatically entitles the tenant to **2,000 Customer Voice responses per tenant/month**, along with the following default capacity:[LG p.38][LG p.40]

| Entitlement | Human Resources |
| --- | --- |
| Customer Voice | 2K responses per tenant/month |
| Dataverse or Operations Database | 90 GB (+1 GB accrued/USL) |
| Dataverse or Operations File | 80 GB (+2 GB accrued/USL) |
| Dataverse Log | 2 GB |
| Environments | 2 Dataverse + 2 AOS |

Source: Dynamics 365 Human Resources Entitlements table.[LG p.40] Additional capacity and environments are available for purchase.[LG p.40] Of the two environments, only one may be in production at any given time, though both may be non-production simultaneously.[LG p.40]

> **Pricing:** Per-user prices change and are not reproduced here. See the official [Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview) for current Human Resources pricing.

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.5
- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.38
- Dynamics 365 Licensing Guide (July 2026), p.39
- Dynamics 365 Licensing Guide (July 2026), p.40
- [Microsoft Learn — Dynamics 365 Human Resources app for leave and absence](https://learn.microsoft.com/dynamics365/human-resources/hr-app)
- [Microsoft Learn — HR recruiting app licensing overview](https://learn.microsoft.com/dynamics365/human-resources/recruit-license)
- [Microsoft Learn — Stay compliant with user licensing requirements](https://learn.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/stay-compliant-user-license-requirement)
- [Microsoft — Dynamics 365 pricing overview](https://www.microsoft.com/dynamics-365/pricing-overview)

---
[⬅ Back to Index](./Index.md)
