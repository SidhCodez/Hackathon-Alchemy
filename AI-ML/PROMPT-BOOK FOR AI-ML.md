# Category 01: AI / ML Hackathons
#AI  #LLMs 
## Phase 1: Problem Definition & Strategy
*Focuses on understanding the problem and defining the product without getting lost in the tech.*

1. **`PROBLEM_ANALYSIS.md`** — Defines the core problem, target users, and existing gaps. *Necessary to ensure the AI is actually solving a real problem, not just being used for the sake of it.*
2. **`PRD.md` (Product Requirements Document)** — Outlines features, user stories, MVP scope, and success metrics. *Necessary to define AI-specific metrics (e.g., accuracy, hallucination rate) and keep the scope tight for the hackathon.*
3. **`TRD.md` (Technical Requirements Document)** — Defines the tech stack, model selection (GPT-4, Claude, Llama), latency limits, and token budgeting. *Necessary to prevent the team from blowing their API budget or hitting rate limits during the demo.*

## Phase 2: Technical Blueprint & AI Core
*Focuses on how the AI actually works and how data flows through the system.*

4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Frontend, Backend, AI Service, and Database. *Necessary to show how the user request reaches the AI model and returns a response.*
5. **`DATA_MODEL.md`** — Defines the database tables, fields, and relationships. *Necessary for storing user data, chat history, and metadata.*
6. **`API_SPECIFICATION.md`** — Defines the REST/GraphQL endpoints. *Necessary to standardize how the frontend talks to the backend (e.g., `POST /api/chat`, `GET /api/history`).*
7. **`AI_RULES.md`** — System prompts, persona guidelines, tone, and guardrails. *Crucial for AI hackathons to prevent the model from going off-topic, hallucinating, or saying inappropriate things during judging.*
8. **`AI_MEMORY.md`** — Context window management, short-term vs. long-term memory. *Necessary to explain how the AI remembers previous user interactions.*
9. **`PROMPT_LIBRARY.md`** — The exact prompts used for different features (e.g., summarization, extraction, classification). *Necessary for version control and team collaboration on prompts.*
10. **`CACHE_SCHEMA.md`** — Strategy for caching AI responses (e.g., Redis or Semantic Cache). *Necessary to reduce latency and save API costs during the live demo.*
11. **`EVIDENCE_MODEL.md`** — How the AI grounds its answers (RAG, citations, source tracking). *Necessary if using RAG to prove the AI isn't making things up.*
12. **`DATABASE SCHEMA.md`** — HOW  the data keys has to be defined 

## Phase 3: Execution, Quality & Security
*Focuses on building, testing, and securing the AI application.*

12. **`UI_SPEC.md`** — Frontend design, components, and user flow. *Necessary to ensure the UI handles loading states and streaming responses properly.*
13. **`ERROR_HANDLING.md`** — What happens when the AI API fails, times out, or returns bad JSON. *Necessary for a smooth demo when the internet inevitably drops.*
14. **`SECURITY.md`** — API key storage, user data privacy, and prompt injection prevention. *Necessary to ensure `.env` files are ignored and user data isn't leaked to the AI.*
15. **`TESTING.md`** — QA plan, edge cases, and manual test checklists. *Necessary to test for hallucinations and edge cases (e.g., empty prompts, malicious inputs).*
16. **`EVALUATION.md`** — How you measure if the AI is performing well. *Necessary for judges who ask, "How do you know your AI is accurate?"*

## Phase 4: Delivery & Presentation (optional)
*Focuses on shipping the project and winning the hackathon.*

17. **`DEPLOYMENT.md`** — Hosting the frontend, backend, and managing production environment variables. *Necessary to get a live URL working early.*
18. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation. *Necessary to ensure the AI features are shown off perfectly within the time limit.*
19. **`GLOSSARY.md`** — Definitions of AI terms (RAG, Tokens, Temperature, Embeddings). *Necessary so every team member can explain the tech to judges without confusion.* 

---
### PROMPTS FOR GENERATING DOCUMENTS

----

