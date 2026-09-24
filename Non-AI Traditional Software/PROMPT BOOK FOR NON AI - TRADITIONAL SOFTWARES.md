Based on our master taxonomy in `CATEGORIES.md`, the next logical category to tackle is:

# Category 02: Non-AI / Traditional Software

This is the perfect follow-up because it strips away the AI-specific complexities (like `AI_RULES`, `AI_MEMORY`, `EVIDENCE_MODEL`) and focuses purely on standard software engineering principles, which are the foundation of every hackathon.

Here is the exact list of documents we will prepare for the **Non-AI / Traditional Software** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core problem, target users, and existing gaps (No AI focus).
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for a standard web/mobile app.
3. **`TRD.md`** (Technical Requirements Document) — Defines the tech stack (e.g., MERN, PERN, Django), database choice, and latency limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Frontend, Backend, and Database (Client-Server architecture).
5. **`DATABASE_SCHEMA.md`** — Defines the database tables, fields, and relationships (SQL/NoSQL).
6. **`API_SPECIFICATION.md`** — Defines the REST/GraphQL endpoints for standard CRUD operations.
7. **`AUTHENTICATION_FLOW.md`** — (Replaces `AI_RULES.md`) Defines JWT, OAuth, session management, and password hashing.

### Phase 3: Execution, Quality & Security
8. **`UI_SPEC.md`** — Frontend design, components, and user flow.
9. **`ERROR_HANDLING.md`** — What happens when the database fails, APIs time out, or users input invalid data.
10. **`SECURITY.md`** — API key storage, user data privacy, SQL injection prevention, and XSS.
11. **`TESTING.md`** — QA plan, edge cases, and manual test checklists for standard features.
12. **`EVALUATION.md`** — How you measure if the software is performing well (Load time, bug rate).

### Phase 4: Delivery & Presentation (optional)
13. **`DEPLOYMENT.md`** — Hosting the frontend (Vercel/Netlify), backend (Render/Railway), and database (Supabase/MongoDB Atlas).
14. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
15. **`GLOSSARY.md`** — Definitions of technical terms (API, REST, JWT, ORM).

---
## PROMPTS FOR GENERATTING DOCUMENTATION 

---
## 1 Problem Analysis

I am participating in a software hackathon and I am a beginner developer.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing solutions
6. Proposed software solution ideas
7. Core features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential technologies that could be used (e.g., React, Node.js, PostgreSQL, etc.)

Do not assume I am an experienced developer. 
Explain all technical concepts in beginner-friendly language.
Do not suggest AI features unless absolutely necessary.

---
## 2 PRODUCT RESOURCE DOCUMENT  (PRD)

You are a senior product manager helping a beginner software hackathon team.
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
7. Product goals
8. User stories
9. Functional requirements (Include standard requirements: Authentication, CRUD operations, Search, Filters, Notifications)
10. Non-functional requirements (Performance, Scalability, Usability)
11. Core features
12. Nice-to-have features
13. User journeys
14. MVP scope
15. Out-of-scope features
16. Success metrics (Include standard metrics: User signups, task completion rate, load time)
17. Risks and assumptions

Keep the MVP realistic for a 24-48 hour hackathon. 
Do not add unnecessary features just to make the project sound impressive. 
Prioritize features that can actually be demonstrated live.
Do not include AI features unless explicitly required.

---
##  3 TECHNICAL RESOURE DOCUMENT (TRD)

You are a senior software engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Frontend requirements (Framework, state management, routing)
3. Backend requirements (Framework, authentication, business logic)
4. Database requirements (SQL vs NoSQL, justification)
5. API design approach (REST vs GraphQL)
6. Authentication and authorization requirements
7. Third-party integrations (Payment, Maps, Email, etc.)
8. Performance and latency requirements
9. Security and data privacy requirements
10. Testing requirements
11. Deployment requirements

Keep the technical stack simple and realistic for a 24-48 hour hackathon. 
Explain all technical concepts in beginner-friendly language.
Do not introduce unnecessary technologies.

---

## 4 SYSTEM ARCHITECTURE  

Act as a senior software architect.
Using the following PRD and TRD, design a realistic hackathon architecture for a standard software project.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended tech stack (Frontend, Backend, Database)
2. Frontend architecture
3. Backend architecture
4. Database architecture
5. Authentication flow
6. External APIs/services
7. Complete request/data flow diagram (Text-based)
8. Folder structure
9. Major components
10. Security considerations
11. Deployment architecture
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language. 
Do not introduce unnecessary technologies. Prefer a simple architecture that can be explained easily to judges.

---

## 5 DATABASE SCHEMA 

Act as a senior database engineer.
Using the PRD and System Architecture below, design the database schema for a software hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Tables (Users, Sessions, Core Entities, Lookup Tables)
2. Columns
3. Data types
4. Primary keys
5. Foreign keys
6. Relationships (One-to-Many, Many-to-Many)
7. Required fields
8. Optional fields
9. Indexes where useful
10. Example records
11. SQL schema

Explain why each table exists. 
Keep the database simple enough for a beginner hackathon team to understand and maintain.
Do not include AI-specific tables like Embeddings or PromptLogs.

---

## 6 API SPECIFICATION 

You are a senior backend developer.
Using the PRD, Architecture, and Database Schema below, create a complete REST API specification for a software hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DATABASE SCHEMA: [PASTE DATABASE_SCHEMA]

For every endpoint provide:
1. HTTP method (GET, POST, PUT, PATCH, DELETE)
2. URL
3. Purpose
4. Authentication requirement
5. Request parameters
6. Request body
7. Example request
8. Example success response
9. Possible error responses (400, 401, 403, 404, 500)
10. HTTP status codes

