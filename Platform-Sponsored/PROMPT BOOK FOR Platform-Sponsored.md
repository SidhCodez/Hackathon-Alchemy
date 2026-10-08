# Category 16: Platform-Sponsored

This category focuses on building solutions specifically for a sponsor's ecosystem using platforms like **OpenAI, AWS, Google Cloud, Microsoft Azure, Stripe, Twilio, n8n, Make, Ethereum, or Vercel**. It focuses purely on **leveraging the sponsor's APIs, SDKs, credits, and ecosystem** — the foundation of every platform-sponsored hackathon.

Here is the exact list of documents we will prepare for the **Platform-Sponsored** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PLATFORM_ANALYSIS.md`** — Defines the sponsor's platform, capabilities, limits, and hackathon requirements.
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and sponsor-aligned metrics.
3. **`TRD.md`** (Technical Requirements Document) — Defines the sponsor's SDKs, APIs, quotas, and integration limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level architecture built around the sponsor's platform.
5. **`PLATFORM_INTEGRATION.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines how the sponsor's services are integrated.
6. **`API_SPECIFICATION.md`** — Defines endpoints including the sponsor's specific APIs.
7. **`SDK_USAGE.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines which SDKs are used, why, and how.
8. **`QUOTA_MANAGEMENT.md`** — Defines API rate limits, credits, and budget management.
9. **`SANDBOX_SPEC.md`** — Defines the sandbox/test environment provided by the sponsor.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Frontend design leveraging the sponsor's UI components (if provided).
11. **`ERROR_HANDLING.md`** — What happens when the sponsor's API fails, quotas are hit, or credits run out.
12. **`SECURITY.md`** — Protecting the sponsor's API keys, tokens, and user data.
13. **`TESTING.md`** — QA plan including sponsor's sandbox and edge cases.
14. **`EVALUATION.md`** — How you measure success using the sponsor's metrics (Usage, Credits, Impact).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Deployment using the sponsor's recommended hosting (Vercel, AWS, etc.).
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation tailored to sponsor judges.
17. **`GLOSSARY.md`** — Definitions of the sponsor's specific terms, APIs, and acronyms.

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PLATFORM_ANALYSIS.md
**Purpose:** To deeply understand the sponsor's platform, its capabilities, and the hackathon's requirements.
```text
I am participating in a platform-sponsored hackathon where [SPONSOR NAME] is the main sponsor. I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. The sponsor's platform and its core capabilities
5. What the sponsor wants participants to build (Hackathon requirements)
6. Proposed solution ideas using the sponsor's platform
7. Core features leveraging the sponsor's APIs/SDKs
8. Nice-to-have features
9. What should NOT be built (Avoid using competitor tools)
10. What could make this solution unique within the sponsor's ecosystem
11. A realistic MVP that can be built during a hackathon
12. The sponsor's specific APIs, SDKs, and tools that could be used

Do not assume I am an expert in the sponsor's platform.
Explain the sponsor's tools and concepts in beginner-friendly language.
Highlight any specific hackathon prizes, credits, or judging criteria mentioned by the sponsor.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear plan aligned with the sponsor's goals.
```text
You are a senior product manager specializing in [SPONSOR NAME]'s ecosystem, helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed solution
7. Product goals (Aligned with sponsor's goals)
8. User stories
9. Functional requirements (Include sponsor-specific API/SDK requirements)
10. Non-functional requirements (Quotas, Latency, Cost)
11. Core features (Maximize sponsor's tools)
12. Nice-to-have features
13. User journeys
14. MVP scope (Which feature must work during the demo?)
15. Out-of-scope features (Explicitly avoid competitor tools)
16. Success metrics (Include sponsor-aligned metrics: Usage, Impact, Innovation)
17. Risks and assumptions (Include sponsor API limits, Credits, Downtime)

Keep the MVP realistic for a 24-48 hour hackathon.
Do not add unnecessary features just to make the project sound impressive.
Prioritize features that directly use the sponsor's platform and can be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on the sponsor's SDKs and APIs.
```text
You are a senior engineer specializing in [SPONSOR NAME]'s platform, helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Sponsor platform integration strategy
3. Sponsor SDKs and APIs required (List them all)
4. Authentication and authorization using sponsor's tools
5. Data storage and management using sponsor's services
6. Rate limits, quotas, and credits management
7. Sponsor-specific performance requirements
8. Security and compliance requirements
9. Testing requirements using sponsor's sandbox
10. Deployment using sponsor's recommended platforms
11. Fallback if sponsor's API is down
12. Budget and cost estimation (Using sponsor credits)