###  1 PROBLEM_ANALYSIS

**Purpose:** To deeply understand the problem before writing any code
I am participating in an AI/ML hackathon and I am a beginner developer.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing solutions
6. Proposed AI/ML solution ideas
7. Core AI features
8. Nice-to-have AI features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential AI technologies that could be used (e.g., LLMs, RAG, Vision, etc.)

Do not assume I am an experienced developer. 
Explain all AI/ML technical concepts in beginner-friendly language.

--------------------------------------------------------------------------
## 2 PRD (Product Requirements Document)
You are a senior product manager helping a beginner AI/ML hackathon team.
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
9. Functional requirements (Include AI-specific requirements: Model selection, prompt handling, streaming, and latency limits)
10. Non-functional requirements
11. Core features
12. Nice-to-have features
13. User journeys
14. MVP scope
15. Out-of-scope features
16. Success metrics (Include AI metrics: Accuracy, hallucination rate, token usage, response time)
17. Risks and assumptions (Include AI risks: API rate limits, bad model outputs, downtime)

Keep the MVP realistic for a 24-48 hour AI hackathon. 
Do not add unnecessary AI features just to make the project sound impressive. 
Prioritize features that can actually be demonstrated live.

-------------------------------------------------------------------------
## 3 TRD (Technical Requirements Document)

You are a senior AI engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. AI model requirements (Which model? e.g., GPT-4o, Claude 3.5. Why? Context window size, temperature)
3. Prompt management strategy (Versioning, system prompts)
4. Data ingestion and preprocessing requirements (PDF parsing, text cleaning, etc.)
5. API rate limits and fallback mechanisms (What happens if the AI API goes down?)
6. Latency and performance requirements (Expected response time)
7. Security and data privacy requirements (Ensuring user data is not leaked to the AI)
8. Cost estimation and token budgeting (How much will the demo cost?)
9. Integration points (Vector DB, external APIs, backend frameworks)
10. Testing requirements for AI outputs

Keep the technical stack simple and realistic for a 24-48 hour hackathon. 
Explain all AI technical concepts in beginner-friendly language.

-------------------------------------------------------------
## 4 SYSTEM ARCHITECTURE 

Act as a senior AI software architect.
Using the following PRD and TRD, design a realistic hackathon architecture for an AI/ML project.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended tech stack (Frontend, Backend, AI frameworks)
2. Frontend architecture
3. Backend architecture
4. AI inference architecture (How the request reaches the model and returns)
5. Database choice (SQL/NoSQL/Vector)
6. Authentication approach
7. External APIs/services
8. Complete request/data flow diagram (Text-based)
9. Folder structure
10. Major components
11. Security considerations
12. Deployment architecture
13. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language. 
Do not introduce unnecessary technologies. Prefer a simple architecture that can be explained easily to judges.

-------------------------------------
## 5 DATABASE SCHEMA

Act as a senior database engineer.
Using the PRD and System Architecture below, design the database schema for an AI hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Tables (Include standard tables + AI-specific tables like ChatHistory, PromptLogs, Embeddings)
2. Columns
3. Data types
4. Primary keys
5. Foreign keys
6. Relationships
7. Required fields
8. Optional fields
9. Indexes where useful
10. Example records
11. SQL schema

Explain why each table exists. 
Keep the database simple enough for a beginner hackathon team to understand and maintain.

-------------------------
## 6 API SPECIFIACTION
You are a senior backend developer.
Using the PRD, Architecture, and Database Schema below, create a complete REST API specification for an AI hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DATABASE SCHEMA: [PASTE DATABASE_SCHEMA]

For every endpoint provide:
1. HTTP method
2. URL
3. Purpose
4. Authentication requirement
5. Request parameters
6. Request body
7. Example request
8. Example success response
9. Possible error responses (Include AI-specific errors like 429 Rate Limit, 503 Model Unavailable)
10. HTTP status codes

Keep the API simple and consistent. 
Do not create endpoints that are not required by the product.

-----------------