Keep the API simple and consistent. 
Do not create endpoints that are not required by the product.
Focus on standard CRUD operations for the core features.

---

## 7 AUTH FLOW 

You are a senior backend security engineer.
Using the PRD and System Architecture below, create an Authentication Flow document for a software hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Authentication method (JWT, Session-based, OAuth)
2. Password hashing strategy (bcrypt, argon2)
3. Registration flow (Step-by-step)
4. Login flow (Step-by-step)
5. Token management (Access token, Refresh token)
6. Role-based access control (Admin, User, Guest)
7. Password reset flow
8. Logout flow
9. Session expiry and handling
10. Third-party login options (Google, GitHub) if applicable
11. A developer checklist for implementing auth

Keep the authentication simple and secure enough for a hackathon. 
Explain concepts in beginner-friendly language.

---
## 8  UI SPEC 

Act as a senior UI/UX designer.
Using the PRD and System Architecture below, create a UI Specification document for a software hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spacing)
2. Component hierarchy (List all major components)
3. Screen-by-screen breakdown (Login, Dashboard, Core Feature, Settings)
4. Loading states (Skeletons, spinners)
5. Error states (How errors are displayed to the user)
6. Empty states (What the user sees before data is loaded)
7. Responsive design guidelines (Mobile and Desktop)
8. Accessibility considerations (Contrast, keyboard navigation)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon. 
Focus on demonstrating the core user journey.

---

## 9 ERROR HANDLING

You are a senior backend developer.
Using the System Architecture and API Specification below, create an Error Handling document for a software hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. API failure modes (Server errors, timeouts, network issues)
2. Fallback responses (What to show the user)
3. Frontend error display (Toasts, inline errors, modals)
4. Retry logic (Exponential backoff, maximum retries)
5. Validation errors (Empty fields, invalid formats)
6. Database connection errors
7. Authentication errors (Expired token, unauthorized access)
8. A checklist for developers to verify error handling before the demo

Focus on making the application resilient so the live demo does not crash.

---

## 10 SECURITY 

Act as a security engineer.
Using the System Architecture and API Specification below, create a Security document for a software hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. API key protection (Environment variables, backend-only access)
2. Authentication security (JWT, session management)
3. Input sanitization (Preventing SQL injection and XSS)
4. Data privacy (Ensuring user data is protected)
5. Database security (Row-level security, permissions)
6. CORS configuration
7. Rate limiting (Preventing abuse of endpoints)
8. HTTPS and secure headers
9. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.

---

##  11 TESTING 

Act as a QA engineer.
Using the PRD and API Specification below, create a Testing document for a software hackathon project.

PRD: [PASTE PRD]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. Testing strategy for core features
2. Edge cases for forms (Empty input, long input, invalid format)
3. API testing (Using Postman or similar tools)
4. Database testing (Data integrity, relationships)
5. Authentication testing (Register, login, logout, password reset)
6. User acceptance testing checklist
7. A manual testing checklist for the demo (Core Feature, UI, Navigation)
8. Cross-browser and responsive testing checklist

Keep the testing plan simple enough for beginner developers to execute under time pressure.

---
## 12 EVALUATION 

You are a software quality expert.
Using the PRD and Architecture below, create an Evaluation document for a software hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Evaluation metrics (Load time, bug rate, task completion rate)
2. Evaluation methods (Manual testing, user feedback)
3. Benchmarking (What is the baseline?)
4. Known limitations of the software
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about software performance and how to answer them

Focus on demonstrating that the team understands their software's capabilities and boundaries.

---
## Phase 4: Delivery & Presentation (OPTIONAL)

## 13 DEPLOYMENT 

Act as a DevOps engineer.
Using the System Architecture and API Specification below, create a Deployment document for a software hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. Deployment platforms (Frontend: Vercel/Netlify, Backend: Render/Railway, Database: Supabase/MongoDB Atlas)
2. Environment variables for production (Database URLs, API keys, JWT secrets)
3. Step-by-step deployment instructions for each component
4. How to test the deployed application
5. Fallback plan if deployment fails during the hackathon
6. A pre-deployment checklist
7. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon. 
Focus on getting a working live URL as early as possible.

---

## 14 DEMO SCRIPT 
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
FEATURES: [PASTE CORE FEATURES]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem
3. Why the problem matters
4. Existing limitations
5. Our solution
6. How it works (Include the architecture briefly)
7. Technology
8. Demo (The most important part)
9. Innovation
10. Impact
11. Future scope
12. Closing

Make the language natural and easy to speak.
Avoid corporate jargon.
Write it as something a student can actually say on stage rather than something that sounds like an AI-generated report.
Also provide:
- 30-second elevator pitch
- 1-minute pitch
- 3-minute presentation
- 5-minute presentation
  
___

##  15 GLOSSARY 

You are a technical writer.
Using the PRD, API Specification, and Architecture below, create a Glossary document for a software hackathon project.

PRD: [PASTE PRD]
API_SPEC: [PASTE API_SPECIFICATION]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Web development terms (API, REST, CRUD, JWT, ORM, MVC)
2. Database terms (SQL, NoSQL, Primary Key, Foreign Key, Index)
3. Frontend terms (Component, State, Props, Routing, SPA)
4. Backend terms (Middleware, Controller, Service, Environment Variables)
5. Deployment terms (CI/CD, Hosting, Domain, SSL)
6. Project-specific terms (Any custom terminology used in the PRD)
7. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable for a beginner audience. 
This will help all team members speak confidently to judges.

---
Thank you for using this guide. Go build something amazing!

**Made by Siddiq

*Credit: Hackathon Alechemy Folder — AI/ML Category*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alechemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**