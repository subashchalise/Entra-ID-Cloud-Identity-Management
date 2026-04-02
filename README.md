# Cloud Identity & Access Management (IAM) with Microsoft Entra ID

## 🏢 Project Overview
**Objective:** To design, configure, and administer a cloud-first Identity and Access Management (IAM) environment for a simulated manufacturing organization using Microsoft Entra ID. 

This project demonstrates practical enterprise IT support skills, including user lifecycle management, departmental group architecture, and the implementation of security best practices like the Principle of Least Privilege (PoLP).

**Environment & Technologies:** * Microsoft Entra ID (formerly Azure AD)
* Microsoft 365 Business Basic
* Role-Based Access Control (RBAC)

---

## 🛠️ Phase 1: User Provisioning & License Management
**Scenario:** The organization required cloud identities for employees distributed across Production, Packaging, Inventory, Human Resources, and IT departments. 

* **Action:** Provisioned structured, cloud-native user identities with standardized naming conventions.
* **Action:** Mapped organizational hierarchy by assigning exact job titles and department attributes to each identity.
* **Action:** Successfully deployed Microsoft 365 Business Basic licenses to active staff to enable cloud application access.

> **Visual Proof: Active Users & Licensing**
> *[Insert Image 1 (All Users pane) here]*

---

## 🗂️ Phase 2: Security Group Architecture
**Scenario:** To manage access, applications, and security policies efficiently at scale, users needed to be organized into role-specific containers rather than being managed individually.

* **Action:** Created Assigned Security Groups for major departments: `Production`, `Inventory`, `Packaging`, `HumanResources`, and `IT Help Desk`.
* **Action:** Populated the functional security groups with the respective departmental users to establish a foundation for bulk policy assignment.

> **Visual Proof: Security Group Creation**
> *[Insert Image 3 (All groups pane) here]*

> **Visual Proof: Group Membership (Inventory Department)**
> *[Insert Image 4 (Inventory group members: Elena & Marcus) here]*

---

## 🔐 Phase 3: Privilege Delegation (RBAC)
**Scenario:** A new Junior Helpdesk technician (John Carter) joined the IT team. He required the ability to reset employee passwords and manage basic credential issues without holding Global Administrator privileges.

* **Action:** Created a dedicated cloud identity for the incoming Junior IT Support technician.
* **Action:** Enforced the Principle of Least Privilege by utilizing the 'Assigned roles' directory to explicitly delegate only the **Helpdesk Administrator** role. 

> **Visual Proof: Role-Based Access Control Application**
> *[Insert Image 2 (John Carter Assigned Roles) here]*

---

## 🎫 Phase 4: Help Desk Operations & Auditing
*(This section covers daily administrative simulations, including access recovery, emergency offboarding, and directory auditing.)*

> **Visual Proof: Entra ID Audit Logs**
> *[Image coming soon]*