## 7 AI RULES 
You are an AI safety and prompt engineering expert.
Using the PRD and System Architecture, create the AI Rules and Guardrails document for this hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Create the AI_RULES.md with these sections:
1. System Prompt definition (The exact base prompt for the AI)
2. AI persona and tone guidelines
3. Context window management rules
4. Hallucination mitigation strategies
5. Fallback responses for API failures or bad outputs
6. Handling of inappropriate or off-topic user inputs
7. Data privacy rules (What should never be sent to the AI)
8. Token optimization rules
9. Output formatting rules (JSON, Markdown, etc.)
10. A checklist for developers to verify AI behavior before the demo

Keep the rules practical and enforceable within a hackathon timeframe.

---------------
## 8 AI MEMORY

Act as an AI systems engineer.
Using the PRD and AI Rules, create the AI Memory Management document for this hackathon project.

PRD: [PASTE PRD]
AI_RULES: [PASTE AI_RULES]

Provide:
1. Short-term memory (Conversation buffer, context window limits)
2. Long-term memory (Database storage, Vector DB if applicable)
3. Memory retrieval strategy (How past interactions are pulled into the prompt)
4. Summarization strategy (What to do when the context window gets full)
5. State management (How the backend tracks user sessions)
6. Privacy considerations for stored memory
7. A simple implementation plan for a 24-48 hour hackathon

Explain how memory improves the user experience without overcomplicating the tech stack.

------------------------------
## 9 PROMPT LIBRARY
Act as an AI systems engineer.
Using the PRD and AI Rules, create the AI Memory Management document for this hackathon project.

PRD: [PASTE PRD]
AI_RULES: [PASTE AI_RULES]

Provide:
1. Short-term memory (Conversation buffer, context window limits)
2. Long-term memory (Database storage, Vector DB if applicable)
3. Memory retrieval strategy (How past interactions are pulled into the prompt)
4. Summarization strategy (What to do when the context window gets full)
5. State management (How the backend tracks user sessions)
6. Privacy considerations for stored memory
7. A simple implementation plan for a 24-48 hour hackathon

Explain how memory improves the user experience without overcomplicating the tech stack.

------------------
## 10 CACHE SCHEMA 
Act as a backend/DevOps engineer.
Using the System Architecture and API Specification, create a Caching Strategy document for this AI hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. Cache strategy (Redis, In-memory, Semantic Cache)
2. Cache key structure (How to uniquely identify a request)
3. TTL (Time-to-live) for different types of data
4. Cache invalidation strategy (When to clear the cache)
5. What to cache (AI responses, embeddings, user sessions)
6. What NOT to cache (Personal data, sensitive prompts)
7. Fallback if cache fails
8. A simple implementation checklist

Explain how caching will save money and make the demo run faster.

------------------
 
## 11 EVIDENCE  MODEL 
You are a RAG and knowledge management expert.
Using the PRD and AI Rules, create the Evidence and Grounding Model for this AI hackathon project.

PRD: [PASTE PRD]
AI_RULES: [PASTE AI_RULES]

Provide:
1. Source of truth (Where does the AI get its facts?)
2. Chunking strategy (If using documents, how are they split?)
3. Embedding model (Which model, why?)
4. Vector Database (Which one, why?)
5. Retrieval logic (How many chunks to retrieve, similarity threshold)
6. Citation format (How does the AI show its sources?)
7. Hallucination checks (How to verify the AI isn't making things up)
8. Fallback if no evidence is found

If RAG is not needed for this project, explain alternative grounding techniques (e.g., few-shot prompting, structured data injection).

--------------
``
## 12 UI SPEC 

Act as a senior UI/UX designer.
Using the PRD and System Architecture below, create a UI Specification document for an AI/ML hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spacing)
2. Component hierarchy (List all major components)
3. Screen-by-screen breakdown (Login, Dashboard, AI Chat, Results)
4. Loading states (Crucial for AI: Skeletons, spinners, streaming text indicators)
5. Error states (How errors are displayed to the user)
6. Empty states (What the user sees before data is loaded)
7. Responsive design guidelines (Mobile and Desktop)
8. Accessibility considerations (Contrast, keyboard navigation)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon. 
Focus on demonstrating the core AI user journey.

