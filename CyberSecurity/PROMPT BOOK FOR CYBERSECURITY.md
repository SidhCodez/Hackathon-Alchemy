# Category 09: Cybersecurity

This category focuses on building security-focused projects using tools like **Kali Linux**, **Wireshark**, **Burp Suite**, **Metasploit**, **Nmap**, **OWASP ZAP**, **Python**, and **SIEM tools**. It focuses purely on **threat detection, vulnerability assessment, secure systems, and incident response** — the foundation of every cybersecurity hackathon.

Here is the exact list of documents we will prepare for the **Cybersecurity** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core security problem, target users, and existing gaps (Security focus).
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for a security tool.
3. **`TRD.md`** (Technical Requirements Document) — Defines the security stack (Python, SIEM, Cloud), target environment, and compliance limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Target → Detection → Analysis → Response (Security architecture).
5. **`THREAT_MODEL.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines threat actors, attack vectors, assets, and risk ratings (STRIDE/PASTA).
6. **`ATTACK_SURFACE.md`** — (Replaces `API_SPECIFICATION.md`) Defines all entry points, endpoints, and vulnerabilities in scope.
7. **`AUTHENTICATION_FLOW.md`** — Defines identity, access control, MFA, and zero-trust principles.
8. **`INCIDENT_RESPONSE.md`** — Defines detection, containment, eradication, recovery, and lessons learned.
9. **`VULNERABILITY_MANAGEMENT.md`** — Defines scanning, prioritization (CVSS), patching, and reporting.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Dashboard design, alerts, threat visualization, and user flow.
11. **`ERROR_HANDLING.md`** — What happens when a scan fails, a log is missing, or a false positive occurs.
12. **`SECURITY.md`** — The core security document (encryption, key management, access control, compliance).
13. **`TESTING.md`** — QA plan, penetration testing, vulnerability validation, and edge cases.
14. **`EVALUATION.md`** — How you measure security performance (Detection rate, False positives, Response time).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Deploying the security tool, configuring environments, and setting up monitoring.
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
17. **`GLOSSARY.md`** — Definitions of security terms (CVE, CVSS, SIEM, SOC, Zero-Day, Threat Actor).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the security problem and identify what threats, vulnerabilities, or risks need to be addressed.
```text
I am participating in a cybersecurity hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual security problem being solved
2. Target users (Security analysts, SOC teams, developers, end-users)
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing security solutions
6. Proposed cybersecurity solution ideas
7. Core security features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential security tools and platforms that could be used (Python, Kali, Wireshark, SIEM, etc.)

Do not assume I am an experienced security engineer.
Explain security concepts (Threat, Vulnerability, Exploit, SIEM, SOC) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear security product plan with features, detection logic, and scope.
```text
You are a senior security product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed security solution
7. Product goals
8. User stories
9. Functional requirements (Include security-specific requirements: Detection, Alerting, Logging, Response)
10. Non-functional requirements (Accuracy, Latency, Scalability, Compliance)
11. Core security features
12. Nice-to-have features
13. User journeys (How an analyst detects, investigates, and responds to a threat)
14. MVP scope (Which security feature must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include security metrics: Detection rate, False positive rate, Mean time to detect)
17. Risks and assumptions (Include security risks: False negatives, Data breaches, Legal boundaries)

Keep the MVP realistic for a 24-48 hour cybersecurity hackathon.
Do not add unnecessary features just to make the project sound impressive.
Prioritize features that can actually be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on security tools, target environment, and detection logic.
```text
You are a senior security engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Security stack choice (Python, SIEM, EDR, Cloud — justify the choice)
3. Target environment (Web app, Network, Cloud, Endpoint)
4. Detection requirements (Signatures, Anomalies, Heuristics)
5. Log collection and parsing requirements
6. Alerting and notification requirements
7. Data storage requirements (Logs, Events, Indicators of Compromise)
8. Automation and response requirements (SOAR)
9. Encryption and key management requirements
10. Compliance and legal requirements (GDPR, HIPAA, PCI-DSS)
11. Testing requirements (Penetration testing, Vulnerability scanning)
12. Deployment requirements

