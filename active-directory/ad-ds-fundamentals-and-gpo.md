# Active Directory — AD DS Fundamentals and GPO

## What is Active Directory?
Active Directory (AD) is Microsoft's directory service used
in enterprise environments to manage users, computers,
groups, and policies from a central location.

Every large organization uses Active Directory. It is the
backbone of Windows-based enterprise IT infrastructure.

---

## Where and Why It Is Used

Used in: enterprises, schools, hospitals, government
organizations — anywhere with multiple Windows computers
that need centralized management.

Why it matters for security:
- Central control of who can log in to what
- Enforces security policies across all machines
- Manages permissions and access at scale
- Single point of authentication for the entire organization

If Active Directory is compromised — the attacker owns
the entire organization. This is why AD attacks like
Pass-the-Hash, Kerberoasting, and DCSync are among the
most dangerous in enterprise cybersecurity.

---

## Key AD Concepts

### Domain
A logical grouping of network objects (users, computers,
printers) that share the same AD database.
Example: intime.local

### Domain Controller (DC)
The server that runs Active Directory and authenticates
users. Every domain needs at least one DC.
In my lab: DC01 (Windows Server)

### Organizational Unit (OU)
A container inside a domain used to organize objects
(users, computers, groups) and apply Group Policies to
specific sets of machines or users.

### LDAP
Lightweight Directory Access Protocol — the protocol
AD uses to communicate. Applications query AD using
LDAP to verify user credentials.

### Kerberos
The authentication protocol used by Active Directory.
When a user logs in, Kerberos issues tickets that
prove identity without sending passwords over the network.

Security relevance: Kerberoasting attack exploits
Kerberos by requesting service tickets and cracking
them offline to extract passwords.

---

## What I Did in the Lab

### Lab Environment Setup
- Created two VMs in VirtualBox:
  - DC01 — Windows Server 2019 (Domain Controller)
  - Client01 — Windows 10 (Domain-joined client)

### Step 1 — Deployed AD DS
Installed Active Directory Domain Services (AD DS)
role on DC01 through Server Manager.
Promoted the server to a Domain Controller.
Created a new forest and domain.

### Step 2 — Connected Server to Client
Joined Client01 to the domain created on DC01.
Verified the client appeared in AD Users and Computers
on the server.

### Step 3 — Configured Both Machines
Configured DNS on the client to point to DC01.
Verified domain join was successful.
Logged into client using a domain user account.

### Step 4 — Created a GPO (Wallpaper Policy)
**What is a GPO?**
Group Policy Object — a set of rules applied to users
or computers in a domain. GPOs control everything from
password requirements to desktop wallpapers to software
installation.

**What I did:**
- Opened Group Policy Management Console on DC01
- Created a new GPO named "Wallpaper Policy"
- Edited the GPO: User Configuration → Policies →
  Administrative Templates → Desktop → Desktop Wallpaper
- Set a specific wallpaper path
- Linked the GPO to the domain

**Result:**
Ran `gpupdate /force` on Client01.
The wallpaper policy applied successfully.
The configured wallpaper appeared on Client01 —
confirming end-to-end GPO deployment worked correctly.

---

## Security Relevance of GPOs

GPOs are one of the most powerful security tools in
an enterprise Windows environment. They can enforce:

- Password complexity requirements
- Account lockout policies
- Disabling USB ports on all machines
- Blocking access to Control Panel
- Enforcing screensaver with password lock
- Restricting software installation
- Configuring Windows Firewall rules centrally

A misconfigured GPO can create security gaps across
every machine in the domain simultaneously. A well-
configured GPO baseline is a foundational security
control in any enterprise environment.

---

## Key Takeaway
Active Directory is not just an IT tool — it is a
critical security infrastructure. Understanding how
AD works, how GPOs are created and applied, and how
attackers target AD is essential knowledge for any
enterprise security engineer.

---
*Active Directory Lab — Intime Solutions*
*VM Environment: DC01 (Windows Server) + Client01*
*Role: Technical Associate @ Intime Solutions, Bangalore*
