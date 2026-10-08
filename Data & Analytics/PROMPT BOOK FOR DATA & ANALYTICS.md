# Category 05: Data & Analytics

This category focuses on building data-driven projects using tools like **Python (Pandas)**, **SQL**, **Power BI**, **Tableau**, **Streamlit**, **Plotly**, and **Apache Spark**. It strips away traditional app-building complexities and focuses purely on **data ingestion, processing, analysis, and visualization** — the foundation of every data & analytics hackathon.

Here is the exact list of documents we will prepare for the **Data & Analytics** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core problem, target users, and existing data gaps (Analytics focus).
2. **`PRD.md`** (Product Requirements Document) — Outlines features, dashboards, MVP scope, and success metrics for a data project.
3. **`TRD.md`** (Technical Requirements Document) — Defines the data stack (Python, SQL, BI tools), data sources, and processing limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Data Sources → ETL → Storage → Analytics → Visualization (Data pipeline architecture).
5. **`DATA_MODEL.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines data tables, fields, relationships, and data dictionary.
6. **`DATA_PIPELINE.md`** — (Replaces `API_SPECIFICATION.md`) Defines the ETL/ELT process, data cleaning, and transformation logic.
7. **`DATA_GOVERNANCE.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines data privacy, access control, and compliance rules.

### Phase 3: Execution, Quality & Security
8. **`DASHBOARD_SPEC.md`** — (Replaces `UI_SPEC.md`) Frontend design, charts, KPIs, and user flow for the dashboard.
9. **`ERROR_HANDLING.md`** — What happens when data is missing, APIs fail, or queries time out.
10. **`SECURITY.md`** — Data privacy, PII handling, API key storage, and access control.
11. **`TESTING.md`** — QA plan, data validation, edge cases, and manual test checklists.
12. **`EVALUATION.md`** — How you measure if the analytics are performing well (Accuracy, Insight quality, Load time).

### Phase 4: Delivery & Presentation
13. **`DEPLOYMENT.md`** — Hosting the dashboard (Streamlit Cloud, Vercel, Power BI Service), database, and scheduled jobs.
14. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
15. **`GLOSSARY.md`** — Definitions of data terms (ETL, KPI, Data Warehouse, Pivot Table).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the problem and identify what data is needed to solve it.
```text
I am participating in a data & analytics hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing solutions
6. Proposed data & analytics solution ideas
7. Core analytics features (Dashboards, Reports, KPIs)
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential data sources and tools that could be used (CSV, APIs, SQL, Python, Power BI, etc.)

Do not assume I am an experienced data scientist.
Explain data concepts (ETL, KPI, Data Cleaning) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear data product plan with dashboards, KPIs, and scope.
```text
You are a senior data product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed analytics solution
7. Product goals
8. User stories
9. Functional requirements (Include data-specific requirements: Data ingestion, Cleaning, Transformation, Visualization)
10. Non-functional requirements (Data freshness, Query speed, Accuracy)
11. Core analytics features (Dashboards, Reports, KPIs)
12. Nice-to-have features
13. User journeys (How a user interacts with the data)
14. MVP scope (Which dashboard must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include data metrics: Data accuracy, Insight quality, Time to insight)
17. Risks and assumptions (Include data risks: Missing data, Dirty data, API limits)

Keep the MVP realistic for a 24-48 hour data hackathon.
Do not add unnecessary dashboards just to make the project sound impressive.
Prioritize insights that can actually be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on data stack, sources, and processing.
```text
You are a senior data engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Data stack choice (Python, SQL, Power BI, Streamlit, etc. — justify the choice)
3. Data sources (CSV, APIs, Databases, Web scraping)
4. Data ingestion requirements (Batch vs Streaming)
5. Data cleaning and transformation requirements
6. Data storage requirements (SQL, NoSQL, Data Warehouse, CSV)
7. Visualization and dashboard requirements
8. Performance and query speed requirements
9. Data privacy and security requirements
10. Data refresh and scheduling requirements
11. Testing requirements
12. Deployment requirements

Keep the data stack simple and realistic for a 24-48 hour hackathon.
Explain all data concepts in beginner-friendly language.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic data pipeline architecture with clear data flow from source to visualization.
```text
Act as a senior data architect.
Using the following PRD and TRD, design a realistic hackathon data architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended data stack (Python, SQL, Power BI, Streamlit, etc.)
2. Complete data pipeline diagram (Text-based, showing Source → Ingestion → Storage → Transformation → Visualization)
3. Data ingestion architecture (How data enters the system)
4. Data storage architecture (Where data is stored)
5. Data transformation architecture (How data is cleaned and processed)
6. Visualization architecture (Dashboards, Charts, KPIs)
7. External data sources and APIs
8. Data refresh and scheduling approach
9. Security and privacy considerations
10. Folder/Project structure
11. Major components
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools. Prefer a simple architecture that can be explained easily to judges.
```

---

### 5. DATA_MODEL.md
**Purpose:** To define the data tables, fields, relationships, and data dictionary.
```text
Act as a senior data modeler.
Using the PRD and System Architecture below, design the data model for a data & analytics hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Tables/Datasets (Fact tables, Dimension tables, Lookup tables)
2. Columns/Fields
3. Data types (Integer, String, Date, Boolean, Float)
4. Primary keys
5. Foreign keys
6. Relationships (One-to-Many, Many-to-Many)
7. Required fields
8. Optional fields
9. Data dictionary (What each field means)
10. Example records
11. Data quality rules (Nulls, Duplicates, Outliers)

