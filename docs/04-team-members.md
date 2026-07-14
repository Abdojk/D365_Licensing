# Dynamics 365 Team Members License

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

The **Dynamics 365 Team Members** license is a low-cost, limited-use license for light, mostly read-only line-of-business users. This page covers who it is for, what it can and cannot do, the designated Team Member apps, the pre-approved use-right scenarios from Appendix D, and the separate **Business Central Team Members** license.

## Who it is for

Team Members is one of the **additional user** licenses. Additional users often represent a large percentage of an organization's total users: they may consume data or reports from line-of-business systems, complete light tasks like time or expense entry and HR record updates, or use the system without needing full-access capabilities.[LG p.6]

The Team Members license specifically is intended for users who **support multiple lines of business and are not tied to a specific business unit**. Licensed users are granted **read-only access to all Dynamics 365 data** and **basic Dynamics 365 capabilities for designated scenarios**, such as expense entry or updating contacts.[LG p.7] Microsoft Learn describes it as a license for users "whose jobs aren't necessarily tied to a function but who still need to use the basic functionality of a line-of-business system," giving lightweight access through **designated scenarios** built into the Team Member experience.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

## Named-user model

Team Members is a **named user subscription** — it is assigned to an individual user with personal login credentials, who can then access the licensed functionality from any device.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license) As with all named-user licenses, the rights are for that user's **own use** and **not** for activities performed for, or on behalf of, other people. For instance, the license does not grant managers the right to perform the same actions for their direct reports (except for the limited HR manager scenarios noted below).[LG p.60]

## Designated Team Member apps