Keep the tech stack centered on the sponsor's ecosystem.
Explain all sponsor-specific concepts in beginner-friendly language.
Do not introduce unnecessary competitor tools.
Flag any integration challenges early.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic architecture built around the sponsor's platform.
```text
Act as a senior architect specializing in [SPONSOR NAME]'s ecosystem.
Using the following PRD and TRD, design a realistic hackathon architecture for this sponsor-focused project.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended sponsor tech stack (Frontend, Backend, Sponsor APIs)
2. Complete architecture diagram (Text-based, showing Users → Frontend → Backend → Sponsor APIs → Database)
3. Frontend architecture
4. Backend architecture
5. Sponsor API integration architecture
6. Data storage architecture (Sponsor's DB or preferred tool)
7. Authentication architecture (Sponsor's auth tools)
8. Data flow (How a user action triggers sponsor APIs)
9. Security and quota considerations
10. Folder structure
11. Major components
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce competitor tools. Stick to the sponsor's ecosystem.
Highlight how the architecture maximizes the use of the sponsor's platform.
```

---

### 5. PLATFORM_INTEGRATION.md
**Purpose:** To define how the sponsor's services are integrated.
```text
Act as a senior integration engineer specializing in [SPONSOR NAME].
Using the PRD and System Architecture below, create a Platform Integration document for this sponsor hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

For each sponsor service integrated, provide:
1. Service name (API, SDK, Tool)
2. Purpose in the project
3. Authentication method (API Key, OAuth, Service Account)
4. Required credentials and where to store them
5. Endpoint or SDK method used
6. Request/Response format
7. Example usage (Copy-paste ready)
8. Rate limits and quotas
9. Error handling
10. Fallback if the service is unavailable

Keep the integrations strictly within the sponsor's ecosystem.
Explain why each service was chosen.
Keep the integration simple and realistic for a hackathon.
Highlight how this maximizes the sponsor's technology.
```

---

### 6. API_SPECIFICATION.md
**Purpose:** To define endpoints including the sponsor's specific APIs.
```text
You are a senior backend developer specializing in [SPONSOR NAME]'s APIs.
Using the PRD, Architecture, and Platform Integration below, create a complete API specification for this sponsor hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

For every endpoint provide:
1. HTTP method
2. URL
3. Purpose
4. Authentication requirement (Using sponsor's auth)
5. Sponsor API used (If any)
6. Request parameters
7. Request body
8. Example request
9. Example success response
10. Possible error responses (Include sponsor-specific errors like 429 Rate Limit)
11. HTTP status codes
12. Quota and rate limit considerations

Keep the API simple and consistent.
Ensure all endpoints align with the sponsor's ecosystem.
Do not create endpoints that use competitor tools.
Prioritize showcasing the sponsor's APIs.
```

---

### 7. SDK_USAGE.md
**Purpose:** To define which sponsor SDKs are used, why, and how.
```text
You are a senior developer specializing in [SPONSOR NAME] SDKs.
Using the PRD and Platform Integration document below, create an SDK Usage document for this sponsor hackathon project.

PRD: [PASTE PRD]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

Provide:
1. List of sponsor SDKs used (Frontend, Backend, Mobile)
2. Why each SDK was chosen
3. Installation instructions for each SDK
4. Configuration and setup
5. Key methods and functions used
6. Example code snippets (Copy-paste ready)
7. Common pitfalls and how to avoid them
8. SDK version requirements
9. Compatibility with other tools
10. Fallback if the SDK is unavailable
11. A checklist for verifying SDK usage before the demo

Explain each SDK in beginner-friendly language.
Keep the SDK usage simple and strictly within the sponsor's ecosystem.
Highlight how the SDKs accelerate development.
```

---

