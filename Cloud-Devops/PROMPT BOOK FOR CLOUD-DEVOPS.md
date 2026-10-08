# Category 10: Cloud / DevOps / Platform

This category focuses on building cloud-native and infrastructure-focused projects using tools like **AWS**, **Azure**, **GCP**, **Docker**, **Kubernetes**, **Terraform**, **GitHub Actions**, **Jenkins**, **Prometheus**, and **Grafana**. It focuses purely on **infrastructure, deployment pipelines, scalability, observability, and platform engineering** — the foundation of every Cloud/DevOps hackathon.

Here is the exact list of documents we will prepare for the **Cloud / DevOps / Platform** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core infrastructure/deployment problem, target users, and existing gaps (DevOps focus).
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for a DevOps tool.
3. **`TRD.md`** (Technical Requirements Document) — Defines the cloud stack (AWS, Azure, GCP), IaC tool, and CI/CD limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Code → Build → Deploy → Monitor (DevOps architecture).
5. **`INFRASTRUCTURE_SPEC.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines cloud resources, compute, storage, and networking.
6. **`PIPELINE_SPEC.md`** — (Replaces `API_SPECIFICATION.md`) Defines CI/CD stages, triggers, and deployment strategies.
7. **`IAC_SPEC.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines Terraform/CloudFormation/Pulumi resources and modules.
8. **`CONTAINER_SPEC.md`** — Defines Docker images, Kubernetes manifests, and orchestration.
9. **`OBSERVABILITY_SPEC.md`** — Defines logging, metrics, tracing, and alerting.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Dashboard design, pipeline visualization, and user flow.
11. **`ERROR_HANDLING.md`** — What happens when a build fails, deployment rolls back, or a node crashes.
12. **`SECURITY.md`** — IAM, secrets management, network security, and compliance.
13. **`TESTING.md`** — QA plan, pipeline testing, chaos engineering, and edge cases.
14. **`EVALUATION.md`** — How you measure DevOps performance (DORA metrics, Uptime, MTTR).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Deploying the platform, configuring environments, and setting up monitoring.
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
17. **`GLOSSARY.md`** — Definitions of DevOps terms (CI/CD, IaC, K8s, DORA, SRE).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the infrastructure/deployment problem and identify what manual, slow, or unreliable processes need automation.
```text
I am participating in a Cloud/DevOps/Platform hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users (Developers, SREs, Platform teams, DevOps engineers)
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing solutions
6. Proposed Cloud/DevOps solution ideas
7. Core DevOps features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential cloud platforms and tools that could be used (AWS, Azure, GCP, Docker, Kubernetes, Terraform)

Do not assume I am an experienced DevOps engineer.
Explain DevOps concepts (CI/CD, IaC, Containers, Orchestration, Observability) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear DevOps product plan with pipelines, infrastructure, and scope.
```text
You are a senior DevOps product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed DevOps solution
7. Product goals
8. User stories
9. Functional requirements (Include DevOps-specific requirements: Build, Test, Deploy, Monitor, Rollback)
10. Non-functional requirements (Reliability, Scalability, Security, Speed)
11. Core DevOps features
12. Nice-to-have features
13. User journeys (How a developer pushes code and sees it deployed)
14. MVP scope (Which pipeline or infrastructure feature must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include DevOps metrics: Deployment frequency, Lead time, MTTR, Change failure rate)
17. Risks and assumptions (Include DevOps risks: Cloud costs, API limits, Region outages)

