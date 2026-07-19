# Entra ID User Lifecycle & RBAC

## Purpose
This lab demonstrates end-to-end new-hire provisioning in Microsoft Entra ID, following enterprise best practices: identity creation, group-based access, least-privilege RBAC, Self-Service Password Reset (SSPR), and account verification with audit review.

**[View Full Lab Documentation](Entra_ID_User_Lifecycle_RBAC.md)**

---

## Scenario
A new employee (James Whitfield, Marketing Coordinator) is starting Monday and requires a fully provisioned Microsoft 365 account before his first day — correct license, group access, and password self-service, verified and audit-logged.

---

## Prerequisites
- Microsoft 365 tenant with available licenses (ResolvePoint IT)
- Global Admin (or User Administrator) account
- Microsoft Entra ID and M365 Admin Center access

---

## Lab Tasks
1. **Create a new user** in Microsoft Entra ID with department and job title attributes.
2. **Assign a Microsoft 365 license** via the M365 Admin Center.
3. **Create a security group** (Marketing-Team) for scalable access management.
4. **Add the user to the group** to inherit department-level access.
5. **Assign an RBAC role** (Helpdesk Administrator) to a separate account, demonstrating least privilege.
6. **Configure Self-Service Password Reset (SSPR)** scoped to the group.
7. **Verify first login** and confirm the M365 app suite loads.
8. **Review the audit log** to confirm all provisioning actions succeeded.

---

## Screenshots Included
All screenshots are located in the `/screenshots` folder.

---

## Learning Outcomes
- End-to-end Microsoft 365 / Entra ID user lifecycle management.
- Application of RBAC and the Principle of Least Privilege.
- Group-based access and license management at scale.
- SSPR configuration as a proactive ticket-reduction measure.
- Verification and audit-log review as a standard part of provisioning.

---

## Skills Demonstrated
`Microsoft Entra ID` · `Microsoft 365 Administration` · `RBAC / Least Privilege` · `Group-Based Access` · `SSPR` · `User Lifecycle` · `Audit & Verification`