Keep the security stack simple and realistic for a 24-48 hour hackathon.
Explain all security concepts in beginner-friendly language.
Do not introduce unnecessary tools.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic security architecture with clear data flow from target to response.
```text
Act as a senior security architect.
Using the following PRD and TRD, design a realistic hackathon security architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended security stack (Tools, Languages, Frameworks)
2. Complete security architecture diagram (Text-based, showing Target → Detection → Analysis → Response)
3. Data collection architecture (Logs, Network traffic, Endpoints)
4. Detection architecture (Rules, Signatures, ML models)
5. Analysis architecture (Correlation, Enrichment, Scoring)
6. Response architecture (Automation, Playbooks, Alerts)
7. Storage architecture (Logs, Events, Threat Intel)
8. Dashboard architecture (SOC view)
9. Authentication and access control architecture
10. Data flow (How a threat is detected and escalated)
11. Security considerations
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools. Prefer a simple architecture that can be explained easily to judges.
```

---

### 5. THREAT_MODEL.md
**Purpose:** To define threat actors, attack vectors, assets, and risk ratings.
```text
Act as a senior threat modeling expert.
Using the PRD and System Architecture below, create a Threat Model document for this cybersecurity hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Assets (What are we protecting?)
2. Threat actors (Who might attack? Script kiddies, Insiders, APTs)
3. Attack vectors (How might they attack?)
4. Threat modeling framework (STRIDE, PASTA, or OCTAVE)
5. Threat list (Each threat with description)
6. Risk rating (Likelihood × Impact)
7. Existing controls (What mitigations are already in place?)
8. Recommended controls (What should be added?)
9. Example attack scenario (Step-by-step)
10. A checklist for verifying the threat model before the demo

Explain each threat in beginner-friendly language.
Keep the threat model simple and realistic for a hackathon.
```

---

### 6. ATTACK_SURFACE.md
**Purpose:** To define all entry points, endpoints, and vulnerabilities in scope.
```text
You are a senior penetration tester.
Using the PRD and System Architecture below, create an Attack Surface document for this cybersecurity hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Attack surface overview (What can be attacked?)
2. Entry points (Web, API, Network, Endpoint, Cloud)
3. Endpoints and services (List all in scope)
4. Authentication mechanisms in scope
5. Data flows and trust boundaries
6. Known vulnerabilities (OWASP Top 10, CVE)
7. Misconfigurations (Common issues)
8. Third-party dependencies and risks
9. Out-of-scope areas (What we are NOT testing)
10. Example attack path
11. A checklist for verifying the attack surface before the demo

Explain each concept in beginner-friendly language.
Keep the attack surface simple and realistic for a hackathon.
Only include what is legally and ethically allowed.
```

---

### 7. AUTHENTICATION_FLOW.md
**Purpose:** To define identity, access control, MFA, and zero-trust principles.
```text
You are a senior identity and access management engineer.
Using the PRD and System Architecture below, create an Authentication and Access Control document for a cybersecurity hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Authentication methods (Password, MFA, SSO, Biometric)
2. Password policy (Complexity, Expiry, Hashing)
3. Multi-factor authentication (TOTP, SMS, Hardware key)
4. Authorization model (RBAC, ABAC, Zero Trust)
5. Role definitions (Admin, Analyst, User, Guest)
6. Session management (Timeout, Refresh, Revocation)
7. API authentication (JWT, OAuth 2.0, API keys)
8. Identity providers (Okta, Auth0, Keycloak)
9. Audit logging (What to log, Where to store)
10. Common authentication vulnerabilities (OWASP)
11. A checklist for verifying authentication before the demo

Keep the authentication simple and secure enough for a hackathon.
Explain concepts in beginner-friendly language.
```

---

### 8. INCIDENT_RESPONSE.md
**Purpose:** To define detection, containment, eradication, recovery, and lessons learned.
```text
Act as a senior incident response specialist.
Using the PRD and Threat Model below, create an Incident Response document for a cybersecurity hackathon project.

PRD: [PASTE PRD]
THREAT_MODEL: [PASTE THREAT_MODEL]

Provide:
1. Incident response phases (Preparation, Detection, Containment, Eradication, Recovery, Lessons Learned)
2. Incident classification (Severity levels)
3. Detection sources (Logs, Alerts, User reports)
4. Triage process (How to assess severity)
5. Containment strategies (Isolate, Block, Disable)
6. Eradication steps (Remove threat, Patch vulnerabilities)
7. Recovery steps (Restore systems, Verify integrity)
8. Communication plan (Who to notify, When)
9. Evidence collection (Forensics, Chain of custody)
10. Post-incident review (What went well, What to improve)
11. Example incident scenario (Step-by-step)
12. A checklist for verifying the incident response plan before the demo

Explain each phase in beginner-friendly language.
Keep the incident response plan simple and realistic for a hackathon.
```