Keep the MVP realistic for a 24-48 hour Cloud/DevOps hackathon.
Do not add unnecessary infrastructure just to make the project sound impressive.
Prioritize features that can actually be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on cloud platform, IaC, and CI/CD tools.
```text
You are a senior cloud engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Cloud platform choice (AWS, Azure, GCP — justify the choice)
3. Infrastructure as Code tool (Terraform, CloudFormation, Pulumi)
4. Containerization requirements (Docker, Podman)
5. Orchestration requirements (Kubernetes, ECS, Cloud Run)
6. CI/CD tool choice (GitHub Actions, GitLab CI, Jenkins, CircleCI)
7. Build and artifact requirements (Docker registry, Artifactory)
8. Environment requirements (Dev, Staging, Prod)
9. Secrets and configuration management (Vault, AWS Secrets Manager)
10. Observability requirements (Logging, Metrics, Tracing)
11. Security and compliance requirements
12. Cost and budget requirements
13. Testing requirements
14. Deployment requirements

Keep the cloud stack simple and realistic for a 24-48 hour hackathon.
Explain all DevOps concepts in beginner-friendly language.
Do not introduce unnecessary tools. Prioritize free-tier services.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic DevOps architecture with clear data flow from code to production.
```text
Act as a senior cloud architect.
Using the following PRD and TRD, design a realistic hackathon DevOps architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended cloud stack (Platform, IaC, Containers, CI/CD)
2. Complete DevOps architecture diagram (Text-based, showing Code → Build → Test → Deploy → Monitor)
3. Source control architecture (Git, Branching strategy)
4. CI architecture (Build, Test, Artifact)
5. CD architecture (Deploy, Rollback, Blue-Green/Canary)
6. Infrastructure architecture (Compute, Storage, Networking)
7. Container architecture (Docker, Kubernetes)
8. Observability architecture (Logs, Metrics, Traces)
9. Secrets management architecture
10. Data flow (How a commit becomes a deployed application)
11. Security considerations (IAM, Network, Secrets)
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools. Prefer a simple architecture that can be explained easily to judges.
Prioritize free-tier and serverless where possible to keep costs at zero.
```

---

### 5. INFRASTRUCTURE_SPEC.md
**Purpose:** To define cloud resources, compute, storage, and networking.
```text
Act as a senior cloud infrastructure engineer.
Using the PRD and System Architecture below, create an Infrastructure Specification document for this DevOps hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Compute resources (VMs, Containers, Serverless functions)
2. Storage resources (Object storage, Block storage, File storage)
3. Database resources (Managed DB, Cache, Queue)
4. Networking resources (VPC, Subnets, Load Balancer, DNS)
5. Identity and access resources (IAM roles, Service accounts)
6. Monitoring resources (Log groups, Metrics, Alerts)
7. Region and availability zone strategy
8. Scaling strategy (Horizontal, Vertical, Auto-scaling)
9. Cost estimate for the hackathon (Free tier, Budget)
10. Resource naming conventions and tagging
11. A checklist for verifying infrastructure before the demo

Explain why each resource exists.
Keep the infrastructure simple enough for a beginner hackathon team to understand and maintain.
Prefer managed services over self-hosted to save time.
```

---

### 6. PIPELINE_SPEC.md
**Purpose:** To define CI/CD stages, triggers, and deployment strategies.
```text
You are a senior DevOps pipeline engineer.
Using the PRD and System Architecture below, create a CI/CD Pipeline Specification document for this DevOps hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. CI/CD tool choice (GitHub Actions, GitLab CI, Jenkins, CircleCI)
2. Pipeline triggers (Push, Pull Request, Tag, Schedule)
3. CI stages (Lint, Build, Test, Security Scan, Artifact)
4. CD stages (Deploy to Dev, Staging, Production)
5. Deployment strategy (Rolling, Blue-Green, Canary)
6. Environment variables and secrets in pipeline
7. Artifact management (Docker registry, Build artifacts)
8. Rollback strategy (How to revert a bad deployment)
9. Notifications (Slack, Email on success/failure)
10. Pipeline as code (YAML example)
11. Branching strategy (GitFlow, Trunk-based)
12. A checklist for verifying the pipeline before the demo

Explain each stage in beginner-friendly language.
Keep the pipeline simple and reliable for a hackathon.
Prioritize speed over completeness.
```

---

### 7. IAC_SPEC.md
**Purpose:** To define Terraform/CloudFormation/Pulumi resources and modules.
```text
Act as a senior Infrastructure as Code engineer.
Using the PRD and Infrastructure Spec below, create an IaC Specification document for this DevOps hackathon project.

PRD: [PASTE PRD]
INFRASTRUCTURE_SPEC: [PASTE INFRASTRUCTURE_SPEC]

Provide:
1. IaC tool choice (Terraform, CloudFormation, Pulumi, Ansible)
2. Project structure (Modules, Environments, Variables)
3. Resource definitions (Compute, Storage, Network, IAM)
4. Variables and outputs
5. State management (Remote state, Locking)
6. Environment separation (Dev, Staging, Prod)
7. Secrets management in IaC
8. Provider configuration
9. Example code snippets
10. Apply and destroy workflow
11. Cost estimation and budget alerts
12. A checklist for verifying IaC before the demo

