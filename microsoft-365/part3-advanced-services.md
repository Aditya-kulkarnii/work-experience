# Microsoft 365 — Part 3: Advanced Services and Compliance

## SharePoint Online

### SharePoint Architecture
Tenant → Site Collections → Sites → Libraries/Lists → Files

**Site Collection** — top level container, has its own
admin and storage quota.
**Site** — individual SharePoint site within a collection.
**Library** — document storage within a site.
**List** — structured data storage (like a database table).

### SharePoint Permissions
Three default permission levels:
- **Owner** — full control, can manage permissions
- **Member** — can edit and add content
- **Visitor** — read only

### Permission Inheritance
By default all subsites, libraries, and files inherit
permissions from the parent site.
Inheritance can be broken at any level to set unique
permissions — but this creates management complexity
and is a common source of accidental data exposure.

Security best practice: minimize permission inheritance
breaks, use groups instead of individual user permissions,
and audit SharePoint permissions regularly.

---

## Microsoft Teams

### Teams Architecture
Teams is built on top of three M365 services:
- **Azure AD** — identity and access
- **SharePoint** — file storage (each Team gets a SharePoint site)
- **Exchange** — calendar and meeting data

### Teams Policies
Control what users can and cannot do in Teams:
- **Meeting policies** — who can record, who can present
- **Messaging policies** — who can delete messages, use GIFs
- **App policies** — which apps are allowed in Teams
- **Calling policies** — who can make private calls

Policies are assigned per user or per group in
the Teams Admin Center.

---

## Microsoft 365 Compliance Center

### Microsoft Purview
Unified data governance and compliance platform.
Covers: data classification, information protection,
data lifecycle management, and compliance management.

### Retention Policies
Define how long content is kept and what happens
when the retention period ends — keep, delete, or
review before deleting.

Applied to: Exchange mailboxes, SharePoint sites,
OneDrive accounts, Teams messages.

Example: "Keep all emails for 7 years, then delete."
Required for regulatory compliance in many industries.

### Data Loss Prevention (DLP)
Policies that detect and prevent sharing of sensitive
information — credit card numbers, national ID numbers,
medical records — outside the organization.

DLP scans: emails, Teams messages, SharePoint files,
OneDrive files in real time.
Action on detection: block, warn user, or notify admin.

### eDiscovery
Legal tool to search, preserve, and export content
from M365 for legal investigations or compliance audits.

Content Search — find emails, files, Teams messages
matching specific criteria across the entire tenant.
Legal Hold — preserve content so it cannot be deleted
even if retention policies would normally remove it.

---

## Key Security Takeaways from M365

**1. Identity is the new perimeter**
In a cloud environment there is no traditional network
perimeter. Azure AD and Entra ID are the security
boundary. MFA, Conditional Access, and PIM are the
most critical controls.

**2. Admin roles must follow least privilege**
Never use Global Administrator for daily tasks.
Use PIM for just-in-time access to privileged roles.

**3. Email authentication is non-negotiable**
SPF, DKIM, and DMARC must all be configured correctly.
Missing any one of them leaves the domain vulnerable
to spoofing and phishing attacks.

**4. DLP protects the data itself**
Even if an attacker gets inside, DLP policies can
prevent sensitive data from leaving the organization.

**5. Audit logs are everything**
Sign-in logs, audit logs, and DLP reports are the
evidence trail for every security investigation.
Without logs — there is no forensics.

---
*Microsoft 365 Part 3 of 3 — Complete*

*Role: Technical Associate @ Intime Solutions, Bangalore*