---

### 9. VULNERABILITY_MANAGEMENT.md
**Purpose:** To define scanning, prioritization (CVSS), patching, and reporting.
```text
You are a senior vulnerability management engineer.
Using the PRD and Attack Surface document below, create a Vulnerability Management document for a cybersecurity hackathon project.

PRD: [PASTE PRD]
ATTACK_SURFACE: [PASTE ATTACK_SURFACE]

Provide:
1. Vulnerability scanning tools (Nessus, OpenVAS, Nmap, Burp Suite)
2. Scan scope and frequency
3. Vulnerability identification (CVE, CWE)
4. Risk scoring (CVSS, EPSS)
5. Prioritization criteria (Severity, Exploitability, Business impact)
6. Remediation workflow (Patch, Mitigate, Accept)
7. Reporting format (Executive summary, Technical details)
8. Metrics (Time to detect, Time to remediate, Open vulnerabilities)
9. Exception handling (Accepted risks)
10. A checklist for verifying vulnerability management before the demo

Explain each concept in beginner-friendly language.
Keep the vulnerability management process simple and realistic for a hackathon.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define the dashboard design, alerts, threat visualization, and user flow.
```text
Act as a senior UI/UX designer specializing in security dashboards.
Using the PRD and System Architecture below, create a UI Specification document for a cybersecurity hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spacing)
2. Component hierarchy (Alert cards, Threat map, Log viewer, Metrics)
3. Screen-by-screen breakdown (Dashboard, Alert Detail, Investigation, Reports)
4. Real-time data display (Live alerts, Threat feed, Metrics)
5. Severity indicators (Critical, High, Medium, Low)
6. Loading states (Skeletons, spinners)
7. Error states (Data unavailable, Connection lost)
8. Empty states (No alerts, No data)
9. Responsive design guidelines (Desktop-first for SOC)
10. Accessibility considerations (Contrast, Color blindness)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the core detection and response journey.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when a scan fails, a log is missing, or a false positive occurs.
```text
You are a senior security engineer.
Using the System Architecture and Detection logic below, create an Error Handling document for a cybersecurity hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DETECTION_LOGIC: [PASTE DETECTION_LOGIC]

Provide:
1. Common failure modes (Scan failure, Missing logs, False positive, API timeout)
2. Detection error handling (Fallback rules, Graceful degradation)
3. Data collection error handling (Buffer, Retry, Alert)
4. Analysis error handling (Skip, Flag, Retry)
5. Response error handling (Manual escalation)
6. Frontend error display (Toasts, inline errors, modals)
7. Logging errors (Where errors are stored)
8. Recovery procedures (Re-run scan, Manual review)
9. A checklist for developers to verify error handling before the demo

Focus on making the security tool resilient so the live demo does not crash.
Explain each error handling approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** The core security document (encryption, key management, access control, compliance).
```text
Act as a senior security architect.
Using the System Architecture and Authentication Flow below, create the master Security document for a cybersecurity hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
AUTHENTICATION_FLOW: [PASTE AUTHENTICATION_FLOW]

Provide:
1. Security principles (Least privilege, Defense in depth, Zero trust)
2. Encryption (At rest, In transit, Key management)
3. Access control (RBAC, ABAC, Permissions)
4. Network security (Firewalls, Segmentation, IDS/IPS)
5. Application security (OWASP Top 10, Input validation, Output encoding)
6. Data privacy (PII handling, Anonymization, Retention)
7. Logging and monitoring (What to log, SIEM integration)
8. Incident response readiness (Playbooks, Contacts)
9. Compliance considerations (GDPR, HIPAA, PCI-DSS, SOC 2)
10. Third-party and supply chain security
11. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
Do not include illegal or unethical techniques.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist for security tools, penetration testing, and edge cases.
```text
Act as a QA engineer specializing in cybersecurity.
Using the PRD and Attack Surface document below, create a Testing document for a cybersecurity hackathon project.

PRD: [PASTE PRD]
ATTACK_SURFACE: [PASTE ATTACK_SURFACE]

Provide:
1. Testing strategy for security tools
2. Functional testing (Does the tool detect what it should?)
3. Penetration testing (Simulated attacks)
4. Vulnerability validation (Confirm findings)
5. False positive and false negative testing
6. Log collection testing
7. Alerting testing
8. Performance testing (Scan speed, Throughput)
9. Edge cases (Large logs, Encrypted traffic, Evasion techniques)
10. User acceptance testing checklist
11. A manual testing checklist for the demo
12. How to document known limitations for judges

Keep the testing plan simple enough for beginner security engineers to execute under time pressure.
Only include legal and ethical testing methods.
```