Explain each concept in beginner-friendly language.
Keep the IaC simple and realistic for a hackathon.
Use free-tier resources wherever possible.
```

---

### 8. CONTAINER_SPEC.md
**Purpose:** To define Docker images, Kubernetes manifests, and orchestration.
```text
You are a senior container and Kubernetes engineer.
Using the PRD and System Architecture below, create a Container Specification document for this DevOps hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Containerization approach (Docker, Podman)
2. Dockerfile best practices (Multi-stage builds, Minimal base images)
3. Image registry (Docker Hub, ECR, GCR, ACR)
4. Image tagging strategy (Latest, Semantic, Git SHA)
5. Orchestration choice (Kubernetes, ECS, Cloud Run, Docker Compose)
6. Kubernetes manifests (Deployment, Service, Ingress, ConfigMap, Secret)
7. Scaling (HPA, Replicas)
8. Health checks (Liveness, Readiness)
9. Resource limits (CPU, Memory)
10. Networking (Service, Ingress, Load Balancer)
11. Example Dockerfile and manifest
12. A checklist for verifying containers before the demo

Explain each concept in beginner-friendly language.
Keep the container setup simple and realistic for a hackathon.
If Kubernetes is too complex, recommend a simpler alternative.
```

---

### 9. OBSERVABILITY_SPEC.md
**Purpose:** To define logging, metrics, tracing, and alerting.
```text
Act as a senior SRE/observability engineer.
Using the PRD and System Architecture below, create an Observability Specification document for this DevOps hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Observability pillars (Logs, Metrics, Traces)
2. Logging strategy (What to log, Format, Retention)
3. Metrics strategy (What to measure, Dashboards)
4. Tracing strategy (Distributed tracing, Correlation IDs)
5. Tools (Prometheus, Grafana, Loki, Jaeger, Datadog, CloudWatch)
6. Alerting rules (What triggers an alert?)
7. Notification channels (Slack, Email, PagerDuty)
8. Dashboards (Golden signals: Latency, Traffic, Errors, Saturation)
9. SLOs and SLIs (If applicable)
10. Incident response integration
11. Example dashboard layout
12. A checklist for verifying observability before the demo

Explain each concept in beginner-friendly language.
Keep the observability setup simple and realistic for a hackathon.
Prefer free-tier tools.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define the dashboard design, pipeline visualization, and user flow.
```text
Act as a senior UI/UX designer specializing in DevOps dashboards.
Using the PRD and System Architecture below, create a UI Specification document for a DevOps hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spacing)
2. Component hierarchy (Pipeline view, Logs viewer, Metrics cards, Alerts)
3. Screen-by-screen breakdown (Dashboard, Pipeline Detail, Logs, Metrics, Alerts)
4. Real-time data display (Pipeline status, Deployment progress, Metrics)
5. Status indicators (Success, Failed, Running, Pending)
6. Loading states (Skeletons, spinners)
7. Error states (Pipeline failed, Connection lost)
8. Empty states (No pipelines yet)
9. Responsive design guidelines (Desktop-first for DevOps)
10. Accessibility considerations (Contrast, Color blindness)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the core pipeline and deployment journey.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when a build fails, deployment rolls back, or a node crashes.
```text
You are a senior DevOps reliability engineer.
Using the System Architecture and Pipeline Spec below, create an Error Handling document for a DevOps hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PIPELINE_SPEC: [PASTE PIPELINE_SPEC]

Provide:
1. Common failure modes (Build failure, Test failure, Deployment failure, Node crash)
2. CI error handling (Fail fast, Retry transient failures)
3. CD error handling (Automatic rollback, Manual approval)
4. Infrastructure error handling (Auto-healing, Auto-scaling)
5. Container error handling (CrashLoopBackOff, OOMKilled)
6. Observability error handling (Alert on failure)
7. Notification strategy (Slack, Email on failure)
8. Recovery procedures (Re-run pipeline, Rollback, Restore from backup)
9. A checklist for developers to verify error handling before the demo

Focus on making the pipeline resilient so the live demo does not crash.
Explain each error handling approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** To define IAM, secrets management, network security, and compliance.
```text
Act as a cloud security engineer.
Using the System Architecture and Infrastructure Spec below, create a Security document for a DevOps hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
INFRASTRUCTURE_SPEC: [PASTE INFRASTRUCTURE_SPEC]

Provide:
1. Identity and Access Management (IAM roles, Least privilege, MFA)
2. Secrets management (Vault, AWS Secrets Manager, GitHub Secrets)
3. Network security (VPC, Security Groups, Firewalls, Private subnets)
4. Container security (Image scanning, Non-root user, Read-only FS)
5. Supply chain security (Dependency scanning, SBOM)
6. Encryption (At rest, In transit, Key management)
7. Compliance considerations (GDPR, SOC 2, HIPAA)
8. Audit logging (CloudTrail, Cloud Audit Logs)
9. Incident response integration
10. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
Never commit secrets to Git.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist for pipelines, infrastructure, and edge cases.
```text
Act as a QA engineer specializing in DevOps.
Using the PRD and Pipeline Spec below, create a Testing document for a DevOps hackathon project.

