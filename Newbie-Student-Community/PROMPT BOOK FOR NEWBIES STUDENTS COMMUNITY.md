# Category 15: Beginner / Student / Community

This category focuses on building solutions for **first-time hackers**, **college students**, **community sprints**, and **learning-focused hackathons**. It focuses purely on **simplicity, learning, mentorship, and community building** — the foundation of every Beginner/Student/Community hackathon.

Here is the exact list of documents we will prepare for the **Beginner / Student / Community** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the problem in beginner-friendly terms, focusing on learning and community impact.
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and learning metrics.
3. **`TRD.md`** (Technical Requirements Document) — Defines the simplest possible tech stack and learning-friendly tools.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level architecture designed for beginners to understand and build.
5. **`LEARNING_PATH.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines what the team needs to learn, in what order, and by when.
6. **`API_SPECIFICATION.md`** — Defines simple endpoints with beginner-friendly documentation.
7. **`MENTOR_GUIDE.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines how mentors can guide the team through blockers.
8. **`TEAM_ROLES.md`** — Defines team roles for beginners (Frontend, Backend, Design, PM).
9. **`RESOURCE_LIST.md`** — Curated list of tutorials, docs, and tools for beginners.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Simple, clean frontend design that beginners can build.
11. **`ERROR_HANDLING.md`** — Common beginner mistakes and how to fix them.
12. **`SECURITY.md`** — Basic security practices explained simply.
13. **`TESTING.md`** — Simple testing checklist for beginners.
14. **`EVALUATION.md`** — How you measure learning and community impact.

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — The simplest way to deploy for beginners (Vercel, Netlify).
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation for first-time presenters.
17. **`GLOSSARY.md`** — Definitions of all terms in beginner-friendly language.

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the problem in beginner-friendly terms, focusing on learning and community impact.
```text
I am participating in a beginner/student/community hackathon and I am a first-time hacker.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language — as if I have never built a project before.
Then provide:
1. The actual problem being solved
2. Target users (Students, Community members, Beginners)
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing solutions
6. Proposed solution ideas (Keep them simple)
7. Core features (What is the smallest thing we can build?)
8. Nice-to-have features
9. What should NOT be built during a short hackathon (Avoid scope creep)
10. What could make this solution unique
11. A realistic MVP that can be built by beginners during a hackathon
12. Potential beginner-friendly technologies that could be used (HTML, CSS, JavaScript, React, no-code tools)

Do not assume I am an experienced developer.
Explain every concept in beginner-friendly language.
Suggest learning resources where needed.
Focus on what is achievable in 24-48 hours by a first-time team.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear, simple plan that beginners can execute.
```text
You are a senior product manager helping a beginner student hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Project name (Simple, memorable)
2. One-line project description
3. Problem statement (Simple language)
4. Target users (Students, Community)
5. User pain points
6. Proposed solution
7. Project goals (Learning + Impact)
8. User stories (Simple, one per feature)
9. Functional requirements (Keep it minimal)
10. Non-functional requirements (Simple, achievable)
11. Core features (Maximum 3)
12. Nice-to-have features (If time permits)
13. User journeys (Simple, step-by-step)
14. MVP scope (What must work during the demo?)
15. Out-of-scope features (What we will NOT build)
16. Success metrics (Learning goals + Impact goals)
17. Risks and assumptions (Beginner-specific risks)

