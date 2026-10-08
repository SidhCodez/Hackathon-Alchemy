
# Category 13: Social Impact / Civic

This category focuses on building solutions for **NGOs**, **government**, **accessibility**, **sustainability**, and **public good** using tools like **web frameworks**, **mobile apps**, **data platforms**, and **open-source technologies**. It focuses purely on **impact, inclusion, community, and solving real social problems** — the foundation of every Social Impact/Civic hackathon.

Here is the exact list of documents we will prepare for the **Social Impact / Civic** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the social problem, affected communities, and existing gaps.
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and impact metrics.
3. **`TRD.md`** (Technical Requirements Document) — Defines the tech stack, accessibility requirements, and deployment limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level architecture for a civic/social impact platform.
5. **`STAKEHOLDER_MAP.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines all stakeholders, their needs, and relationships.
6. **`API_SPECIFICATION.md`** — Defines endpoints including government/NGO integrations.
7. **`ACCESSIBILITY_SPEC.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines WCAG compliance, inclusive design, and assistive tech support.
8. **`IMPACT_MEASUREMENT.md`** — Defines how impact will be measured, tracked, and reported.
9. **`DATA_ETHICS.md`** — Defines ethical handling of vulnerable populations' data.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Frontend design focused on inclusion and accessibility.
11. **`ERROR_HANDLING.md`** — What happens when government APIs fail, data is missing, or users have low connectivity.
12. **`SECURITY.md`** — Data privacy for vulnerable populations, consent, and compliance.
13. **`TESTING.md`** — QA plan including accessibility testing and community validation.
14. **`EVALUATION.md`** — How you measure social impact (Lives improved, Access gained, Cost saved).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Deployment with low-bandwidth, offline-first, and accessibility considerations.
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation tailored to impact judges.
17. **`GLOSSARY.md`** — Definitions of civic and social impact terms (NGO, CSR, WCAG, Digital Divide, Last-Mile).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the social problem, affected communities, and existing gaps.
```text
I am participating in a Social Impact/Civic hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual social problem being solved
2. Affected communities and target users
3. User pain points (Social, Economic, Cultural)
4. Existing ways people or organizations solve this problem
5. Limitations of existing social/civic solutions
6. Proposed social impact solution ideas
7. Core features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential technologies, open data sources, and NGO/government APIs that could be used

Do not assume I am an expert in social work or civic tech.
Explain social impact concepts (Digital Divide, Last-Mile, Inclusion) in beginner-friendly language.
Highlight ethical considerations for vulnerable populations.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear social impact plan with features, beneficiaries, and impact metrics.
```text
You are a senior product manager specializing in social impact, helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement (Social context)
4. Target users (Beneficiaries, NGOs, Government, Volunteers)
5. User pain points
6. Proposed solution
7. Product goals (Social impact goals)
8. User stories
9. Functional requirements (Include accessibility and low-bandwidth requirements)
10. Non-functional requirements (Inclusion, Privacy, Accessibility, Offline capability)
11. Core features
12. Nice-to-have features
13. User journeys (How a beneficiary accesses and benefits)
14. MVP scope (Which feature must work during the demo?)
15. Out-of-scope features
16. Impact metrics (Lives improved, Access gained, Cost saved, Time saved)
17. Risks and assumptions (Include ethical risks, Digital Divide, Adoption barriers)

