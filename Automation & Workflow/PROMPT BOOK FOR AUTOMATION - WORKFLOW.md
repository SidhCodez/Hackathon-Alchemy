# Category 03: Automation & Workflow (n8n / Make)

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the problem and identify what manual, repetitive, or disconnected processes need automation.
```text
I am participating in an automation-focused hackathon (using tools like n8n, Make, or Zapier) and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. Existing ways people might solve this problem manually
5. Limitations of existing manual or semi-automated solutions
6. Proposed automation solution ideas
7. Core automation features
8. Nice-to-have automation features
9. What should NOT be built during a short hackathon
10. What could make this automation unique
11. A realistic MVP workflow that can be built during a hackathon
12. Potential tools and platforms that could be used (n8n, Make, Zapier, Airtable, Google Sheets, etc.)

Do not assume I am an experienced developer.
Explain automation concepts (triggers, actions, webhooks, nodes) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear automation plan with triggers, actions, and workflow scope.
```text
You are a senior automation product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed automation solution
7. Product goals
8. User stories
9. Functional requirements (Include automation-specific requirements: Triggers, Actions, Conditions, Data Transformations)
10. Non-functional requirements (Reliability, Speed, Error tolerance)
11. Core automation workflows
12. Nice-to-have workflows
13. User journeys (Manual step → Automated step)
14. MVP scope (Which workflow must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include automation metrics: Time saved, Manual steps reduced, Error rate)
17. Risks and assumptions (Include automation risks: API rate limits, Broken webhooks, Third-party downtime)

Keep the MVP realistic for a 24-48 hour automation hackathon.
Do not add unnecessary workflows just to make the project sound impressive.
Prioritize automations that can actually be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on platform choice, triggers, actions, and integrations.
```text
You are a senior automation engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Automation platform choice (n8n vs Make vs Zapier — justify the choice)
3. Trigger requirements (Webhook, Schedule, App Event, Manual)
4. Action node requirements (What each node does)
5. Data transformation requirements (Formatting, Mapping, Filtering)
6. Conditional logic requirements (If/Else, Switch, Loops)
7. External service integrations (Google Sheets, Slack, Gmail, Airtable, etc.)
8. API and webhook requirements
9. Error handling and retry requirements
10. Credential and secret management
11. Performance and execution time limits
12. Testing requirements

Keep the automation stack simple and realistic for a 24-48 hour hackathon.
Explain all automation concepts in beginner-friendly language.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design the automation workflow architecture with clear triggers, actions, and data flow.
```text
Act as a senior automation architect.
Using the following PRD and TRD, design a realistic hackathon automation architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended automation platform (n8n, Make, or Zapier)
2. Complete workflow diagram (Text-based, showing Trigger → Nodes → Output)
3. Trigger architecture (What starts the workflow?)
4. Action architecture (What happens step by step?)
5. Data flow (How data moves between nodes)
6. Conditional logic and branching
7. External service connections (APIs, Webhooks, Databases)
8. Database or storage choice if needed (Google Sheets, Airtable, Supabase)
9. Credential and authentication approach
10. Error handling and retry architecture
11. Folder/Workflow organization
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools. Prefer a simple workflow that can be explained easily to judges.
```

---

### 5. WORKFLOW_SCHEMA.md
**Purpose:** To define the exact node-by-node structure of each automation workflow.
```text
Act as a senior automation engineer.
Using the PRD and System Architecture below, design the complete workflow schema for this automation hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

For each core workflow, provide:
1. Workflow name
2. Trigger type (Webhook, Schedule, App Event, Manual)
3. Trigger configuration
4. Node-by-node breakdown (Node name, Type, Purpose, Configuration)
5. Data mapping between nodes
6. Conditional logic (Filters, If/Else, Switch)
7. Error handling per node (Continue on fail, Retry, Stop)
8. Output destination (Email, Database, Slack, etc.)
9. Example input data
10. Example output data
11. Execution time estimate

Explain why each node exists.
Keep the workflow simple enough for a beginner hackathon team to understand and maintain.
```

---

### 6. API_INTEGRATION.md
**Purpose:** To define all external APIs and webhooks used in the automation.
```text
You are a senior integration engineer.
Using the PRD and Workflow Schema below, create a complete API Integration document for this automation hackathon project.

