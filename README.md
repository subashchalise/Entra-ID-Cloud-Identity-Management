# Entra ID Tier 1 Help Desk Administration

## Project Overview
This project simulates a real-world enterprise cloud IT environment, focusing on Identity and Access Management (IAM) within Microsoft Entra ID and the Microsoft 365 Admin Center. Building upon foundational Active Directory lifecycle concepts, this project demonstrates practical cloud administration and aligns with the core identity objectives of the MS-900 (Microsoft 365 Fundamentals) certification.

---

## Phase 1: Identity Lifecycle & User Onboarding

**Objective:** To provision cloud-only identities, configure organizational metadata, apply appropriate licenses, and securely delegate administrative roles.

### 1. User Provisioning & Metadata Management
To establish the organization's foundation, I created multiple cloud-only users divided into distinct departments (IT, HR, Production, Packaging, and Inventory). 

Beyond simply creating the accounts, I ensured each user profile was fully populated with realistic enterprise metadata. This included assigning Employee IDs, physical office locations, job titles, and establishing reporting structures (assigning Managers). Clean data management at this stage is critical for future automation, such as dynamic group memberships.

> **Proof of Execution:** Successfully provisioned a multi-departmental directory, mapping key attributes like Department and Job Title to ensure clean Identity and Access Management (IAM).
> ![All Users Dashboard](images/1a.png)
>


> **Proof of Execution:** A fully realized user profile demonstrating enterprise-level attention to detail, including reporting structures (Manager assigned) and corporate contact information.
> ![All Users Dashboard](images/1b.png)

### 2. Resource Provisioning & Licensing
Once the identities were created, the next step was granting them the tools necessary to perform their jobs. For this simulation, I navigated to the Microsoft 365 Admin Center to assign licenses to the Junior Helpdesk user.

I applied two specific licenses:
* **Microsoft 365 Business Basic:** To provide an Exchange mailbox for support tickets and Teams for communication.
* **Entra ID Premium P1:** To unlock enterprise security features required for later phases, such as Conditional Access and dynamic grouping.

> **Proof of Execution:** Successfully navigated the M365 Admin Center to provision productivity applications and advanced security licenses to an end-user.
> ![All Users Dashboard](images/1c.png)

### 3. Role-Based Access Control (RBAC)
To maintain a secure environment, it is crucial to follow the **Principle of Least Privilege**. Rather than giving the Junior Helpdesk employee full Global Administrator rights, I assigned a specialized built-in role. 

I granted the **Helpdesk Administrator** role. This securely delegates the ability to reset user passwords and troubleshoot sign-in issues without giving the account the power to alter global tenant security settings or delete accounts.

> **Proof of Execution:** Demonstrated understanding of RBAC by securely delegating the Helpdesk Administrator role, ensuring the user has exactly the access needed for their job and nothing more.
> ![All Users Dashboard](images/1d.png)

---
## Phase 2: Group Management & Delegation

**Objective:** To organize identities for scalable management, demonstrating both manual administrative delegation and automated dynamic memberships to reduce Tier 1 support overhead.

### 1. Manual Security Groups & Delegation
In enterprise environments, access is granted to groups, not individuals. I established a standard Security Group for the Production department (`PRD-Production-Team`). 

To alleviate basic ticket volume from the IT Help Desk, I applied the principle of delegation by assigning the Production Manager as the "Owner" of this group. This empowers the department head to manage their own team's membership without requiring Global Admin intervention.

> **Proof of Execution:** Created a departmental security group and successfully delegated ownership to a non-IT manager.
> > ![All Users Dashboard](images/2a.png)

### 2. Dynamic Group Automation
To demonstrate advanced identity automation, I utilized my Entra ID Premium P1 license to configure a Dynamic Security Group for the Human Resources department (`HR-Human-Resources-Team`). 

Instead of relying on manual additions during onboarding, I built a membership query that automatically evaluates user metadata. If a user's `Department` attribute is set to "Human Resources," they are instantly added to the group. This eliminates human error and guarantees secure, instant access provisioning.

> **Proof of Execution:** Successfully configured a dynamic membership query `(user.department -eq "Human Resources")` to automate group assignments based on user attributes.
> > ![All Users Dashboard](images/2b.png)

---
*Author: Subash Chalise | IT Support Professional*
