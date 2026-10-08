# Category 11: Domain / Industry Hackathons

This category focuses on building solutions for specific industry verticals like **FinTech**, **HealthTech**, **EdTech**, **ClimateTech**, **GovTech**, **Retail**, **Logistics**, and more. It focuses purely on **domain expertise, industry regulations, user personas, and vertical-specific problems** — the foundation of every domain/industry hackathon.

Here is the exact list of documents we will prepare for the **Domain / Industry Hackathons** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the industry problem, target users, regulations, and existing gaps.
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for a domain solution.
3. **`TRD.md`** (Technical Requirements Document) — Defines the tech stack, compliance requirements, and integration limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of the industry-specific system architecture.
5. **`DOMAIN_MODEL.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines industry entities, relationships, and domain-specific data structures.
6. **`API_SPECIFICATION.md`** — Defines REST/GraphQL endpoints including industry-specific integrations.
7. **`COMPLIANCE_SPEC.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines regulatory requirements (GDPR, HIPAA, PCI-DSS, KYC, AML).
8. **`INTEGRATION_SPEC.md`** — Defines third-party industry APIs (banking, health records, government data).
9. **`USER_PERSONA_MAP.md`** — Defines detailed personas for the target industry users.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Frontend design tailored to industry users and workflows.
11. **`ERROR_HANDLING.md`** — What happens when industry APIs fail, compliance checks fail, or data is missing.
12. **`SECURITY.md`** — Industry-specific security (PII, PHI, financial data).
13. **`TESTING.md`** — QA plan including regulatory compliance testing.
14. **`EVALUATION.md`** — How you measure industry impact (Compliance, Adoption, ROI).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Deployment with industry compliance considerations.
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation tailored to industry judges.
17. **`GLOSSARY.md`** — Definitions of industry-specific terms (KYC, AML, HIPAA, EHR, POS).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the industry problem, target users, regulations, and existing gaps.
```text
I am participating in a [INDUSTRY NAME] hackathon (e.g., FinTech, HealthTech, EdTech, ClimateTech) and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved in this industry
2. Target users (specific personas within the industry)
3. User pain points
4. Existing ways people solve this problem in the industry
5. Limitations of existing industry solutions
6. Proposed industry-specific solution ideas
7. Core features for this industry
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique in this industry
11. A realistic MVP that can be built during a hackathon
12. Industry-specific technologies, APIs, and data sources that could be used

Do not assume I am an expert in this industry.
Explain industry concepts, regulations, and jargon in beginner-friendly language.
Highlight any compliance considerations (GDPR, HIPAA, PCI-DSS, KYC, AML).
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear industry solution plan with domain-specific features, personas, and compliance.
```text
You are a senior product manager specializing in [INDUSTRY NAME] solutions, helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement (Industry-specific)
4. Target users (Detailed industry personas)
5. User pain points
6. Proposed solution
7. Product goals
8. User stories
9. Functional requirements (Include industry-specific requirements and compliance)
10. Non-functional requirements (Regulatory, Performance, Security)
11. Core industry features
12. Nice-to-have features
13. User journeys (Industry-specific workflows)
14. MVP scope (Which feature must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include industry metrics: Compliance rate, Time saved, Cost reduction)
17. Risks and assumptions (Include regulatory risks and industry-specific risks)