---
## 13 ERROR HANDLING 

You are a senior backend developer.
Using the System Architecture and API Specification below, create an Error Handling document for this AI hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. AI API failure modes (Rate limits, timeouts, server errors)
2. Fallback responses (What to show the user if the AI fails)
3. Frontend error display (Toasts, inline errors, modals)
4. Retry logic (Exponential backoff, maximum retries)
5. Validation errors (Empty prompts, too long inputs)
6. Database connection errors
7. Authentication errors
8. A checklist for developers to verify error handling before the demo

Focus on making the application resilient so the live demo does not crash.

---
## 14 SECURITY 

Act as a security engineer.
Using the System Architecture and API Specification below, create a Security document for this AI hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. API key protection (Environment variables, backend-only access)
2. Authentication security (JWT, session management)
3. Input sanitization (Preventing prompt injection and XSS)
4. Data privacy (Ensuring user data is not leaked to the AI model)
5. Database security (Row-level security, permissions)
6. CORS configuration
7. Rate limiting (Preventing abuse of AI endpoints)
8. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.

---
## 15 TESTING

Act as a QA engineer specializing in AI applications.
Using the PRD and AI Rules below, create a Testing document for this AI/ML hackathon project.

PRD: [PASTE PRD]
AI_RULES: [PASTE AI_RULES]

Provide:
1. Testing strategy for AI outputs
2. Edge cases for prompts (Empty input, long input, malicious input)
3. How to test for hallucinations
4. API failure testing (Simulating downtime or rate limits)
5. Latency testing
6. User acceptance testing checklist
7. A manual testing checklist for the demo (Authentication, Core Feature, UI)
8. How to document known AI limitations for judges

Keep the testing plan simple enough for beginner developers to execute under time pressure.

---

## 16 EVALUATION 

You are an AI evaluation expert.
Using the PRD and AI Rules below, create an Evaluation document for this AI hackathon project.

PRD: [PASTE PRD]
AI_RULES: [PASTE AI_RULES]

Provide:
1. Evaluation metrics (Accuracy, relevance, latency, token usage)
2. Evaluation methods (Manual human-in-the-loop scoring, rubric)
3. Benchmarking (What is the baseline?)
4. Known limitations of the AI model
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about AI performance and how to answer them

Focus on demonstrating that the team understands their AI's capabilities and boundaries.

---
# BELOW DOCS ARE OPTIONAL - PHASE 4 

---

## 17 DEPLOYMENT 
Act as a DevOps engineer.
Using the System Architecture and API Specification below, create a Deployment document for this AI hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. Deployment platforms (Frontend, Backend, Database, AI service)
2. Environment variables for production (API keys, database URLs)
3. Step-by-step deployment instructions for each component
4. How to test the deployed application
5. Fallback plan if deployment fails during the hackathon
6. Cost considerations for AI API usage in production
7. A pre-deployment checklist
8. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon. 
Focus on getting a working live URL as early as possible.

---
## 18 DEMO SCRIPT
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
6. How it works (Include the AI model and architecture briefly)
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

## 19 GLOSSARY 
You are a technical writer.
Using the PRD, AI Rules, and Architecture below, create a Glossary document for this AI hackathon project.

PRD: [PASTE PRD]
AI_RULES: [PASTE AI_RULES]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. AI/ML terms (LLM, RAG, Embeddings, Tokens, Temperature, Context Window, Hallucination)
2. Technical terms (API, REST, JWT, Database, Vector DB, Cache)
3. Project-specific terms (Any custom terminology used in the PRD)
4. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable for a beginner audience. 
This will help all team members speak confidently to judges.

---

# All 19 documents for the **AI/ML Hackathons** category now have their complete Prompt Packs across all 4 Phases

---

### Thank You

Thank you for using this guide. Go build something amazing!

**Made by Siddiq

*Credit: Hackathon Alechemy Folder — AI/ML Category*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alechemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**