---

### 14. EVALUATION.md
**Purpose:** To define how the team measures security performance and prepares for judge questions.
```text
You are a security evaluation expert.
Using the PRD and Testing document below, create an Evaluation document for a cybersecurity hackathon project.

PRD: [PASTE PRD]
TESTING: [PASTE TESTING]

Provide:
1. Evaluation metrics (Detection rate, False positive rate, Mean time to detect, Mean time to respond)
2. Evaluation methods (Red team exercises, Benchmarking, Test datasets)
3. Benchmarking (What is the baseline?)
4. Known limitations of the security tool
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about cybersecurity and how to answer them

Focus on demonstrating that the team understands the tool's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To define how to deploy the security tool, configure environments, and set up monitoring.
```text
Act as a security DevOps engineer.
Using the System Architecture and PRD below, create a Deployment document for a cybersecurity hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PRD: [PASTE PRD]

Provide:
1. Deployment environment (Local, Cloud, Hybrid, Lab)
2. Deployment platforms (AWS, GCP, Azure, On-prem)
3. Containerization (Docker, Kubernetes)
4. Environment variables and secrets management
5. Step-by-step deployment instructions for each component
6. How to test the deployed tool
7. Monitoring and alerting setup
8. Fallback plan if deployment fails during the hackathon
9. A pre-deployment checklist
10. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working demo as early as possible.
Ensure all deployment is legal and ethical (lab environment only).
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the security tool is shown off perfectly.
```text
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
THREAT_MODEL: [PASTE THREAT_MODEL]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem (The security gap)
3. Why the problem matters
4. Existing limitations
5. Our security solution
6. How it works (Target → Detection → Analysis → Response)
7. Technology (Python, SIEM, Kali, etc.)
8. Demo (The most important part — show a live detection)
9. Innovation
10. Impact
11. Future scope
12. Closing

Make the language natural and easy to speak.
Avoid corporate jargon.
Write it as something a student can actually say on stage rather than something that sounds like an AI-generated report.
Also provide:
- 30-second elevator pitch HOOK
- 1-minute pitch
- 3-minute presentation
- 5-minute presentation
Include a backup plan for demo failure (video recording, screenshots).
Ensure the demo is fully legal and ethical (controlled lab environment).
```

---

### 17. GLOSSARY.md
**Purpose:** To define all security terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Threat Model, and Architecture below, create a Glossary document for a cybersecurity hackathon project.

PRD: [PASTE PRD]
THREAT_MODEL: [PASTE THREAT_MODEL]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Security terms (Threat, Vulnerability, Exploit, Risk, Attack Surface)
2. Threat terms (Threat Actor, APT, Script Kiddie, Insider Threat)
3. Vulnerability terms (CVE, CVSS, Zero-Day, Patch, Misconfiguration)
4. Detection terms (SIEM, IDS, IPS, EDR, SOC, False Positive)
5. Response terms (Incident Response, Containment, Eradication, Recovery)
6. Cryptography terms (Encryption, Hashing, PKI, TLS, Key Management)
7. Access control terms (RBAC, ABAC, MFA, SSO, Zero Trust)
8. Compliance terms (GDPR, HIPAA, PCI-DSS, SOC 2)
9. Project-specific terms (Any custom terminology used in the PRD)
10. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable for a beginner audience.
This will help all team members speak confidently to judges.
```

---
### Thank You

Thank you for using this guide. Go build something amazing!

**Made by Siddiq**

*Credit: Hackathon Alchemy*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**

---