Keep the MVP extremely realistic for first-time hackers.
Do not add unnecessary features.
Prioritize learning and completion over complexity.
Maximum 3 core features.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into the simplest possible technical specifications.
```text
You are a senior developer helping a beginner student hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview (Simple explanation)
2. Tech stack choice (Simplest possible: HTML/CSS/JS, React, or no-code)
3. Frontend requirements (What tools? What framework?)
4. Backend requirements (Do we even need one?)
5. Database requirements (Simple: JSON file, localStorage, or Firebase)
6. API requirements (If needed)
7. Authentication requirements (If needed — keep simple)
8. Third-party integrations (Free tools only)
9. Performance requirements (Basic)
10. Security requirements (Basic)
11. Testing requirements (Simple manual testing)
12. Deployment requirements (Free hosting: Vercel, Netlify, GitHub Pages)

Keep the tech stack as simple as possible for beginners.
Explain every technical choice in beginner-friendly language.
If something is too complex, suggest a simpler alternative.
Only include what is necessary for the MVP.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic architecture that beginners can understand and build.
```text
Act as a senior developer and mentor.
Using the following PRD and TRD, design a realistic hackathon architecture for a beginner team.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended tech stack (Simplest possible)
2. Complete architecture diagram (Text-based, simple boxes and arrows)
3. Frontend architecture (Components or pages)
4. Backend architecture (If needed)
5. Database architecture (If needed)
6. Data flow (Simple step-by-step)
7. Folder structure (Beginner-friendly)
8. Major components (Maximum 5)
9. What each team member will build
10. Simplifications that make this beginner-friendly
11. Common beginner mistakes to avoid
12. A simple checklist for the team

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools.
If something is complex, explain how to simplify it.
Focus on what a beginner team can actually build in 24-48 hours.
```

---

### 5. LEARNING_PATH.md
**Purpose:** To define what the team needs to learn, in what order, and by when.
```text
You are a senior mentor for beginner hackathon teams.
Using the PRD and System Architecture below, create a Learning Path document for this beginner hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Skills needed (Frontend, Backend, Design, Git)
2. Learning priority (What to learn first?)
3. Time allocation (Hours per skill)
4. Learning resources (Free tutorials, YouTube, Docs)
5. Pre-hackathon preparation (What to learn before the event)
6. During-hackathon learning (Just-in-time learning)
7. Skill-to-task mapping (Who learns what to build what)
8. Pair learning strategy (Learn together)
9. Mentor checkpoints (When to ask for help)
10. A checklist for the team to track progress

Explain each skill in beginner-friendly language.
Recommend only free resources.
Keep the learning path realistic for a 24-48 hour hackathon.
Focus on learning by building, not learning everything upfront.
```

---

### 6. API_SPECIFICATION.md
**Purpose:** To define simple endpoints with beginner-friendly documentation.
```text
You are a senior developer who loves teaching beginners.
Using the PRD and System Architecture below, create a simple API specification for a beginner hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

For every endpoint provide:
1. HTTP method (GET, POST, etc.)
2. URL (Simple and clear)
3. What it does (In one sentence)
4. Do you need authentication? (Yes/No)
5. What data you send (Request body)
6. What data you get back (Response)
7. Example request (Copy-paste ready)
8. Example response (Copy-paste ready)
9. Common errors and what they mean
10. Beginner tip (Something helpful)

Keep the API as simple as possible.
If the project does not need an API, explain why and suggest an alternative.
Explain everything in beginner-friendly language.
Use simple examples that beginners can understand.
```

---

### 7. MENTOR_GUIDE.md
**Purpose:** To define how mentors can guide the team through blockers.
```text
You are a senior hackathon mentor.
Using the PRD and System Architecture below, create a Mentor Guide document for this beginner hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. How mentors can help (Without taking over)
2. Common beginner blockers and solutions
3. Debugging strategies for beginners
4. How to explain technical concepts simply
5. When to intervene vs when to let them figure it out
6. Mentor check-in schedule (Every 2-4 hours)
7. Questions mentors should ask
8. Questions mentors should NOT answer directly
9. Encouraging progress and celebrating small wins
10. How to help with time management
11. How to help with scope management
12. A checklist for mentors before the demo

Explain each concept in beginner-friendly language.
Focus on empowering the team to solve their own problems.
Keep the mentor involvement light — this is a learning experience.
```

---

### 8. TEAM_ROLES.md
**Purpose:** To define team roles for beginners (Frontend, Backend, Design, PM).
```text
You are a senior team lead for beginner hackathon teams.
Using the PRD and System Architecture below, create a Team Roles document for this beginner hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

For a team of 3-4 beginners, define:
1. Role names (Frontend Developer, Backend Developer, Designer, PM/Presenter)
2. Responsibilities for each role
3. Skills needed for each role
4. Daily tasks for each role
5. Collaboration points (When roles work together)
6. Backup plans (If someone is stuck)
7. How to divide the MVP work
8. How to handle overlaps
9. Communication guidelines
10. A RACI matrix (Who is Responsible, Accountable, Consulted, Informed)

Also provide:
11. What to do if you are a solo hacker
12. What to do if someone drops out
13. How to rotate roles if needed

