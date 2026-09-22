# Category 01: AI / ML Hackathons

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

## Phase 3: Execution, Quality & Security
*Focuses on building, testing, and securing the AI application.*

12. **`UI_SPEC.md`** — Frontend design, components, and user flow. *Necessary to ensure the UI handles loading states and streaming responses properly.*
13. **`ERROR_HANDLING.md`** — What happens when the AI API fails, times out, or returns bad JSON. *Necessary for a smooth demo when the internet inevitably drops.*
14. **`SECURITY.md`** — API key storage, user data privacy, and prompt injection prevention. *Necessary to ensure `.env` files are ignored and user data isn't leaked to the AI.*
15. **`TESTING.md`** — QA plan, edge cases, and manual test checklists. *Necessary to test for hallucinations and edge cases (e.g., empty prompts, malicious inputs).*
16. **`EVALUATION.md`** — How you measure if the AI is performing well. *Necessary for judges who ask, "How do you know your AI is accurate?"*

## Phase 4: Delivery & Presentation
*Focuses on shipping the project and winning the hackathon.*

17. **`DEPLOYMENT.md`** — Hosting the frontend, backend, and managing production environment variables. *Necessary to get a live URL working early.*
18. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation. *Necessary to ensure the AI features are shown off perfectly within the time limit.*
19. **`GLOSSARY.md`** — Definitions of AI terms (RAG, Tokens, Temperature, Embeddings). *Necessary so every team member can explain the tech to judges without confusion.*

---

### Prompts for Generating Documents 
---------------------------

###  1 PROBLEM_ANALYSIS.md

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