Explain why each table exists.
Keep the data model simple enough for a beginner hackathon team to understand and maintain.
```

---

### 6. DATA_PIPELINE.md
**Purpose:** To define the ETL/ELT process, data cleaning, and transformation logic.
```text
You are a senior data engineer.
Using the PRD, Architecture, and Data Model below, create a Data Pipeline document for a data & analytics hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DATA_MODEL: [PASTE DATA_MODEL]

Provide:
1. Data sources (Where data comes from)
2. Ingestion method (Batch, Streaming, API pull, CSV upload)
3. Data cleaning steps (Handling nulls, duplicates, outliers)
4. Data transformation steps (Aggregations, Joins, Calculations)
5. Data validation rules (How to check if data is correct)
6. Data loading steps (Where cleaned data is stored)
7. Scheduling and refresh frequency
8. Error handling in the pipeline (What if data fails to load?)
9. Tools and libraries used (Pandas, SQL, Airflow, etc.)
10. A checklist for developers to verify the pipeline before the demo

Keep the pipeline simple and realistic for a hackathon.
Explain each step in beginner-friendly language.
```

---

### 7. DATA_GOVERNANCE.md
**Purpose:** To define data privacy, access control, and compliance rules.
```text
Act as a data governance specialist.
Using the PRD and Data Model below, create a Data Governance document for a data & analytics hackathon project.

PRD: [PASTE PRD]
DATA_MODEL: [PASTE DATA_MODEL]

Provide:
1. Data ownership (Who owns the data?)
2. Data privacy rules (What data can be shown publicly?)
3. PII handling (How to handle personally identifiable information)
4. Access control (Who can view, edit, or delete data?)
5. Data retention policy (How long is data stored?)
6. Compliance considerations (GDPR, HIPAA if applicable)
7. Data anonymization techniques (If needed)
8. A pre-submission data governance checklist

Keep the governance simple but responsible enough for a hackathon.
Explain concepts in beginner-friendly language.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 8. DASHBOARD_SPEC.md
**Purpose:** To define the dashboard layout, charts, KPIs, and user flow for the analytics interface.
```text
Act as a senior data visualization designer.
Using the PRD and System Architecture below, create a Dashboard Specification document for a data & analytics hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, chart styles)
2. Dashboard layout (Grid, Sections, Hierarchy)
3. Key Performance Indicators (KPIs) to display
4. Chart types for each insight (Bar, Line, Pie, Heatmap, Map)
5. Filters and interactivity (Date range, Category, Search)
6. Screen-by-screen breakdown (Overview, Detail, Comparison)
7. Loading states (Skeletons, spinners)
8. Error states (What if data fails to load?)
9. Empty states (What if no data is available?)
10. Responsive design guidelines (Desktop and Mobile)
11. Accessibility considerations (Color blindness, Contrast)

Keep the dashboard simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the core insights.
```

---

### 9. ERROR_HANDLING.md
**Purpose:** To define what happens when data is missing, APIs fail, or queries time out.
```text
You are a senior data engineer.
Using the System Architecture and Data Pipeline document below, create an Error Handling document for a data & analytics hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DATA_PIPELINE: [PASTE DATA_PIPELINE]

Provide:
1. Common failure modes (Missing data, API failures, Query timeouts, Data type errors)
2. Data validation errors (Nulls, Duplicates, Outliers)
3. Dashboard error display (Toasts, inline errors, fallback charts)
4. Retry logic for data ingestion
5. Fallback responses (What to show if data is unavailable)
6. Notification strategy (Alerts when data fails to load)
7. Error logging (Where errors are stored)
8. A checklist for developers to verify error handling before the demo

Focus on making the dashboard resilient so the live demo does not crash.
```