Explain each role in beginner-friendly language.
Keep the roles simple and flexible.
Focus on ensuring everyone has something meaningful to do.
```

---

### 9. RESOURCE_LIST.md
**Purpose:** To curate a list of tutorials, docs, and tools for beginners.
```text
You are a senior developer curating resources for beginner hackathon teams.
Using the PRD and TRD below, create a Resource List document for this beginner hackathon project.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide curated resources for:
1. HTML, CSS, JavaScript (MDN, freeCodeCamp, W3Schools)
2. React (React Docs, Scrimba, YouTube)
3. Tailwind CSS (Tailwind Docs, YouTube)
4. Git and GitHub (GitHub Docs, Git Basics)
5. Backend (Node.js, Express, FastAPI — depending on stack)
6. Database (Firebase, Supabase, SQLite — depending on stack)
7. Design (Figma, Canva, Coolors, Google Fonts)
8. Deployment (Vercel, Netlify, GitHub Pages)
9. Debugging (Chrome DevTools, Console)
10. AI Coding Tools (Claude, Cursor, GitHub Copilot)
11. Free Assets (Unsplash, Lucide, Heroicons, Google Fonts)
12. YouTube Channels (Traversy Media, Web Dev Simplified, Fireship)

For each resource, include:
- Name
- Link
- What it's for
- Why it's good for beginners

Keep the list short and focused — maximum 2-3 resources per topic.
Only recommend free resources.
Explain each resource in beginner-friendly language.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define a simple, clean frontend design that beginners can build.
```text
Act as a senior UI/UX designer who loves teaching beginners.
Using the PRD and System Architecture below, create a simple UI Specification document for a beginner hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Simple: 2 colors, 1 font, basic spacing)
2. Component hierarchy (Maximum 5 components)
3. Screen-by-screen breakdown (Maximum 3 screens)
4. Simple layouts (Text-based wireframes)
5. Loading states (Simple spinners)
6. Error states (Simple messages)
7. Empty states (Simple placeholders)
8. Responsive design (Mobile-first, simple breakpoints)
9. Accessibility basics (Contrast, Alt text)
10. Free design tools (Figma, Canva, Coolors)
11. A checklist for beginners

Keep the UI extremely simple.
Do not over-design.
Focus on functionality over beauty.
Explain every design choice in beginner-friendly language.
Suggest free templates where possible.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define common beginner mistakes and how to fix them.
```text
You are a patient senior developer helping beginners.
Using the System Architecture and API Specification below, create an Error Handling document for a beginner hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. Top 10 beginner mistakes (With fixes)
2. Common JavaScript errors (Undefined, Null, Type errors)
3. Common React errors (Hooks, State, Props)
4. Common Git errors (Merge conflicts, Push rejected)
5. Common API errors (CORS, 404, 500)
6. Common deployment errors (Build failed, Environment variables)
7. Debugging tools for beginners (Console.log, Chrome DevTools)
8. How to search for errors effectively
9. How to ask for help (Mentors, Stack Overflow, AI tools)
10. A checklist for beginners to verify before asking for help

Explain each error in beginner-friendly language.
Provide copy-paste fixes where possible.
Focus on building confidence, not fear.
Keep it simple — 1-2 sentences per error.
```

---

### 12. SECURITY.md
**Purpose:** To define basic security practices explained simply.
```text
Act as a security engineer who loves teaching beginners.
Using the System Architecture and PRD below, create a simple Security document for a beginner hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PRD: [PASTE PRD]