### 8. QUOTA_MANAGEMENT.md
**Purpose:** To define API rate limits, credits, and budget management.
```text
Act as a senior engineer managing [SPONSOR NAME]'s quotas and credits.
Using the Platform Integration and PRD below, create a Quota Management document for this sponsor hackathon project.

PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]
PRD: [PASTE PRD]

Provide:
1. List of all sponsor APIs and their rate limits
2. Available credits provided by the sponsor
3. Estimated usage per feature
4. Total estimated credits required for the demo
5. Strategy to stay within limits (Caching, Batching, Throttling)
6. What happens when quotas are exceeded
7. Fallback mechanisms (Cached responses, Degraded features)
8. How to monitor usage (Sponsor dashboards)
9. How to request additional credits (If needed)
10. A checklist for verifying quota management before the demo

Explain each concept in beginner-friendly language.
Ensure the demo does not fail due to exceeded quotas.
Keep the strategy simple and realistic for a hackathon.
```

---

### 9. SANDBOX_SPEC.md
**Purpose:** To define the sandbox/test environment provided by the sponsor.
```text
You are a senior developer using [SPONSOR NAME]'s sandbox environment.
Using the PRD and Platform Integration document below, create a Sandbox Specification document for this sponsor hackathon project.

PRD: [PASTE PRD]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

Provide:
1. Sponsor's sandbox environment details
2. How to access the sandbox
3. Sandbox vs Production differences
4. Sandbox credentials and setup
5. Limitations of the sandbox
6. How to test sponsor APIs in the sandbox
7. Mock data and test accounts
8. How to transition from sandbox to production
9. Common sandbox mistakes and how to avoid them
10. A checklist for verifying sandbox usage before the demo

Explain each concept in beginner-friendly language.
Focus on testing the sponsor's APIs thoroughly before the demo.
Keep the sandbox setup simple and realistic for a hackathon.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define frontend design leveraging the sponsor's UI components (if provided).
```text
Act as a senior UI/UX designer specializing in [SPONSOR NAME]'s design system.
Using the PRD and System Architecture below, create a UI Specification document for a sponsor hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Use sponsor's design tokens if provided)
2. Sponsor UI components (If any: Buttons, Modals, Cards)
3. Component hierarchy
4. Screen-by-screen breakdown (Dashboard, Core feature, Settings)
5. Loading states (For sponsor API calls)
6. Error states (Sponsor API errors)
7. Empty states
8. Responsive design guidelines
9. Accessibility considerations (WCAG, Sponsor standards)

Keep the UI simple, clean, and aligned with the sponsor's brand.
Focus on demonstrating the core sponsor-powered journey.
If the sponsor provides a UI kit, use it. Otherwise, design a simple, modern UI.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when the sponsor's API fails, quotas are hit, or credits run out.
```text
You are a senior engineer specializing in [SPONSOR NAME]'s platform.
Using the System Architecture and Platform Integration document below, create an Error Handling document for a sponsor hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

Provide:
1. Common failure modes (Sponsor API failures, Quota exceeded, Credit exhausted)
2. Sponsor API error codes and meanings
3. Rate limit handling (Backoff, Retry)
4. Quota exhaustion handling (Fallback, Cached responses)
5. Credit exhaustion handling (Notify, Degrade gracefully)
6. Authentication errors (Expired tokens, Invalid keys)
7. Frontend error display
8. Fallback responses
9. Audit logging of errors
10. A checklist for developers to verify error handling before the demo

Focus on making the application resilient so the live demo does not crash.
Prioritize staying within the sponsor's limits.
Explain each approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** To protect the sponsor's API keys, tokens, and user data.
```text
Act as a security engineer specializing in [SPONSOR NAME]'s platform.
Using the System Architecture and Platform Integration document below, create a Security document for a sponsor hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

