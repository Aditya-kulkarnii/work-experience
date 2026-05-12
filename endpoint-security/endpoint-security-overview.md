# Endpoint Security — Complete Overview

## What is an Endpoint?
Any device that connects to a network and can be used
as an entry point by an attacker.

Examples: laptops, desktops, smartphones, tablets,
servers, printers, IoT devices, virtual machines.

Every endpoint is a potential attack surface.
The more endpoints an organization has — the larger
its attack surface.

---

## Basics of Endpoint Security
Endpoint security protects individual devices from
threats — malware, ransomware, unauthorized access,
and data theft.

Modern endpoint security goes far beyond traditional
antivirus. It includes:
- Real-time threat detection and prevention
- Behavioral analysis — detecting malicious behavior
  even from unknown threats
- Automated response — isolating infected devices
- Threat hunting — proactively searching for hidden threats
- Forensic investigation capabilities

---

## The Attack Surface — Entry Points on an Endpoint

Common ways attackers get onto an endpoint:
- **Phishing emails** — malicious attachments or links
- **Drive-by downloads** — visiting compromised websites
- **Software vulnerabilities** — unpatched applications
- **USB drops** — malicious USB devices left in public
- **Remote Desktop Protocol (RDP)** — brute forced or
  exploited RDP sessions
- **Supply chain attacks** — malicious code in
  legitimate software updates
- **Credential theft** — stolen passwords used to log in

---

## Evolution of Endpoint Security

### Generation 1 — Signature-Based Antivirus (1990s)
Scans files against a database of known malware signatures.
Limitation: cannot detect unknown or new malware.
Attackers simply modified malware slightly to evade it.

### Generation 2 — Heuristic Detection (2000s)
Analyzes code behavior patterns instead of just signatures.
Better at detecting variants of known malware.
Still struggled with completely new attack techniques.

### Generation 3 — Behavioral Analysis (2010s)
Monitors what programs actually do at runtime.
Detects suspicious behavior even from unknown malware.
Introduction of sandboxing — run suspicious files in
isolated environment to observe behavior safely.

### Generation 4 — EDR (2013 onwards)
Endpoint Detection and Response — continuous monitoring,
recording all endpoint activity, detection, and response.
Can detect attacks that bypass prevention completely.
Enables forensic investigation after an incident.

### Generation 5 — XDR and AI (2020s — current)
Extended Detection and Response — correlates endpoint
data with network, cloud, email, and identity signals.
AI and machine learning for behavioral anomaly detection.
Automated response — contain threats without human action.
Predictive capabilities — stop attacks before they execute.

---

## Industry Frameworks

### Gartner Magic Quadrant
Annual analyst report ranking cybersecurity vendors
in four quadrants: Leaders, Challengers, Visionaries,
Niche Players.

Leaders quadrant = strongest execution and vision.
Used by enterprises to shortlist vendors for evaluation.

For endpoint security the consistent Leaders are:
CrowdStrike, Microsoft, SentinelOne, and Palo Alto.

### MITRE ATT&CK Framework
A globally recognized knowledge base of adversary
tactics, techniques, and procedures based on
real-world observations.

Organized into: Tactics (the goal) → Techniques
(how they achieve it) → Sub-techniques (specific methods)

14 Tactics including: Initial Access, Execution,
Persistence, Privilege Escalation, Defense Evasion,
Credential Access, Discovery, Lateral Movement,
Collection, Exfiltration, Command and Control.

Endpoint security vendors map their detections to
MITRE ATT&CK — showing which techniques their
product can detect and prevent.

---

## Major Endpoint Security Vendors

### 1. CrowdStrike — Falcon Platform
Global market leader in EDR/XDR.
Cloud-native architecture — lightweight agent,
all processing in the cloud via Threat Graph.
Threat Graph: AI-powered graph database recording
all endpoint activity globally in real time.
Known for: fastest detection, threat hunting capability.
Note: July 2024 incident — a faulty content update
caused global Windows BSOD across millions of devices.
Lesson: even security tools can be a risk if not
managed carefully.

### 2. Microsoft Defender
Built into Windows — zero additional deployment needed.
Included in Microsoft 365 E5 at no extra cost.
Best choice for organizations already on M365.
Deeply integrated with Entra ID, Sentinel SIEM,
and the entire Microsoft security stack.

### 3. SentinelOne — Singularity Platform
Known for: autonomous AI response without human action.
Unique feature: ransomware rollback — can automatically
reverse changes made by ransomware to restore files.
Storyline: automatically correlates all related events
into a single attack story for investigation.
Purple AI: generative AI for threat hunting queries.

### 4. Palo Alto Cortex — XDR and XSIAM
Best-in-class network + endpoint correlation.
Cortex XDR: correlates endpoint, network, and cloud
telemetry in one platform.
XSIAM: AI-driven SOC platform — replaces traditional
SIEM with automated detection and response.
Best fit: large SOC teams and enterprises that also
use Palo Alto NGFWs (full ecosystem integration).

### 5. Trend Micro — Vision One
Strongest protection for server workloads and
cloud environments.
Particularly strong in APAC region.
Best fit: organizations with heavy server and
cloud infrastructure.

### 6. Symantec / Broadcom
Legacy enterprise endpoint protection.
Best-in-class DLP (Data Loss Prevention) capabilities.
Migration concerns since Broadcom acquisition —
some customers have moved to other vendors.

### 7. Trellix (formerly McAfee + FireEye)
Strong in legacy enterprise environments.
Significant presence in US federal government.
Merging of McAfee Enterprise and FireEye capabilities.

### 8. ESET
Lightweight agent — minimal system performance impact.
Strong detection rates with low false positives.
Affordable — popular in Europe and mid-market organizations.
Best fit: organizations needing strong security
without heavy resource consumption.

### 9. Sophos — Intercept X
Synchronized Security: firewall and endpoint share
threat intelligence in real time.
Strong MDR (Managed Detection and Response) service.
Best fit: mid-market organizations wanting firewall
and endpoint from one vendor.

### 10. Malwarebytes
Focused on SMB (small and medium business) market.
Strong remediation capabilities — excellent at
cleaning already-infected systems.
Used as a secondary scanner alongside primary AV.

---

## Key Takeaway
The endpoint security market has moved far beyond
antivirus. Modern organizations need EDR at minimum
and are moving toward XDR that correlates signals
across endpoints, networks, cloud, and identity.

For my career path toward Palo Alto Networks —
Cortex XDR and XSIAM are the most relevant products
to understand deeply. They represent the direction
the entire industry is moving toward: AI-driven,
automated, correlated security operations.

---
*Endpoint Security — Intime Solutions Work Learning*
*Role: Technical Associate @ Intime Solutions, Bangalore*