Provide:
1. What is an API key? (Simple explanation)
2. Why you should NEVER commit API keys to GitHub
3. How to use .env files (Step-by-step)
4. How to add .env to .gitignore
5. Basic password security (Don't store plain text)
6. Basic input validation (Don't trust user input)
7. HTTPS basics (Why it matters)
8. Free security tools (GitHub secret scanning)
9. A pre-submission security checklist for beginners
10. What to do if you accidentally exposed a secret

Explain each concept in beginner-friendly language.
Use analogies where helpful.
Do not overwhelm — focus on the 3-5 most important rules.
Keep it practical for a 24-48 hour hackathon.
```

---

### 13. TESTING.md
**Purpose:** To create a simple testing checklist for beginners.
```text
Act as a QA engineer who loves teaching beginners.
Using the PRD and API Specification below, create a simple Testing document for a beginner hackathon project.

PRD: [PASTE PRD]
API_SPEC: [PASTE API_SPECIFICATION]

Provide:
1. What is testing? (Simple explanation)
2. Manual testing checklist (Click everything)
3. Form testing (Empty, Invalid, Long input)
4. Button testing (Does it do what it should?)
5. Page testing (Does every page load?)
6. Mobile testing (Resize browser, Use phone)
7. Link testing (Click every link)
8. Console testing (Check for errors)
9. A simple test log template
10. What to do when you find a bug
11. A checklist for the demo

Keep the testing plan extremely simple.
No automated testing — just manual checks.
Explain everything in beginner-friendly language.
Focus on preventing demo-day disasters.
```

---

### 14. EVALUATION.md
**Purpose:** To define how you measure learning and community impact.
```text
You are a senior educator and hackathon evaluator.
Using the PRD and Learning Path below, create an Evaluation document for a beginner hackathon project.

PRD: [PASTE PRD]
LEARNING_PATH: [PASTE LEARNING_PATH]

Provide:
1. Learning metrics (What did the team learn?)
2. Project metrics (Does the project work?)
3. Community metrics (Does it help the target users?)
4. Self-assessment checklist (Rate yourself 1-5)
5. Peer assessment (Team members rate each other)
6. Mentor assessment (What did the mentor observe?)
7. Evidence to gather (Screenshots, Demo, Repo)
8. How to present learning outcomes to judges
9. Common judge questions for beginner teams
10. How to answer "What would you do differently?"

Focus on growth and learning, not perfection.
Celebrate progress over polish.
Explain each concept in beginner-friendly language.
Prepare the team to speak confidently about their journey.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To define the simplest way to deploy for beginners.
```text
Act as a DevOps engineer who loves teaching beginners.
Using the System Architecture and PRD below, create a simple Deployment document for a beginner hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PRD: [PASTE PRD]

Provide:
1. What is deployment? (Simple explanation)
2. Free hosting options (Vercel, Netlify, GitHub Pages)
3. Which one to pick and why
4. Step-by-step deployment for beginners
5. Connecting your GitHub repository
6. Environment variables (If needed)
7. How to test your deployed site
8. What to do if deployment fails
9. Common deployment mistakes for beginners
10. A pre-deployment checklist
11. How to share your live link

Keep the deployment process as simple as possible.
No complex DevOps — just drag-and-drop or one-click deploys.
Explain everything in beginner-friendly language.
Include screenshots descriptions where helpful.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation for first-time presenters.
```text
Act as an expert hackathon presentation coach for first-time presenters.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
FEATURES: [PASTE CORE FEATURES]
DEMO FLOW: [PASTE USER JOURNEY]

Create a simple, encouraging hackathon presentation script.
The presentation should follow:
1. Introduction (Who we are)
2. The Problem (Why we built this)
3. Our Solution (What we built)
4. How It Works (Simple, no jargon)
5. Live Demo (The most important part)
6. What We Learned (This is key for beginners)
7. Challenges We Overcame
8. Future Ideas
9. Thank You

Make the language simple and natural.
Encourage honesty about challenges.
Celebrate the learning journey.
Write it as something a first-time presenter can actually say.
Provide:
- 30-second elevator pitch
- 1-minute pitch
- 3-minute presentation
- 5-minute presentation
Include tips for overcoming nervousness.
Include a backup plan for demo failure (screenshots, video).
```

---

### 17. GLOSSARY.md
**Purpose:** To define all terms in beginner-friendly language.
```text
You are a patient teacher explaining technical terms to beginners.
Using the PRD, TRD, and Architecture below, create a Glossary document for a beginner hackathon project.

PRD: [PASTE PRD]
TRD: [PASTE TRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide simple definitions for all terms used in the project:
1. Web basics (HTML, CSS, JavaScript, Browser, Server)
2. Frontend terms (Component, State, Props, Responsive)
3. Backend terms (API, Endpoint, Database, Server)
4. Git terms (Repository, Commit, Push, Pull, Branch)
5. Deployment terms (Hosting, Domain, Environment Variables)
6. Hackathon terms (MVP, Demo, Pitch, Judge)
7. Project-specific terms (Any custom terminology)

For each term:
- Simple definition (One sentence, no jargon)
- Real-world analogy (Compare to something familiar)
- Why it matters for this project

Keep definitions extremely simple.
Use analogies wherever possible (e.g., "An API is like a waiter taking your order to the kitchen").
This glossary should make any beginner feel confident.
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