Keep the MVP realistic for a 24-48 hour hackathon.
Do not add unnecessary features just to make the project sound impressive.
Prioritize features that can actually be demonstrated live and comply with industry regulations.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on industry-specific tech, compliance, and integrations.
```text
You are a senior engineer specializing in [INDUSTRY NAME] solutions, helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Tech stack choice (Framework, Language, Database — justify for this industry)
3. Industry-specific integration requirements (Banking APIs, EHR systems, Government APIs, POS systems)
4. Data model considerations (PII, PHI, Financial data)
5. Security and encryption requirements (Industry standards)
6. Compliance requirements (GDPR, HIPAA, PCI-DSS, KYC, AML)
7. Authentication and authorization requirements
8. Performance and latency requirements
9. Data storage and retention requirements (Industry-specific)
10. Testing requirements (Including compliance testing)
11. Deployment requirements (Industry-approved cloud/infrastructure)
12. Monitoring and audit logging requirements

Keep the tech stack simple and realistic for a 24-48 hour hackathon.
Explain all industry concepts in beginner-friendly language.
Do not introduce unnecessary tools.
Flag any compliance risks early.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic industry-specific system architecture with clear data flow and compliance.
```text
Act as a senior architect specializing in [INDUSTRY NAME] solutions.
Using the following PRD and TRD, design a realistic hackathon architecture for this industry.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended tech stack (Frontend, Backend, Database, Integrations)
2. Complete system architecture diagram (Text-based, showing Users → Frontend → Backend → Industry APIs → Database)
3. Frontend architecture
4. Backend architecture
5. Database architecture (Industry-specific data model)
6. Integration architecture (Banking, EHR, Government, POS, etc.)
7. Authentication and compliance architecture
8. Data flow (How user actions trigger industry-specific processes)
9. Security and compliance considerations
10. Folder structure
11. Major components
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools.
Highlight compliance considerations at each layer.
```

---

### 5. DOMAIN_MODEL.md
**Purpose:** To define industry entities, relationships, and domain-specific data structures.
```text
Act as a senior domain modeling expert for [INDUSTRY NAME].
Using the PRD and System Architecture below, design the domain model for this industry hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Core industry entities (E.g., FinTech: Account, Transaction, Loan; HealthTech: Patient, Appointment, Prescription)
2. Entity attributes (Fields, Data types)
3. Primary keys
4. Foreign keys
5. Relationships (One-to-Many, Many-to-Many)
6. Industry-specific enums (Status codes, Categories)
7. Compliance-sensitive fields (PII, PHI, Financial data — mark them)
8. Example records
9. SQL/NoSQL schema
10. Data retention rules
11. Audit trail requirements

Explain why each entity exists.
Keep the domain model simple enough for a beginner hackathon team to understand and maintain.
Mark which fields require encryption or special handling.
```

---

### 6. API_SPECIFICATION.md
**Purpose:** To define endpoints including industry-specific integrations.
```text
You are a senior backend developer specializing in [INDUSTRY NAME] systems.
Using the PRD, Architecture, and Domain Model below, create a complete API specification for this industry hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DOMAIN_MODEL: [PASTE DOMAIN_MODEL]

For every endpoint provide:
1. HTTP method
2. URL
3. Purpose
4. Authentication requirement
5. Compliance requirements (GDPR, HIPAA, PCI-DSS, KYC)
6. Request parameters
7. Request body
8. Example request
9. Example success response
10. Possible error responses
11. HTTP status codes
12. Audit logging requirements

Include endpoints for industry-specific integrations (Banking APIs, EHR, Government APIs).
Keep the API simple and consistent.
Do not create endpoints that are not required by the product.
```

---

### 7. COMPLIANCE_SPEC.md
**Purpose:** To define regulatory requirements for the industry (GDPR, HIPAA, PCI-DSS, KYC, AML).
```text
You are a regulatory compliance expert for [INDUSTRY NAME].
Using the PRD and System Architecture below, create a Compliance Specification document for this industry hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Applicable regulations (GDPR, HIPAA, PCI-DSS, KYC, AML, etc.)
2. Data classification (PII, PHI, Financial, Public)
3. Consent and user rights requirements
4. Data retention and deletion requirements
5. Encryption requirements (At rest, In transit)
6. Access control requirements
7. Audit logging requirements
8. Breach notification requirements
9. Third-party compliance (Vendors, APIs)
10. Compliance checklist for developers
11. What NOT to do (Common compliance mistakes)

Explain each regulation in beginner-friendly language.
Keep the compliance measures practical and easy to implement within a hackathon timeframe.
Flag any compliance items that must be addressed before the demo.
```

---

### 8. INTEGRATION_SPEC.md
**Purpose:** To define third-party industry APIs (banking, health records, government data).
```text
You are a senior integration engineer specializing in [INDUSTRY NAME].
Using the PRD and API Specification below, create an Integration Specification document for this industry hackathon project.