PRD: [PASTE PRD]
PIPELINE_SPEC: [PASTE PIPELINE_SPEC]

Provide:
1. Testing strategy for DevOps
2. Unit testing in CI (Code tests)
3. Integration testing in CI (Service tests)
4. Pipeline testing (Does the pipeline run end-to-end?)
5. Infrastructure testing (Does IaC apply cleanly?)
6. Container testing (Does the image build and run?)
7. Deployment testing (Does the app deploy and respond?)
8. Rollback testing (Does rollback work?)
9. Chaos engineering (Simulate failures)
10. Edge cases (Large builds, Slow networks, Resource limits)
11. User acceptance testing checklist
12. A manual testing checklist for the demo
13. How to document known DevOps limitations for judges

Keep the testing plan simple enough for beginner DevOps engineers to execute under time pressure.
```

---

### 14. EVALUATION.md
**Purpose:** To define how the team measures DevOps performance and prepares for judge questions.
```text
You are a DevOps evaluation expert.
Using the PRD and Pipeline Spec below, create an Evaluation document for a DevOps hackathon project.

PRD: [PASTE PRD]
PIPELINE_SPEC: [PASTE PIPELINE_SPEC]

Provide:
1. Evaluation metrics (DORA metrics: Deployment frequency, Lead time, MTTR, Change failure rate)
2. Additional metrics (Uptime, Build time, Cost per deployment)
3. Evaluation methods (Benchmarking, Load testing, Chaos testing)
4. Benchmarking (What is the baseline?)
5. Known limitations of the DevOps setup
6. How to explain these limitations to judges honestly
7. A checklist of evidence to gather for the presentation
8. Common judge questions about DevOps and how to answer them

Focus on demonstrating that the team understands the pipeline's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To define how to deploy the platform, configure environments, and set up monitoring.
```text
Act as a DevOps deployment engineer.
Using the System Architecture and Pipeline Spec below, create a Deployment document for a DevOps hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PIPELINE_SPEC: [PASTE PIPELINE_SPEC]

Provide:
1. Deployment environment (Dev, Staging, Prod)
2. Deployment platforms (AWS, GCP, Azure, Vercel, Render)
3. IaC apply steps (Terraform plan, apply)
4. Container deployment steps (Push image, Deploy to K8s/ECS)
5. Environment variables and secrets setup
6. Step-by-step deployment instructions for each component
7. How to test the deployed platform
8. Monitoring and alerting setup in production
9. Fallback plan if deployment fails during the hackathon
10. A pre-deployment checklist
11. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working live pipeline as early as possible.
Ensure the hackathon budget is not exceeded.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the pipeline is shown off perfectly.
```text
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PIPELINE_SPEC: [PASTE PIPELINE_SPEC]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem (Manual, slow, unreliable deployments)
3. Why the problem matters
4. Existing limitations
5. Our DevOps solution
6. How it works (Code → Build → Deploy → Monitor)
7. Technology (AWS, Terraform, Docker, GitHub Actions)
8. Demo (The most important part — show a live commit-to-deploy)
9. Innovation
10. Impact (Time saved, Errors reduced, DORA improvements)
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
Include a backup plan for demo failure (video recording, screenshots, pre-deployed environment).
```

---

### 17. GLOSSARY.md
**Purpose:** To define all DevOps terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Pipeline Spec, and Architecture below, create a Glossary document for a DevOps hackathon project.

PRD: [PASTE PRD]
PIPELINE_SPEC: [PASTE PIPELINE_SPEC]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. DevOps terms (CI, CD, Pipeline, Artifact, Rollback)
2. Cloud terms (Region, AZ, VPC, IAM, Managed Service)
3. IaC terms (Terraform, Module, State, Plan, Apply)
4. Container terms (Docker, Image, Container, Registry, Kubernetes, Pod)
5. Orchestration terms (Cluster, Node, Deployment, Service, Ingress)
6. Observability terms (Log, Metric, Trace, Alert, Dashboard, SLO)
7. DORA metrics (Deployment Frequency, Lead Time, MTTR, Change Failure Rate)
8. Security terms (IAM, Secrets, Encryption, Least Privilege)
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
