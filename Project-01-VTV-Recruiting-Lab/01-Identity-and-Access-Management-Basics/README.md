Identity and Access Management (IAM) Basics

 What is IAM?

Identity and Access Management (IAM) is how organizations control who can access resources, what they can access, and how that access is protected.

Key IAM Concepts

Identity
An identity represents a user, device, or application that needs access.

Examples:
- Employee
- Contractor
- Service account

Authentication
Authentication proves who someone is.

Examples:
- Password
- Multi-Factor Authentication (MFA)

Authorization
Authorization determines what a user is allowed to access.

Example:
A finance employee can access finance files but should not access HR records.

Least Privilege

Users should only receive the access needed to perform their job.

Microsoft Entra ID

Microsoft Entra ID is Microsoft's cloud identity and access management service used to manage:
- Users
- Groups
- Applications
- Authentication
- Access policies

What I Learned

I learned the foundations of IAM and how identity security helps organizations protect resources.


 Project Scenario

VTV Recruiting is a growing organization that needs a secure way to manage employee identities and access to company resources.

As an IAM Analyst, my responsibility is to help manage:

- User accounts
- Group memberships
- Access permissions
- Authentication methods
- Security policies

 Business Problem

The organization needs to make sure:

- Employees have the correct access
- Users do not have unnecessary permissions
- Sensitive information is protected
- Access is removed when employees leave

 IAM Solution Approach

I will use Microsoft Entra ID concepts to design:

- Users
- Groups
- Roles
- Authentication policies
- Access controls


Hands-On IAM Scenario

Ticket #002 - Recruiter Access Provisioning

User: Kre Atkins  
Department:Recruiting  
Request: Add the user to the Recruiters group to provide access required for the Recruiting role.  
Approval: Manager approved

My Decision

I verified that the request was approved and that Kre Atkins was assigned to the Recruiting department. Based on his job role, I determined that membership in the Recruiters group was appropriate. I followed the principle of least privilege by granting only the group access required for his assigned role and not assigning additional administrative permissions.

I would verify any Microsoft 365 licensing requirements separately rather than assuming the user requires the same license as other members of the group.

Actions Taken

1. Opened Microsoft Entra ID.
2. Navigated to Groups, Recruiters, Members.
3. Reviewed the existing Recruiters group membership.
4. Selected Add members.
5. Located and selected Kre Atkins.
6. Added Kre Atkins to the Recruiters group.
7. Verified that Kre appeared as an active member of the group.

IAM Concepts Demonstrated

Identity and Access Management (IAM)
User provisioning
Group-based access
Role-Based Access Control (RBAC)
Least privilege
Authorization
Access verification

Result

Kre Atkins was successfully added to the Recruiters group and received the access associated with his approved Recruiting role.
Results:

Evidence

The screenshot below verifies that Kre Atkins was successfully added to the Recruiters group in Microsoft Entra ID.

![Recruiters Group Access Provisioning](Screenshot%202026-08-11%201.09.29%20PM.png)


## Hands-On IAM Scenario

### Ticket #003 - Department Transfer & Access Modification

**User:** Randy Kumah  
**Previous Department:** Finance  
**New Department:** Recruiting  
**Request:** Update the user's access after an approved transfer from Finance to Recruiting.  
**Approval:** Manager approved

### My Decision

I determined that Randy's existing Finance access should be removed because it was no longer required for his new role. Keeping unnecessary Finance access could cause privilege creep and violate the principle of least privilege.

I removed Randy from the Finance group and added him to the Recruiters group so his access matched his new job responsibilities.

### Actions Taken

1. Verified Randy's existing membership in the Finance group.
2. Confirmed the department transfer was approved.
3. Removed Randy from the Finance group.
4. Verified Randy was no longer a Finance group member.
5. Added Randy to the Recruiters group.
6. Verified Randy appeared in the Recruiters group.
7. Reviewed Microsoft Entra audit logs to confirm the group membership changes were completed successfully.

### IAM Concepts Demonstrated

- Identity lifecycle management
- Access provisioning
- Access deprovisioning
- Group-based access management
- Least privilege
- Prevention of privilege creep
- Authorization
- Audit logging and verification

### Evidence - Before Access Change

Randy was originally a member of the Finance group.

![Randy Finance Membership Before Transfer](Screenshot%202026-08-11%202.54.42%20PM.png)

### Evidence - New Role Access

After removing the outdated Finance access, Randy was added to the Recruiters group.

![Randy Recruiters Membership After Transfer](Screenshot%202026-08-11%203.03.38%20PM.png)

### Evidence - Audit Verification

Microsoft Entra audit logs confirmed that the removal from the previous group completed successfully.

![Successful Group Removal Audit Log](Screenshot%202026-08-11%204.11.51%20PM.png)

### Result

Randy's access was successfully updated to reflect his department transfer. His outdated Finance group membership was removed and his new Recruiting group membership was provisioned. The changes were verified through Microsoft Entra group membership and audit logs.