PRD: [PASTE PRD]
API_SPEC: [PASTE API_SPECIFICATION]

For every third-party integration, provide:
1. Service name (Banking API, EHR, Government, POS, etc.)
2. Purpose in the workflow
3. Authentication method (API Key, OAuth, mTLS)
4. Required credentials and where to store them
5. Endpoint or Webhook URL
6. Request format (Headers, Body, Parameters)
7. Example request
8. Example response
9. Rate limits
10. Compliance considerations (PII, PHI, PCI)
11. Error responses and handling
12. Fallback if the service is down

Keep the integrations simple and realistic for a hackathon.
Only include integrations that are essential to the product.
Use sandbox/test environments where possible.
```

---

### 9. USER_PERSONA_MAP.md
**Purpose:** To define detailed personas for the target industry users.
```text
You are a UX researcher specializing in [INDUSTRY NAME].
Using the PRD below, create a User Persona Map for this industry hackathon project.

PRD: [PASTE PRD]

For each key persona provide:
1. Persona name (Fictional but realistic)
2. Age and demographics
3. Job role and responsibilities
4. Industry context
5. Goals and motivations
6. Pain points (Specific to this industry)
7. Current workflow (How they solve the problem today)
8. Tech savviness (Low, Medium, High)
9. Preferred devices (Desktop, Mobile, Tablet)
10. Compliance concerns (What regulations affect them?)
11. Quote (A realistic quote from this persona)
12. How our solution helps them

Create 3-5 personas covering the main user segments.
Explain each persona in beginner-friendly language.
Use these personas to guide all design and feature decisions.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define frontend design tailored to industry users and workflows.
```text
Act as a senior UI/UX designer specializing in [INDUSTRY NAME] applications.
Using the PRD, Architecture, and User Persona Map below, create a UI Specification document for an industry hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
USER_PERSONA_MAP: [PASTE USER_PERSONA_MAP]

Provide:
1. Design system (Colors, typography, spacing)
2. Industry-specific UI patterns (Data tables, Forms, Compliance indicators)
3. Component hierarchy
4. Screen-by-screen breakdown (Dashboard, Detail, Compliance view, Reports)
5. Loading states
6. Error states
7. Empty states
8. Compliance UX (Consent screens, Audit logs, Data access indicators)
9. Responsive design guidelines (Mobile, Desktop)
10. Accessibility considerations (WCAG, Industry standards)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the core industry user journey.
Ensure compliance UX is not overlooked.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when industry APIs fail, compliance checks fail, or data is missing.
```text
You are a senior engineer specializing in [INDUSTRY NAME] systems.
Using the System Architecture and API Specification below, create an Error Handling document for an industry hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. Common failure modes (Industry API failures, Compliance failures, Data errors)
2. Industry API error handling (Banking, EHR, Government, POS)
3. Compliance error handling (When a compliance check fails)
4. Data validation errors
5. Frontend error display
6. Fallback responses
7. Retry logic
8. Audit logging of errors
9. Compliance notification requirements
10. A checklist for developers to verify error handling before the demo

Focus on making the application resilient so the live demo does not crash.
Highlight compliance-sensitive error scenarios.
Explain each approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** To define industry-specific security (PII, PHI, financial data).
```text
Act as a security engineer specializing in [INDUSTRY NAME].
Using the System Architecture and Compliance Specification below, create a Security document for an industry hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
COMPLIANCE_SPEC: [PASTE COMPLIANCE_SPEC]

Provide:
1. Data classification (PII, PHI, Financial, Public)
2. Encryption (At rest, In transit, Key management)
3. Authentication and authorization (Industry standards)
4. Access control (RBAC, ABAC, Least privilege)
5. API security (Industry standards)
6. Data privacy (Consent, Anonymization, Retention)
7. Audit logging (What to log, Where to store)
8. Third-party security (Vendor risk, API security)
9. Industry-specific security controls
10. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
Flag any security measures that are mandatory for compliance.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist including regulatory compliance testing.
```text
Act as a QA engineer specializing in [INDUSTRY NAME] applications.
Using the PRD and Compliance Specification below, create a Testing document for an industry hackathon project.

