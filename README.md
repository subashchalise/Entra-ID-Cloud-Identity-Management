# Entra ID Tier 1 Help Desk Administration

## Project Overview
This project simulates a real-world enterprise cloud IT environment, focusing on Identity and Access Management (IAM) within Microsoft Entra ID and the Microsoft 365 Admin Center. Building upon foundational Active Directory lifecycle concepts, this project demonstrates practical cloud administration and aligns with the core identity objectives of the MS-900 (Microsoft 365 Fundamentals) certification.

---

## Phase 1: Identity Lifecycle & User Onboarding

**Objective:** To provision cloud-only identities, configure organizational metadata, apply appropriate licenses, and securely delegate administrative roles.

### 1. User Provisioning & Metadata Management
To establish the organization's foundation, I created multiple cloud-only users divided into distinct departments (IT, HR, Production, Packaging, and Inventory). 

Beyond simply creating the accounts, I ensured each user profile was fully populated with realistic enterprise metadata. This included assigning Employee IDs, physical office locations, job titles, and establishing reporting structures (assigning Managers). Clean data management at this stage is critical for future automation, such as dynamic group memberships.

![All Users Dashboard](Screenshot-All-Users.png)
> **Proof of Execution:** Successfully provisioned a multi-departmental directory, mapping key attributes like Department and Job Title to ensure clean Identity and Access Management (IAM).

![User Properties Profile](Screenshot-User-Profile.png)
> **Proof of Execution:** A fully realized user profile demonstrating enterprise-level attention to detail, including reporting structures (Manager assigned) and corporate contact information.

### 2. Resource Provisioning & Licensing
Once the identities were created, the next step was granting them the tools necessary to perform their jobs. For this simulation, I navigated to the Microsoft 365 Admin Center to assign licenses to the Junior Helpdesk user.

I applied two specific licenses:
* **Microsoft 365 Business Basic:** To provide an Exchange mailbox for support tickets and Teams for communication.
* **Entra ID Premium P1:** To unlock enterprise security features required for later phases, such as Conditional Access and dynamic grouping.

![M365 License Assignment](Screenshot-License-Assignment.png)
> **Proof of Execution:** Successfully navigated the M365 Admin Center to provision productivity applications and advanced security licenses to an end-user.

### 3. Role-Based Access Control (RBAC)
To maintain a secure environment, it is crucial to follow the **Principle of Least Privilege**. Rather than giving the Junior Helpdesk employee full Global Administrator rights, I assigned a specialized built-in role. 

I granted the **Helpdesk Administrator** role. This securely delegates the ability to reset user passwords and troubleshoot sign-in issues without giving the account the power to alter global tenant security settings or delete accounts.

![RBAC Role Assignment](Screenshot-Role-Assignment.png)
> **Proof of Execution:** Demonstrated understanding of RBAC by securely delegating the Helpdesk Administrator role, ensuring the user has exactly the access needed for their job and nothing more.

---
*Author: Subash Chalise | IT Support Professional*