PRD: [PASTE PRD]
WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]

For every external service and API, provide:
1. Service name (Google Sheets, Slack, Gmail, OpenAI, etc.)
2. Purpose in the workflow
3. Authentication method (API Key, OAuth, Webhook URL)
4. Required credentials and where to store them
5. Endpoint or Webhook URL used
6. Request format (Headers, Body, Parameters)
7. Example request
8. Example response
9. Rate limits (If any)
10. Error responses and handling
11. Fallback if the service is down

Keep the integrations simple and realistic for a hackathon.
Do not include services that are not required by the product.
```

---

### 7. NODE_LOGIC.md
**Purpose:** To define the logic, conditions, and data transformations inside each node.
```text
Act as a senior automation logic designer.
Using the Workflow Schema and PRD below, create the Node Logic document for this automation hackathon project.

WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]
PRD: [PASTE PRD]

Provide:
1. Data transformation rules (Formatting, Parsing, Merging)
2. Conditional logic rules (If/Else, Switch, Filters)
3. Loop and iteration logic
4. Variable and expression usage
5. Date/Time formatting rules
6. Text manipulation rules (Split, Replace, Trim)
7. Number and currency formatting rules
8. Error handling logic per node
9. Edge cases for each node (Empty data, Missing fields, Invalid formats)
10. A checklist for developers to verify node logic before the demo

Explain every logic rule in beginner-friendly language.
Keep the logic simple and easy to debug.
```

---

### 8. TRIGGER_MAP.md
**Purpose:** To define how each workflow is triggered and under what conditions.
```text
You are an automation trigger specialist.
Using the PRD and Workflow Schema below, create a Trigger Map document for this automation hackathon project.

PRD: [PASTE PRD]
WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]

For each workflow, provide:
1. Workflow name
2. Trigger type (Webhook, Schedule, App Event, Manual)
3. Trigger source (Form submission, Email received, New row in Sheet, etc.)
4. Trigger configuration details
5. Trigger frequency or schedule (If applicable)
6. Trigger payload structure (What data comes in?)
7. Example trigger event
8. Conditions that must be met for the trigger to fire
9. What happens if the trigger fails
10. How to manually test the trigger

Explain each trigger in beginner-friendly language.
Keep the triggers simple and easy to demonstrate live.
```

---

### 9. CREDENTIAL_MANAGEMENT.md
**Purpose:** To securely manage API keys, webhooks, and credentials for the automation.
```text
Act as a security-conscious automation engineer.
Using the Workflow Schema and API Integration document below, create a Credential Management document for this automation hackathon project.

WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]
API_INTEGRATION: [PASTE API_INTEGRATION]

Provide:
1. List of all credentials required (API keys, tokens, webhook URLs)
2. Where each credential is stored (Platform vault, .env file, Environment variables)
3. How to securely share credentials with team members
4. How to rotate credentials if compromised
5. What NEVER to commit to GitHub
6. How to use n8n/Make credential vaults properly
7. Fallback if a credential expires during the demo
8. A pre-submission credential checklist

Keep the credential management simple but secure enough for a hackathon.
Explain concepts in beginner-friendly language.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define the user-facing interface (forms, dashboards, or trigger points) that interacts with the automation.
```text
Act as a senior UI/UX designer.
Using the PRD and System Architecture below, create a UI Specification document for an automation hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spacing)
2. Component hierarchy (Forms, Dashboards, Status Cards)
3. Screen-by-screen breakdown (Trigger Form, Status Dashboard, Logs View)
4. Loading states (For automation triggers)
5. Success states (What the user sees when the automation runs)
6. Error states (What the user sees when the automation fails)
7. Empty states (Before any automation has run)
8. Responsive design guidelines (Mobile and Desktop)
9. Accessibility considerations

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the automation trigger and result.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when a node fails, an API times out, or credentials expire.
```text
You are a senior automation engineer.
Using the Workflow Schema and API Integration document below, create an Error Handling document for this automation hackathon project.

WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]
API_INTEGRATION: [PASTE API_INTEGRATION]

Provide:
1. Common failure modes (API timeouts, Rate limits, Invalid credentials, Missing data)
2. Node-level error handling (Continue on fail, Retry, Stop workflow)
3. Retry logic (Exponential backoff, Maximum retries)
4. Fallback responses (What to do if a critical node fails)
5. Notification strategy (Email, Slack alert when a workflow fails)
6. Error logging (Where errors are stored)
7. Frontend error display (If applicable)
8. A checklist for developers to verify error handling before the demo