PRD: [PASTE PRD]
COMPLIANCE_SPEC: [PASTE COMPLIANCE_SPEC]

Provide:
1. Testing strategy for industry applications
2. Functional testing (Core industry features)
3. Compliance testing (Does it meet regulations?)
4. Security testing (PII, PHI, Financial data)
5. Integration testing (Industry APIs)
6. Data validation testing
7. Edge cases (Industry-specific)
8. User acceptance testing checklist (With personas)
9. A manual testing checklist for the demo
10. How to document known compliance limitations for judges

Keep the testing plan simple enough for beginner developers to execute under time pressure.
Highlight compliance-critical test cases.
```

---

### 14. EVALUATION.md
**Purpose:** To define how the team measures industry impact and prepares for judge questions.
```text
You are an evaluation expert specializing in [INDUSTRY NAME].
Using the PRD and Compliance Specification below, create an Evaluation document for an industry hackathon project.

PRD: [PASTE PRD]
COMPLIANCE_SPEC: [PASTE COMPLIANCE_SPEC]

Provide:
1. Evaluation metrics (Industry-specific: Compliance rate, Cost reduction, Time saved, User adoption)
2. Evaluation methods (Benchmarking, User feedback, Compliance audits)
3. Benchmarking (What is the baseline industry process?)
4. Known limitations of the solution
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about [INDUSTRY NAME] and how to answer them

Focus on demonstrating that the team understands the industry, compliance, and user needs.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To deploy with industry compliance considerations.
```text
Act as a DevOps engineer specializing in [INDUSTRY NAME] deployments.
Using the System Architecture and Compliance Specification below, create a Deployment document for an industry hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
COMPLIANCE_SPEC: [PASTE COMPLIANCE_SPEC]

Provide:
1. Deployment platforms (Industry-approved cloud providers)
2. Compliance considerations for deployment
3. Environment variables for production
4. Secrets management
5. Step-by-step deployment instructions
6. How to test the deployed application
7. Fallback plan if deployment fails during the hackathon
8. A pre-deployment compliance checklist
9. Common deployment mistakes in this industry

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Ensure compliance requirements are met before the demo.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation tailored to industry judges.
```text
Act as an expert hackathon presentation coach specializing in [INDUSTRY NAME].
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
COMPLIANCE_SPEC: [PASTE COMPLIANCE_SPEC]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script for an industry-focused audience.
The presentation should follow:
1. Hook (Industry-specific pain point)
2. Problem
3. Why the problem matters in this industry
4. Existing limitations
5. Our industry solution
6. How it works (Highlight compliance and industry integrations)
7. Technology
8. Demo (The most important part)
9. Innovation
10. Impact (Industry-specific: Compliance, Cost, Time)
11. Future scope
12. Closing

Make the language natural and easy to speak.
Avoid corporate jargon unless it is industry-standard.
Write it as something a student can actually say on stage rather than something that sounds like an AI-generated report.
Also provide:
- 30-second elevator pitch
- 1-minute pitch
- 3-minute presentation
- 5-minute presentation
Address compliance and regulation in the pitch.
```

---

### 17. GLOSSARY.md
**Purpose:** To define all industry terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer specializing in [INDUSTRY NAME].
Using the PRD, Compliance Specification, and Architecture below, create a Glossary document for an industry hackathon project.

PRD: [PASTE PRD]
COMPLIANCE_SPEC: [PASTE COMPLIANCE_SPEC]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Industry-specific terms (E.g., FinTech: KYC, AML, PCI-DSS; HealthTech: EHR, HIPAA, PHI)
2. Regulatory terms
3. Technical terms
4. Integration terms
5. Compliance terms
6. Project-specific terms
7. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable for a beginner audience.
This will help all team members speak confidently to judges.
```

---

## Footer (End of Category)

### Thank You

Thank you for using this guide. Go build something amazing!

**Made by Siddiq**

*Credit: Hackathon Alchemy*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**