---

### 10. SECURITY.md
**Purpose:** To secure data, API keys, and user access in the analytics project.
```text
Act as a security engineer.
Using the System Architecture and Data Model below, create a Security document for a data & analytics hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DATA_MODEL: [PASTE DATA_MODEL]

Provide:
1. API key protection (Environment variables, Secret management)
2. Data privacy (PII handling, Anonymization)
3. Access control (Who can view or edit data?)
4. Database security (Row-level security, permissions)
5. Input sanitization (Preventing SQL injection)
6. Secure data transmission (HTTPS, Encryption)
7. Logging and monitoring for suspicious activity
8. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
```

---

### 11. TESTING.md
**Purpose:** To create a manual testing checklist for data quality, dashboards, and edge cases.
```text
Act as a QA engineer specializing in data & analytics.
Using the PRD and Data Pipeline document below, create a Testing document for a data & analytics hackathon project.

PRD: [PASTE PRD]
DATA_PIPELINE: [PASTE DATA_PIPELINE]

Provide:
1. Testing strategy for data quality
2. Data validation testing (Nulls, Duplicates, Outliers)
3. ETL testing (Does data transform correctly?)
4. Dashboard testing (Do charts load correctly?)
5. Filter and interactivity testing
6. Edge cases (Empty data, Large datasets, Missing fields)
7. User acceptance testing checklist
8. A manual testing checklist for the demo
9. How to document known data limitations for judges

Keep the testing plan simple enough for beginner data analysts to execute under time pressure.
```

---

### 12. EVALUATION.md
**Purpose:** To define how the team measures analytics performance and prepares for judge questions.
```text
You are a data evaluation expert.
Using the PRD and Architecture below, create an Evaluation document for a data & analytics hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Evaluation metrics (Data accuracy, Insight quality, Query speed, Load time)
2. Evaluation methods (Manual validation, Benchmarking, User feedback)
3. Benchmarking (What is the baseline?)
4. Known limitations of the data or analysis
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about data & analytics and how to answer them

Focus on demonstrating that the team understands the data's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 13. DEPLOYMENT.md
**Purpose:** To define how to deploy the dashboard, database, and scheduled jobs for the live demo.
```text
Act as a DevOps engineer.
Using the System Architecture and Data Pipeline document below, create a Deployment document for a data & analytics hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
DATA_PIPELINE: [PASTE DATA_PIPELINE]

Provide:
1. Deployment platforms (Streamlit Cloud, Vercel, Power BI Service, Render)
2. Database hosting (Supabase, PostgreSQL, MongoDB Atlas)
3. Environment variables for production
4. Step-by-step deployment instructions for each component
5. How to test the deployed dashboard
6. Scheduled jobs and data refresh in production
7. Fallback plan if deployment fails during the hackathon
8. A pre-deployment checklist
9. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working live dashboard as early as possible.
```

---

### 14. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the insights are shown off perfectly.
```text
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
INSIGHTS: [PASTE KEY INSIGHTS]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem
3. Why the problem matters
4. Existing limitations
5. Our data solution
6. How it works (Data pipeline and dashboard briefly)
7. Technology (Python, SQL, Power BI, Streamlit)
8. Demo (The most important part — show the insights)
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
```

---

### 15. GLOSSARY.md
**Purpose:** To define all data terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Data Pipeline, and Architecture below, create a Glossary document for a data & analytics hackathon project.

PRD: [PASTE PRD]
DATA_PIPELINE: [PASTE DATA_PIPELINE]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Data terms (ETL, ELT, Data Warehouse, Data Lake, Dataset, Schema)
2. Analytics terms (KPI, Metric, Dimension, Fact Table, Aggregation)
3. Visualization terms (Dashboard, Chart, Filter, Drill-down)
4. Data quality terms (Null, Duplicate, Outlier, Data Cleaning)
5. Tool-specific terms (Pandas, SQL, Power BI, Streamlit, Plotly)
6. Project-specific terms (Any custom terminology used in the PRD)
7. Acronyms and abbreviations

For each term:
- Simple definition (Beginner-friendly)
- Why it matters for this project
- Example usage in context

Keep definitions concise and understandable for a beginner audience.
This will help all team members speak confidently to judges.
```

---
Thank you for using this guide. Go build something amazing!

**Made by Siddiq

*Credit: Hackathon Alechemy 

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alechemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**