Provide:
1. Sponsor API key protection (Environment variables, Secret managers)
2. Authentication security (Sponsor's auth best practices)
3. Token management (Expiry, Refresh, Revocation)
4. Data privacy (User data handled by sponsor's services)
5. Access control (Who can access what?)
6. API security (Rate limiting, Input validation)
7. Logging and monitoring (Sponsor dashboards)
8. Incident response (If credentials are leaked)
9. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
Flag any security measures that are mandatory for the sponsor's platform.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist including the sponsor's sandbox and edge cases.
```text
Act as a QA engineer specializing in [SPONSOR NAME]'s platform.
Using the PRD and Platform Integration document below, create a Testing document for a sponsor hackathon project.

PRD: [PASTE PRD]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

Provide:
1. Testing strategy for sponsor-integrated applications
2. Sponsor sandbox testing
3. Functional testing (Core features using sponsor APIs)
4. Integration testing (Sponsor SDKs, APIs)
5. Quota and rate limit testing
6. Error case testing (API down, Quota exceeded)
7. User acceptance testing checklist
8. A manual testing checklist for the demo
9. How to document known sponsor-related limitations for judges

Keep the testing plan simple enough for beginner developers to execute under time pressure.
Prioritize testing the sponsor's APIs thoroughly.
```

---

### 14. EVALUATION.md
**Purpose:** To define how you measure success using the sponsor's metrics.
```text
You are a sponsor-aligned evaluation expert.
Using the PRD and Platform Integration document below, create an Evaluation document for a sponsor hackathon project.

PRD: [PASTE PRD]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

Provide:
1. Evaluation metrics (Sponsor API usage, Credits consumed, User impact)
2. Sponsor-specific metrics (If any provided by the sponsor)
3. Evaluation methods (Usage data, Benchmarking, Feedback)
4. Benchmarking (What is the baseline?)
5. Known limitations of the solution
6. How to explain these limitations to sponsor judges honestly
7. A checklist of evidence to gather for the presentation (Sponsor dashboards, Logs)
8. Common sponsor judge questions and how to answer them

Focus on demonstrating that the team maximized the sponsor's platform.
Highlight innovation within the sponsor's ecosystem.
Use hard numbers from sponsor dashboards where possible.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To deploy using the sponsor's recommended hosting (Vercel, AWS, etc.).
```text
Act as a DevOps engineer specializing in [SPONSOR NAME]'s deployment.
Using the System Architecture and Platform Integration document below, create a Deployment document for a sponsor hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]

Provide:
1. Sponsor-recommended hosting platforms
2. Sponsor-specific deployment steps
3. Environment variables for production
4. Secrets management using sponsor tools
5. Step-by-step deployment instructions
6. How to test the deployed application
7. Monitoring using sponsor dashboards
8. Fallback plan if deployment fails during the hackathon
9. A pre-deployment sponsor checklist
10. Common deployment mistakes

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Ensure deployment maximizes the sponsor's platform (e.g., Vercel for Next.js, AWS for AWS-sponsored).
Focus on getting a working live demo as early as possible.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation tailored to sponsor judges.
```text
Act as an expert hackathon presentation coach specializing in [SPONSOR NAME]'s ecosystem.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script for sponsor judges.
The presentation should follow:
1. Hook (The problem)
2. Problem
3. Why the problem matters
4. Our solution
5. How it works (Highlight the sponsor's platform)
6. Technology (Sponsor's SDKs, APIs)
7. Demo (The most important part — show sponsor-powered features)
8. Innovation within the sponsor's ecosystem
9. Impact
10. Future scope using the sponsor's tools
11. Closing

Make the language natural and easy to speak.
Avoid corporate jargon.
Write it as something a student can actually say on stage rather than something that sounds like an AI-generated report.
Highlight how the solution maximizes the sponsor's platform.
Also provide:
- 30-second elevator pitch
- 1-minute pitch
- 3-minute presentation
- 5-minute presentation
Include a backup plan for demo failure (video recording, screenshots, sponsor dashboard screenshots).
```

---

### 17. GLOSSARY.md
**Purpose:** To define the sponsor's specific terms, APIs, and acronyms.
```text
You are a technical writer specializing in [SPONSOR NAME]'s platform.
Using the PRD, Platform Integration, and Architecture below, create a Glossary document for a sponsor hackathon project.

PRD: [PASTE PRD]
PLATFORM_INTEGRATION: [PASTE PLATFORM_INTEGRATION]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Sponsor platform terms (APIs, SDKs, Services)
2. Sponsor-specific features (Functions, Tools, Dashboards)
3. Sponsor pricing terms (Credits, Quotas, Rate Limits)
4. Sponsor authentication terms (Tokens, Keys, OAuth)
5. Project-specific terms
6. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable for a beginner audience.
This will help all team members speak confidently to sponsor judges.
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

---