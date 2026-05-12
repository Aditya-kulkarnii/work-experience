# Microsoft 365 — Part 2: Hybrid Environment and Authentication

## What is a Hybrid Environment?

Most large enterprises do not move everything to the cloud
at once. They run a hybrid environment — some systems
on-premises, some in the cloud, both connected and
synchronized.

### Components of a Hybrid Environment

**On-Premises Active Directory (On-Prem AD)**
Traditional AD running on servers inside the
organization's own data center. Manages users,
computers, and policies locally.

**Azure Active Directory / Microsoft Entra ID**
Microsoft's cloud-based identity platform.
Manages authentication for cloud services like
M365, Azure, and third-party SaaS apps.
Note: Microsoft rebranded Azure AD to Entra ID in 2023.

**Hybrid Identity**
Synchronizing on-prem AD users to Azure AD so that
one set of credentials works for both on-prem resources
and cloud services. Users log in once and access everything.

---

## Types of Hybrid Authentication

### 1. Password Hash Sync (PHS)
The most common and simplest hybrid authentication method.
A hash of the user's password is synchronized from
on-prem AD to Azure AD.
Authentication happens in the cloud directly.
Works even if the on-prem infrastructure goes down.
Recommended for most organizations.

### 2. Pass-through Authentication (PTA)
User credentials are validated against on-prem AD
in real time — the password hash never goes to the cloud.
Requires on-prem infrastructure to be running for
authentication to work.
Used when organizations have compliance requirements
that prevent storing credentials in the cloud.

### 3. Federation (ADFS)
Active Directory Federation Services — on-prem
server that handles all authentication.
Azure AD redirects login requests to ADFS.
Most complex setup, highest maintenance overhead.
Being phased out in favor of PHS and PTA.

---

## Microsoft Entra ID (Azure AD)

### RBAC — Role Based Access Control
Assigns permissions based on roles, not individuals.
Built-in roles: Global Administrator, User Administrator,
Security Administrator, Exchange Administrator, etc.
Best practice: assign least privileged role needed.
Never use Global Admin for day-to-day tasks.

### Privileged Identity Management (PIM)
Just-in-time privileged access. Instead of giving
someone permanent admin rights, PIM allows them to
activate admin roles only when needed — for a limited
time period. Automatically removes the role after.
Dramatically reduces risk from compromised admin accounts.

### Entra ID Protection (Identity Protection)
AI-driven risk detection for user sign-ins.
Detects: impossible travel, anonymous IP login,
leaked credentials, unfamiliar sign-in properties.
Can automatically block or require MFA for risky logins.

---

## Microsoft Groups

### Distribution List (DL)
Email-only group. Send one email to the group address
and it goes to all members. No M365 features beyond email.
Example: allstaff@company.com

### Security Group
Used to assign permissions to resources — SharePoint
sites, Teams, apps. Not email-enabled by default.
Example: Finance-Team-SharePoint-Access

### Mail-Enabled Security Group
Combination — can receive email AND be used for
permission assignment.

### Microsoft 365 Group (Modern Group)
Full collaboration group — creates a shared mailbox,
SharePoint site, Teams channel, OneNote notebook, and
Planner board automatically. The backbone of Teams.

---

## Exchange Online

### Shared Mailbox
A mailbox accessed by multiple users — no license
required for the mailbox itself (up to 50GB).
Used for: support@company.com, info@company.com
Multiple team members can read and respond from it.

### Mail Flow Rules (Transport Rules)
Server-side rules that act on all email passing through
Exchange Online — before it reaches the user's inbox.
Can: block certain file types, add disclaimers, encrypt
emails, redirect messages, reject based on content.

### Email Quarantine
Emails flagged as spam, phishing, or malware go to
quarantine instead of the inbox. Admins and users
can review and release legitimate emails from quarantine.

---

## Common Azure AD Error Codes

| Code | Meaning |
|------|---------|
| AADSTS50126 | Invalid username or password |
| AADSTS50076 | MFA required — user must complete MFA |
| AADSTS53003 | Blocked by Conditional Access policy |
| AADSTS50057 | Account is disabled |
| AADSTS700016 | Application not found in tenant |

These are the most common codes seen in real support
tickets. Knowing them instantly speeds up diagnosis.

---

## Support Ticket Lifecycle

Real end-to-end ticket handling process:

1. Client raises ticket
2. Ticket assigned to you (L1 support)
3. Acknowledge the client within SLA time
4. Gather information — error codes, screenshots, affected users
5. Diagnose — check sign-in logs, admin center, error codes
6. Fix or escalate to L2/L3 if beyond L1 scope
7. Confirm resolution with client
8. Document the issue and resolution
9. Close ticket

Sign-In Logs in Entra ID show every login attempt —
success, failure, location, device, and error code.
First place to look for any authentication issue.

---
*Microsoft 365 Part 2 of 3*

*Role: Technical Associate @ Intime Solutions, Bangalore*