Keep the MVP realistic for a 24-48 hour hackathon.
Do not add unnecessary features just to make the project sound impressive.
Prioritize features that can actually be demonstrated live and create real impact.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on accessibility, low-bandwidth, and open-source tools.
```text
You are a senior engineer specializing in civic tech, helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Tech stack choice (Framework, Language, Database — justify for social impact)
3. Accessibility requirements (WCAG 2.1 AA, Screen readers, Keyboard-only)
4. Low-bandwidth and offline-first requirements
5. Multilingual and localization requirements
6. Open data and government API integrations
7. Data privacy and consent requirements
8. Security requirements for vulnerable populations
9. Performance and latency requirements (Low-end devices, Slow networks)
10. Deployment requirements (Low-cost, Scalable, Free-tier friendly)
11. Testing requirements (Including accessibility and community testing)
12. Sustainability requirements (How will this be maintained post-hackathon?)

Keep the tech stack simple, free, and realistic for a 24-48 hour hackathon.
Explain all concepts in beginner-friendly language.
Prioritize open-source and free-tier tools.
Flag any ethical concerns early.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic social impact architecture with clear data flow and accessibility.
```text
Act as a senior architect specializing in civic tech.
Using the following PRD and TRD, design a realistic hackathon architecture for this social impact project.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended tech stack (Frontend, Backend, Database, Integrations)
2. Complete system architecture diagram (Text-based, showing Users → Frontend → Backend → Data Sources → Impact)
3. Frontend architecture (Accessible, Low-bandwidth)
4. Backend architecture
5. Database architecture (Ethical data handling)
6. Integration architecture (Government APIs, NGO data, Open Data)
7. Accessibility architecture (Screen readers, Keyboard nav, Voice)
8. Offline-first architecture (If applicable)
9. Data flow (How a beneficiary's action creates impact)
10. Security and privacy considerations
11. Folder structure
12. Major components
13. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools.
Prioritize accessibility and inclusion at every layer.
```

---

### 5. STAKEHOLDER_MAP.md
**Purpose:** To define all stakeholders, their needs, and relationships.
```text
Act as a senior social impact strategist.
Using the PRD and System Architecture below, create a Stakeholder Map for this social impact hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Primary beneficiaries (Who directly benefits?)
2. Secondary beneficiaries (Who indirectly benefits?)
3. Implementing organizations (NGOs, Government, Community groups)
4. Funders and supporters (CSR, Grants, Donors)
5. Technical partners (Open-source communities, API providers)
6. Regulators and policymakers
7. For each stakeholder:
   - Their needs
   - Their pain points
   - How they interact with the solution
   - Their success metrics
8. Stakeholder relationships (Who influences whom?)
9. Power dynamics and considerations
10. Engagement strategy (How to involve stakeholders)
11. A checklist for verifying stakeholder alignment before the demo

Explain each stakeholder in beginner-friendly language.
Keep the stakeholder map simple and actionable.
Focus on the most critical stakeholders for the MVP.
```

---

### 6. API_SPECIFICATION.md
**Purpose:** To define endpoints including government/NGO integrations.
```text
You are a senior backend developer specializing in civic tech.
Using the PRD, Architecture, and Stakeholder Map below, create a complete API specification for this social impact hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
STAKEHOLDER_MAP: [PASTE STAKEHOLDER_MAP]

For every endpoint provide:
1. HTTP method
2. URL
3. Purpose
4. Authentication requirement
5. Privacy and consent requirements
6. Request parameters
7. Request body
8. Example request
9. Example success response
10. Possible error responses
11. HTTP status codes
12. Data minimization (What data is NOT collected?)

Include endpoints for government/NGO integrations (Open Data, Eligibility checks, Reporting).
Keep the API simple and consistent.
Do not create endpoints that are not required by the product.
Prioritize privacy and data minimization.
```

---

### 7. ACCESSIBILITY_SPEC.md
**Purpose:** To define WCAG compliance, inclusive design, and assistive tech support.
```text
You are an accessibility expert specializing in inclusive design.
Using the PRD and System Architecture below, create an Accessibility Specification document for this social impact hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. WCAG 2.1 AA compliance checklist
2. Visual accessibility (Contrast, Text size, Color blindness)
3. Motor accessibility (Keyboard navigation, Touch targets, Voice control)
4. Auditory accessibility (Captions, Transcripts, Visual alerts)
5. Cognitive accessibility (Simple language, Clear navigation, Consistency)
6. Screen reader compatibility (ARIA, Semantic HTML)
7. Multilingual and localization support
8. Low-literacy design considerations
9. Assistive technology compatibility
10. Testing tools and methods (axe, WAVE, Screen readers)
11. A pre-submission accessibility checklist

Explain each rule in beginner-friendly language.
Provide code examples where useful (ARIA, semantic HTML).
Keep accessibility practical and central to the design, not an afterthought.
```

---

### 8. IMPACT_MEASUREMENT.md
**Purpose:** To define how impact will be measured, tracked, and reported.
```text
You are a social impact measurement expert.
Using the PRD and Stakeholder Map below, create an Impact Measurement document for this social impact hackathon project.

PRD: [PASTE PRD]
STAKEHOLDER_MAP: [PASTE STAKEHOLDER_MAP]

Provide:
1. Theory of Change (Inputs → Activities → Outputs → Outcomes → Impact)
2. Key Impact Indicators (KPIs)
3. Quantitative metrics (Numbers, Percentages, Cost savings)
4. Qualitative metrics (Stories, Testimonials, Behavior change)
5. Data collection methods (Surveys, Interviews, Usage data)
6. Baseline and targets
7. Measurement frequency (Daily, Weekly, Monthly)
8. Reporting format (For judges, NGOs, Funders)
9. Data ethics in measurement (Consent, Anonymity)
10. A checklist for verifying impact measurement before the demo

Explain each metric in beginner-friendly language.
Keep the impact measurement simple and demonstrable within a hackathon timeframe.
Focus on metrics that can be shown live during the demo.
```

---

### 9. DATA_ETHICS.md
**Purpose:** To define ethical handling of vulnerable populations' data.
```text
You are a data ethics expert specializing in social impact.
Using the PRD and Stakeholder Map below, create a Data Ethics document for this social impact hackathon project.

PRD: [PASTE PRD]
STAKEHOLDER_MAP: [PASTE STAKEHOLDER_MAP]

Provide:
1. Ethical principles (Do no harm, Informed consent, Data minimization)
2. Vulnerable population considerations
3. Consent management (How is consent obtained and recorded?)
4. Data minimization (What data is NOT collected?)
5. Data anonymization and pseudonymization
6. Data storage and retention (How long? Where?)
7. Data sharing rules (Who can access what?)
8. Right to deletion and correction
9. Transparency (How is data use communicated?)
10. Bias and fairness considerations
11. A pre-submission data ethics checklist

Explain each principle in beginner-friendly language.
Keep the data ethics practical and enforceable within a hackathon timeframe.
Flag any ethical red flags that must be addressed.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define frontend design focused on inclusion and accessibility.
```text
Act as a senior UI/UX designer specializing in inclusive design.
Using the PRD, Architecture, and Accessibility Spec below, create a UI Specification document for a social impact hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
ACCESSIBILITY_SPEC: [PASTE ACCESSIBILITY_SPEC]

Provide:
1. Design system (Colors, typography, spacing)
2. Inclusive design patterns (Simple navigation, Clear language, Visual cues)
3. Component hierarchy
4. Screen-by-screen breakdown (Onboarding, Core feature, Help, Settings)
5. Low-bandwidth design (Minimal images, Fast loading)
6. Loading states
7. Error states (Simple, actionable errors)
8. Empty states
9. Multilingual and localization design
10. Responsive design guidelines (Mobile-first for low-end devices)
11. Accessibility considerations (WCAG 2.1 AA)

Keep the UI simple, clean, and accessible for a 24-48 hour hackathon.
Focus on demonstrating the core beneficiary journey.
Design for the lowest common denominator (low-end device, slow network, low literacy).
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when government APIs fail, data is missing, or users have low connectivity.
```text
You are a senior engineer specializing in civic tech.
Using the System Architecture and API Specification below, create an Error Handling document for a social impact hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. Common failure modes (Government API failures, Data missing, Low connectivity)
2. Government/NGO API error handling
3. Data validation errors
4. Offline error handling (Queue, Retry, Sync)
5. Low-bandwidth error handling (Reduce payload, Fallback to SMS/USSD)
6. Frontend error display (Simple, multilingual, actionable)
7. Fallback responses
8. Retry logic
9. Recovery procedures
10. A checklist for developers to verify error handling before the demo

Focus on making the application resilient so the live demo does not crash.
Ensure errors are understandable to non-technical users.
Explain each approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** To define data privacy for vulnerable populations, consent, and compliance.
```text
Act as a security and privacy engineer specializing in civic tech.
Using the System Architecture and Data Ethics document below, create a Security document for a social impact hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DATA_ETHICS: [PASTE DATA_ETHICS]

Provide:
1. Data classification (Sensitive, Personal, Public)
2. Encryption (At rest, In transit, Key management)
3. Authentication and authorization (Simple, accessible)
4. Consent management (How consent is stored and respected)
5. Data minimization (Only collect what is needed)
6. Anonymization and pseudonymization
7. Access control (Who can view what?)
8. Audit logging (Who accessed what, when)
9. Breach notification plan
10. Compliance (GDPR, Local data protection laws)
11. A pre-submission security and privacy checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
Prioritize the safety of vulnerable populations.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist including accessibility testing and community validation.
```text
Act as a QA engineer specializing in social impact applications.
Using the PRD and Accessibility Spec below, create a Testing document for a social impact hackathon project.

PRD: [PASTE PRD]
ACCESSIBILITY_SPEC: [PASTE ACCESSIBILITY_SPEC]

Provide:
1. Testing strategy for social impact applications
2. Functional testing (Core features)
3. Accessibility testing (Screen readers, Keyboard, Contrast)
4. Low-bandwidth testing (Slow network, Offline)
5. Low-end device testing
6. Multilingual testing
7. Integration testing (Government/NGO APIs)
8. Edge cases (Missing data, Vulnerable user scenarios)
9. Community validation (Testing with real users or proxies)
10. A manual testing checklist for the demo
11. How to document known limitations for judges

Keep the testing plan simple enough for beginner developers to execute under time pressure.
Prioritize accessibility and inclusion in all tests.
```

---

### 14. EVALUATION.md
**Purpose:** To define how you measure social impact and prepare for judge questions.
```text
You are a social impact evaluation expert.
Using the PRD and Impact Measurement document below, create an Evaluation document for a social impact hackathon project.

PRD: [PASTE PRD]
IMPACT_MEASUREMENT: [PASTE IMPACT_MEASUREMENT]

Provide:
1. Evaluation metrics (Lives improved, Access gained, Cost saved, Time saved)
2. Evaluation methods (Surveys, Interviews, Usage data, Case studies)
3. Benchmarking (What is the baseline social problem?)
4. Known limitations of the solution
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about social impact and how to answer them
8. Ethical considerations in evaluation (Do no harm)

Focus on demonstrating that the team understands the social problem, the community, and the impact.
Use real stories and data where possible.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To deploy with low-bandwidth, offline-first, and accessibility considerations.
```text
Act as a DevOps engineer specializing in civic tech.
Using the System Architecture and Accessibility Spec below, create a Deployment document for a social impact hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
ACCESSIBILITY_SPEC: [PASTE ACCESSIBILITY_SPEC]

Provide:
1. Deployment platforms (Free-tier, Low-cost, Scalable)
2. Low-bandwidth deployment considerations (CDN, Compression, Minimal assets)
3. Offline-first deployment (Service workers, PWA)
4. Accessibility considerations for deployment
5. Environment variables for production
6. Step-by-step deployment instructions
7. How to test the deployed application
8. Fallback plan if deployment fails during the hackathon
9. A pre-deployment accessibility and impact checklist
10. Common deployment mistakes in civic tech

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working, accessible live demo as early as possible.
Prioritize free and sustainable hosting.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation tailored to impact judges.
```text
Act as an expert hackathon presentation coach specializing in social impact.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
IMPACT_MEASUREMENT: [PASTE IMPACT_MEASUREMENT]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script for a social impact audience.
The presentation should follow:
1. Hook (A human story or statistic)
2. Problem (The social problem)
3. Why the problem matters
4. Existing limitations
5. Our solution
6. How it works (Highlight accessibility and inclusion)
7. Technology
8. Demo (The most important part — show real impact)
9. Impact (Stories, Numbers, Theory of Change)
10. Future scope (Scalability, Sustainability, Community ownership)
11. Closing (Call to action)

Make the language natural and easy to speak.
Avoid corporate jargon.
Write it as something a student can actually say on stage rather than something that sounds like an AI-generated report.
Focus on the human impact, not just the technology.
Also provide:
- 30-second elevator pitch
- 1-minute pitch
- 3-minute presentation
- 5-minute presentation
Include a backup plan for demo failure (video recording, screenshots, beneficiary testimonials).
```

---

### 17. GLOSSARY.md
**Purpose:** To define all civic and social impact terms so every team member can explain the project to judges without confusion.
```text
You are a technical writer specializing in civic tech.
Using the PRD, Impact Measurement, and Architecture below, create a Glossary document for a social impact hackathon project.

PRD: [PASTE PRD]
IMPACT_MEASUREMENT: [PASTE IMPACT_MEASUREMENT]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Social impact terms (Beneficiary, Theory of Change, Last-Mile, Digital Divide)
2. Civic tech terms (Open Data, GovTech, Civic Participation, Public Good)
3. Accessibility terms (WCAG, ARIA, Screen Reader, Assistive Tech)
4. NGO/Government terms (CSR, Grant, Policy, Stakeholder, M&E)
5. Data ethics terms (Consent, Anonymization, Data Minimization, Do No Harm)
6. Technical terms (Offline-first, PWA, Low-bandwidth)
7. Project-specific terms (Any custom terminology used in the PRD)
8. Acronyms and abbreviations

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

🔗 **[Link to Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)****

---