Focus on making the automation resilient so the live demo does not crash.
```

---

### 12. SECURITY.md
**Purpose:** To secure webhooks, API keys, and user data flowing through the automation.
```text
Act as a security engineer.
Using the Workflow Schema and API Integration document below, create a Security document for an automation hackathon project.

WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]
API_INTEGRATION: [PASTE API_INTEGRATION]

Provide:
1. Webhook security (Secret tokens, IP whitelisting)
2. API key protection (Vault storage, Environment variables)
3. Authentication for external services (OAuth best practices)
4. Input sanitization (Preventing injection through forms)
5. Data privacy (What data flows through the automation?)
6. Access control (Who can edit the workflow?)
7. Logging and monitoring for suspicious activity
8. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist for automation workflows and edge cases.
```text
Act as a QA engineer specializing in automation workflows.
Using the PRD and Workflow Schema below, create a Testing document for an automation hackathon project.

PRD: [PASTE PRD]
WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]

Provide:
1. Testing strategy for automation workflows
2. Trigger testing (Does the workflow start correctly?)
3. Node testing (Does each node produce the correct output?)
4. Data transformation testing (Is data mapped correctly?)
5. Error case testing (Missing data, API failures)
6. End-to-end workflow testing
7. User acceptance testing checklist
8. A manual testing checklist for the demo
9. How to document known automation limitations for judges

Keep the testing plan simple enough for beginner developers to execute under time pressure.
```

---

### 14. EVALUATION.md
**Purpose:** To define how the team measures automation performance and prepares for judge questions.
```text
You are an automation evaluation expert.
Using the PRD and Workflow Schema below, create an Evaluation document for an automation hackathon project.

PRD: [PASTE PRD]
WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]

Provide:
1. Evaluation metrics (Time saved, Manual steps reduced, Error rate, Execution time)
2. Evaluation methods (Before vs After comparison, Manual timing)
3. Benchmarking (What is the baseline manual process?)
4. Known limitations of the automation
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about automation and how to answer them

Focus on demonstrating that the team understands the automation's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To define how to activate, publish, and share the automation workflow for the live demo.
```text
Act as a DevOps engineer.
Using the System Architecture and Workflow Schema below, create a Deployment document for an automation hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]

Provide:
1. Deployment approach (Activate workflow, Publish, Share link)
2. Environment variables and credentials for production
3. Step-by-step activation instructions for each workflow
4. How to test the live workflow
5. Fallback plan if the workflow fails during the hackathon
6. How to share the workflow with judges or users
7. A pre-deployment checklist
8. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working live automation as early as possible.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the automation is shown off perfectly.
```text
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
WORKFLOWS: [PASTE CORE WORKFLOWS]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem (Manual, repetitive, error-prone process)
3. Why the problem matters
4. Existing limitations
5. Our automation solution
6. How it works (Trigger → Nodes → Output)
7. Technology (n8n/Make, APIs used)
8. Demo (The most important part — show the trigger and the automated result)
9. Innovation
10. Impact (Time saved, Errors reduced)
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
```

---

### 17. GLOSSARY.md
**Purpose:** To define all automation terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Workflow Schema, and API Integration document below, create a Glossary document for an automation hackathon project.

PRD: [PASTE PRD]
WORKFLOW_SCHEMA: [PASTE WORKFLOW_SCHEMA]
API_INTEGRATION: [PASTE API_INTEGRATION]

Provide definitions for all key terms used in the project, including:
1. Automation terms (Trigger, Action, Node, Workflow, Webhook, Schedule)
2. Integration terms (API, Endpoint, OAuth, API Key, Rate Limit)
3. Data terms (Payload, JSON, Mapping, Transformation, Filter)
4. Platform-specific terms (n8n Node, Make Module, Zapier Zap)
5. Conditional logic terms (If/Else, Switch, Loop, Branch)
6. Error handling terms (Retry, Fallback, Timeout)
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
### Thank You

Thank you for using this guide. Go build something amazing!

**Made by Siddiq

*Credit: Hackathon Alechemy 

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alechemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**