For the customer engagement apps (Sales, Customer Service, Field Service, and Project Operations), the Team Member experience is delivered through a fixed set of **designated apps** rather than the full application:[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

- **Customer Service Team Member**
- **Sales Team Member**
- **Project Resource Hub** (Project Operations)

The licensing guide grants the Team Members rights through the **Customer Service Team Members, Sales Team Members, and Project Operations Team Members** application modules.[LG p.59]

A user with only a Team Members license sees only the Team Member app (for example, the **Customer Service Team Member** app), not the full hub (e.g. Customer Service Hub or Sales Hub). If such a user tries to reach an app they aren't entitled to — through a bookmark or shared link — they receive an "Invalid License" error once enforcement is applied.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

### What each designated app does

- **Customer Service Team Member** — create, read, and update your **own** cases; use the comments feature to interact with service representatives; and search and view knowledge base articles.[Learn: Customer Service Team Member app](https://learn.microsoft.com/dynamics365/customer-service/customer-service-team-member)
- **Sales Team Member** — customer management (work with contacts or see accounts); lead and opportunity management (see leads/opportunities linked with accounts or contacts); and add notes and activities such as tasks. Administrators can configure the app for additional scenarios, but **not beyond** those listed in the licensing guide.[Learn: Sales Team Member app](https://learn.microsoft.com/dynamics365/sales-enterprise/sales-team-member)

## What Team Members can do

The guide lists the rights granted through the license across two platforms. All rights are for the user's **own use**.[LG p.59][LG p.60]

**Through the Sales / Customer Service / Project Operations Team Member modules (Dataverse platform):**[LG p.59][LG p.60]

- Create, read, update, and delete **contacts, activities, and notes**
- Update their **own** employee information
- Record time, materials, and expenses
- Approve time, expenses, materials, and vendor invoices
- Use reporting and dashboards
- Participate as a **consumer** of Dynamics 365 services, such as responding to surveys

**Additional rights for Finance, Supply Chain, Commerce, Human Resources, and Project Operations (finance and operations platform)** — for the user's own use, or for limited HR use by managers:[LG p.60]

- Record any type of time or expense
- Approve time, expenses, and vendor invoices
- Create requisitions
- Create or edit items related to **quality control** and **departmental budgets**
- Manage their own employee information
- Manage human resources activities for direct employees or those reporting up through the user's reporting chain
- Use Human Resources Self Service functionality (when Human Resources is licensed by the organization)

### Customization limit: 15 tables

A Team Members license holder may customize a **maximum of 15 additional tables** (custom tables or standard Dataverse tables) available to licensed users, per the pre-approved scenarios in the guide's appendices.[LG p.60] Microsoft Learn states the same limit as a maximum of **15 entities** per Team Member app.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

## What Team Members cannot do

- **No custom apps beyond the designated scenarios.** The Team Members subscription does **not** provide access to custom applications and isn't intended for scenarios beyond those listed in the licensing guide.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license) Once enforcement is applied for an environment, Team Member users can only access the designated Team Member applications.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)
- **Not for acting on behalf of others.** Rights are for the user's own use, not for performing actions for other people (with the limited HR manager exception).[LG p.60]
- **Read-only for most data** beyond the pre-approved create/update scenarios.[LG p.7]

If a user needs a **custom app**, the appropriate license is a **Power Apps** per-app or per-user license.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license) If a user needs to access or update Dynamics 365 data **beyond** the Team Member use rights (for example, frequent edits to the Case entity outside self-service), Microsoft recommends assigning the appropriate full license, such as **Dynamics 365 Customer Service Enterprise**.[Learn: Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)

## Appendix D: Team Members use-rights overview

Appendix D of the guide summarizes the use rights granted through a Dynamics 365 Team Members license (⚫ = included). It is split across two platforms: the **Dataverse platform** (with Sales, Customer Service, Field Service, Project Operations) and the **Finance and Operations platform** (with Finance, SCM, Commerce, HR, Project Operations). **Appendix D does not apply to Business Central Team Members.**[LG p.76]

### Access, read, and general system use

| Use right | Dataverse platform | F&O platform |
|---|---|---|
| Access anywhere: Web, Mobile, Tablet, Dynamics 365 App for Outlook | ⚫ | |
| Full read across Dynamics 365 applications | ⚫ | ⚫ |
| Activities: create, update, delete | ⚫ | |
| Announcements: create, update, delete | ⚫ | |
| Contacts: create, update, delete | ⚫ | |
| Dynamics 365 mobile client (iPad, Windows) except Field Service | ⚫ | |
| Microsoft Excel: export data, access user reports/charts/dashboards | ⚫ | |
| Notes: create, update, delete | ⚫ | |
| Yammer collaboration (needs Yammer license) | ⚫ | |
| Customization: additional tables (custom or standard Dataverse), 15 per app | ⚫ | |

*Source: [LG p.76]*

### Pre-approved application scenarios

| Scenario | Dataverse platform | F&O platform |
|---|---|---|
| **General** — Employee self-serve | | ⚫ |
| **General** — Manager: review team data, light actions (approve time, expenses, leave) | | ⚫ |
| **General** — Purchase requisitions: create, edit, approve | | ⚫ |
| **General** — Contractor: worker in contractor relationship with legal entities | | ⚫ |
| **Sales** — Employee self-serve: contacts/read accounts; read leads & opportunities linked with accounts (via Sales for Team Members, Power Pages, or API) | ⚫ | |
| **Customer Service** — Employee self-serve: create/update/delete own case; read knowledge articles (via Customer Service for Team Members, Power Pages, or API) | ⚫ | |
| **Field Service** — Work orders: create/update/delete for self-serve; internal create on behalf of customers (cannot resolve/close) | ⚫ | |

*Source: [LG p.76]*

### Finance, Supply Chain, Commerce, and HR scenarios (F&O platform)

| Area | Approved actions |
|---|---|
| **Finance** | View positive pay events; monitor assigned cost objects; create/edit department budget; employee self-serve (personal info, time & expense); approve vendor invoices; respond to inventory needs; manager self-serve; respond to/approve POs (when listed as contact); approve time and expense[LG p.77] |
| **Supply Chain Management** | Employee self-serve; create maintenance requests; approve time & attendance; monitor cost objects; confirm shipments/receipts and update delivery status; view BOM/product details; respond to production-line inventory needs; approve purchase orders; quality control create/edit/update; edit sales order (custom security role); monitor transportation[LG p.77] |
| **Commerce** | Employee self-serve; approve expense; approve invoice; manager self-serve; picking, receiving, stock counting in store/warehouse; approve time[LG p.77][LG p.78] |
| **Human Resources** | Approve absence and leave; employee self-serve (personal info, request leave/absence); manager self-serve (manage direct reports, record/update employee info)[LG p.78] |
| **Project Operations** | Approve time/expense/material usage; create and submit time, expense, and material usage entries; access assigned work for current/future periods; approve purchase order/request and project timesheet[LG p.78] |

*Note: the Project Operations Team Members app provides Dataverse capabilities only when Project Operations is installed in Dataverse; the sales-order edit right requires a custom security role.[LG p.78]*

## Business Central Team Members (separate license)

The **Dynamics 365 Business Central Team Members** license is **not to be confused** with the Dynamics 365 Team Members license, and it is **not** covered by Appendix D.[LG p.59][LG p.76] It is assigned to a named user and provides **read-only access to certain data and limited functionality** within Business Central deployments.[LG p.6]

It grants the named user the following rights, **for their own use only** (not for or on behalf of others):[LG p.59]

- Read data within Business Central
- Update **existing** data and entries (e.g. previously created customer, vendor, or item records; entries are specific accounting information such as a due date on customer ledger entries)
- Approve or reject tasks in all workflows assigned to that user (approvals/rejections can only update data in records the license can access)
- Create, edit, and delete a **sales or purchase quote**
- Create, edit, and delete **personal** information
- Edit **job time sheets** for approval
- Use the Power Apps / Power Automate use rights provided with a Dynamics 365 license
- Customize the Business Central Team Members application module with a **maximum of 15 additional tables** (custom or standard Dataverse tables)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.6
- Dynamics 365 Licensing Guide (July 2026), p.7
- Dynamics 365 Licensing Guide (July 2026), p.59
- Dynamics 365 Licensing Guide (July 2026), p.60
- Dynamics 365 Licensing Guide (July 2026), p.76
- Dynamics 365 Licensing Guide (July 2026), p.77
- Dynamics 365 Licensing Guide (July 2026), p.78
- [Microsoft Learn — Dynamics 365 Team Members license](https://learn.microsoft.com/dynamics365/get-started/team-members-license)
- [Microsoft Learn — Customer Service Team Member app](https://learn.microsoft.com/dynamics365/customer-service/customer-service-team-member)
- [Microsoft Learn — Sales Team Member app](https://learn.microsoft.com/dynamics365/sales-enterprise/sales-team-member)

---
[⬅ Back to Index](./Index.md)
