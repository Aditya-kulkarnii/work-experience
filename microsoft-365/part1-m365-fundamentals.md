# Microsoft 365 — Part 1: Fundamentals and Products

## What is Microsoft 365?
Microsoft 365 (formerly Office 365) is Microsoft's
cloud-based subscription service that bundles productivity
apps, cloud storage, and enterprise security tools into
one platform.

Used by millions of organizations worldwide as their
complete workplace productivity and communication platform.

---

## Core M365 Products

### Microsoft Word
Document creation and editing. Cloud-saved via OneDrive.
Real work use: client reports, proposals, documentation.

### Microsoft Excel
Spreadsheet and data analysis tool.
Real work use: license tracking, client asset inventories.

### Microsoft PowerPoint
Presentation creation tool.
Real work use: client proposals, training materials.

### Microsoft Outlook
Email client and calendar management.
Enterprise use: connected to Exchange Online for
centralized email management, shared mailboxes,
and mail flow rule enforcement.

### Microsoft Teams
Communication and collaboration platform — chat,
video calls, file sharing, and app integrations.
Architecture: built on SharePoint (file storage),
Exchange (calendar/email), and Azure AD (identity).

### Microsoft OneDrive
Personal cloud storage — 1TB per user in most plans.
Files sync between devices and are accessible anywhere.

### Microsoft SharePoint
Team and department file storage and intranet platform.
Architecture: Site Collections → Sites → Libraries → Files
Permissions: inherited by default, can be broken at any level.

---

## What is Microsoft Azure?
Microsoft's cloud computing platform — provides
virtual machines, databases, networking, AI services,
and security tools as cloud services.

Key difference:
- Microsoft 365 = productivity and collaboration tools
- Microsoft Azure = infrastructure and cloud services

---

## Microsoft Licensing

### Types of M365 Business Plans
For organizations under 300 users:
- Microsoft 365 Business Basic
- Microsoft 365 Business Standard
- Microsoft 365 Business Premium (includes Defender)

### Types of M365 Enterprise Plans
For large organizations, no user limit:
- Microsoft 365 E3 — core productivity + security
- Microsoft 365 E5 — full security suite including
  Defender, Purview, and advanced compliance tools

### CSP — Cloud Solution Provider
Partners like Intime Solutions who resell Microsoft
licenses to clients. CSP partners manage billing,
support, and licensing on behalf of clients.

### Licensing Models
- **Perpetual License** — one-time purchase, own forever,
  no automatic updates. Example: Office 2019.
- **Subscription License** — monthly/annual payment,
  always latest version. Example: Microsoft 365.
- **EA — Enterprise Agreement** — volume licensing for
  large enterprises, 3-year commitment, discounted pricing.
- **MPSA** — Microsoft Products and Services Agreement,
  flexible volume licensing without fixed terms.
- **NCE — New Commerce Experience** — Microsoft's current
  licensing model, annual or monthly subscriptions through
  CSP partners.

---

## Key Microsoft Services

### Microsoft Intune — Device Management
MDM (Mobile Device Management) and MAM (Mobile App
Management) solution. Controls what devices can access
company resources and enforces security policies on
endpoints — phones, laptops, tablets.

### Microsoft Defender — Security
Built-in security across M365:
- Defender for Endpoint — EDR for Windows devices
- Defender for Office 365 — email and collaboration security
- Defender for Identity — AD attack detection
- Defender for Cloud Apps — CASB solution
Included in M365 E5. Defender for Endpoint included in
Business Premium.

### Microsoft Power Platform
Low-code tools: Power BI (analytics), Power Apps
(app building), Power Automate (workflow automation).

### Microsoft Dynamics 365
Business operations platform — CRM, ERP, sales,
customer service, and field service management.

---

## Microsoft Tenant
A dedicated instance of Microsoft's cloud services
for one organization. Every organization that signs
up for M365 or Azure gets their own tenant.
Identified by: companyname.onmicrosoft.com

## Microsoft Admin Center
Web portal at admin.microsoft.com where IT admins
manage users, licenses, groups, and services for
their organization's M365 tenant.

## Identity and Access Management (IAM)
Managing who has access to what in the M365 environment.
Includes: user creation, license assignment, role
assignment, MFA enforcement, and conditional access policies.

---

## Email Authentication — SPF, DKIM, DMARC

### SPF — Sender Policy Framework
A DNS TXT record that specifies which mail servers
are authorized to send email on behalf of a domain.
Prevents other servers from spoofing your domain.

### DKIM — DomainKeys Identified Mail
Adds a cryptographic digital signature to outgoing emails.
The receiving server verifies the signature to confirm
the email genuinely came from the stated domain and
was not modified in transit.

### DMARC — Domain-based Message Authentication
Reporting and Conformance
Policy that tells receiving servers what to do when
SPF or DKIM checks fail — quarantine or reject the email.
Also sends reports back to the domain owner about
who is sending email using their domain.

Together SPF + DKIM + DMARC form the complete email
authentication stack. Without all three, a domain
is vulnerable to email spoofing and phishing attacks
that impersonate the organization.

---
*Microsoft 365 Part 1 of 3*

*Role: Technical Associate @ Intime Solutions, Bangalore*
