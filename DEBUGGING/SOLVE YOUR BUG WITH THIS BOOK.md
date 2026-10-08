# Category 17: Debugging (Revised Format)

**Unique Framework: The 6 Debugging Pillars**
*(Not phased. Each pillar represents a stage in the debugging lifecycle — you move through them sequentially when hunting a bug, but can jump back if new evidence emerges.)*

---

## The 6 Debugging Pillars

| # | Pillar | Question It Answers | Focus |
| :--- | :--- | :--- | :--- |
| 1 | **Detect & Define** | What is broken and how bad is it? | Symptoms, Impact, Severity |
| 2 | **Reproduce & Isolate** | Can we make it happen reliably? | Minimal Repro, Environment |
| 3 | **Instrument & Observe** | What is the system telling us? | Logs, Traces, Metrics |
| 4 | **Hypothesize & Test** | What do we think is wrong? | 5 Whys, Bisect, Experiments |
| 5 | **Resolve & Verify** | Is it actually fixed? | Fix, Regression Tests, Deploy |
| 6 | **Prevent & Learn** | How do we stop this forever? | Post-Mortem, Monitoring, Debt |

---

## Pillar 1: Detect & Define

### 1. `SYMPTOM_REPORT.md`
```text
You are a senior debugging mentor.
Help me clearly define the bug I'm facing.

INPUT:
[PASTE BUG DESCRIPTION, ERROR LOG, OR OBSERVED BEHAVIOR]

Provide:
1. Bug title (Short, specific)
2. Symptom summary (What is happening?)
3. Expected behavior (What should happen?)
4. Actual behavior (What is happening instead?)
5. First observed (When did it start?)
6. Frequency (Always, Sometimes, Rare)
7. Reproduction reliability (Can we make it happen?)
8. User-visible impact
9. Affected components
10. Related errors or warnings
11. What is NOT the problem (Ruled out)

Explain in beginner-friendly language.
Do not guess the cause yet — just define the symptom precisely.
```

### 2. `IMPACT_ASSESSMENT.md`
```text
You are an incident severity expert.
Assess the impact of this bug.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]

Provide:
1. Severity level (P0: Critical, P1: High, P2: Medium, P3: Low)
2. Users affected (How many? Which segments?)
3. Business impact (Revenue, Trust, Compliance)
4. Technical impact (Data loss, Downtime, Corruption)
5. Blast radius (What else might break?)
6. Time sensitivity (How urgent?)
7. Workarounds available (Can users continue?)
8. Escalation required (Who needs to know?)
9. Fix priority
10. A triage checklist

Explain severity in beginner-friendly language.
Keep the assessment honest — do not exaggerate or minimize.
```

---

## Pillar 2: Reproduce & Isolate

### 3. `REPRODUCTION_STEPS.md`
```text
You are a senior QA engineer specializing in bug reproduction.
Create clear reproduction steps for this bug.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]

Provide:
1. Preconditions (User state, Data state, Config)
2. Step-by-step reproduction steps (Numbered, precise)
3. Expected result at each step
4. Actual result at each step
5. Minimal reproducible case (Smallest possible)
6. Frequency of reproduction
7. Any logs or stack traces
8. Screenshots or recordings needed
9. Variables to test (Browser, OS, Data, Timing)
10. A reliability checklist

If the bug is not reproducible, list the top 3 reasons why and how to narrow it down.
Explain each step in beginner-friendly language.
```

### 4. `ENVIRONMENT_MATRIX.md`
```text
You are a systems engineer specializing in environmental factors.
Create an environment matrix to isolate the bug.

INPUTS:
Reproduction Steps: [PASTE REPRODUCTION_STEPS]

Provide a matrix testing:
1. Operating systems (Windows, Mac, Linux)
2. Browsers (Chrome, Firefox, Safari, Edge)
3. Browser versions (Latest, Previous, Specific)
4. Devices (Desktop, Tablet, Mobile)
5. Network conditions (WiFi, 4G, 3G, Offline)
6. User roles (Admin, User, Guest)
7. Data states (Empty, Populated, Edge values)
8. Time zones and locales
9. Feature flags or config variations
10. Environment (Dev, Staging, Production)

For each dimension:
- Does the bug reproduce? (Yes/No)
- What does this tell us?

Highlight the narrowest environment where the bug reproduces.
Explain in beginner-friendly language.
```

### 5. `BISECT_PLAN.md`
```text
You are a senior debugging engineer.
Create a bisection plan to isolate when the bug was introduced.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]

Provide:
1. What is bisecting? (Beginner-friendly explanation)
2. Last known good version
3. First known bad version
4. Commits or changes in between
5. Bisect strategy (Git bisect, Manual, Code-level)
6. Step-by-step bisect process
7. What to look for at each step
8. How to verify "good" vs "bad" at each step
9. What to do if bisect is inconclusive
10. Alternative isolation techniques (Comment out, Feature flag)
11. A checklist for isolating the change

If Git bisect is not applicable, suggest alternatives (manual code review, log diffing).
```

---

## Pillar 3: Instrument & Observe

### 6. `OBSERVABILITY_SETUP.md`
```text
You are a senior observability engineer.
Help me set up observability to understand this bug.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]
Environment Matrix: [PASTE ENVIRONMENT_MATRIX]

Provide:
1. What observability means (Beginner explanation)
2. Logs — what to capture and at what level
3. Metrics — what to measure (Latency, Error rate, Throughput)
4. Traces — how to follow a request end-to-end
5. Correlation IDs — how to link logs, metrics, traces
6. Tools to use (Console, DevTools, APM, Log aggregators)
7. Where to place instrumentation
8. What NOT to instrument (Avoid noise)
9. Real-time monitoring setup
10. Alerting on the bug recurrence
11. A setup checklist

Keep the observability setup minimal and targeted.
Explain each concept in beginner-friendly language.
```

### 7. `LOG_TRACE_STRATEGY.md`
```text
You are a senior SRE.
Create a log and trace strategy specific to this bug.

INPUTS:
Observability Setup: [PASTE OBSERVABILITY_SETUP]
Symptom Report: [PASTE SYMPTOM_REPORT]

Provide:
1. Log levels to use (DEBUG, INFO, WARN, ERROR)
2. What to log at each level (Specific to this bug)
3. Log format (JSON, Text, Structured)
4. Required fields (Timestamp, Request ID, User ID, Component)
5. What NEVER to log (PII, Passwords, Tokens)
6. Trace spans for the affected request flow
7. Sampling strategy (If high volume)
8. Where logs are stored
9. Retention policy
10. Example log entries (Before/After fix)
11. A checklist to verify logging

Focus logs on the bug's suspected area.
Explain each concept in beginner-friendly language.
```

### 8. `DEVTOOLS_WORKFLOW.md`
```text
You are a browser and runtime debugging expert.
Create a debugging workflow using DevTools.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]
Environment Matrix: [PASTE ENVIRONMENT_MATRIX]

Provide:
1. Chrome DevTools panels to use (Elements, Console, Sources, Network, Performance, Application)
2. Breakpoint strategy (Line, Conditional, DOM, Event listener)
3. Watch expressions
4. Call stack analysis
5. Network tab investigation (Headers, Payload, Response, Timing)
6. Performance profiling (Flamegraph, Memory)
7. Application tab (Storage, Cookies, Cache)
8. Console debugging techniques
9. Mobile remote debugging
10. Common DevTools mistakes
11. A step-by-step debugging session plan

Explain each panel and technique in beginner-friendly language.
Tailor the workflow to the specific bug.
```

---

## Pillar 4: Hypothesize & Test

### 9. `HYPOTHESIS_LOG.md`
```text
You are a senior debugging mentor.
Create a hypothesis log for this bug.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]
Observability Setup: [PASTE OBSERVABILITY_SETUP]

For each hypothesis, provide:
1. Hypothesis statement (If X is true, then Y explains the bug)
2. Reasoning (Why we believe this)
3. Evidence needed to confirm
4. Evidence needed to reject
5. Experiment to run
6. Expected result if true
7. Expected result if false
8. Actual result
9. Conclusion (Confirmed, Rejected, Inconclusive)
10. Next hypothesis to explore

List at least 5 potential hypotheses.
Rank them by likelihood.
Explain in beginner-friendly language.
```

### 10. `ROOT_CAUSE_ANALYSIS.md`
```text
You are a senior engineer specializing in root cause analysis.
Identify the root cause of this bug.

INPUTS:
Hypothesis Log: [PASTE HYPOTHESIS_LOG]
Symptom Report: [PASTE SYMPTOM_REPORT]

Provide:
1. Problem statement
2. 5 Whys analysis (Ask "Why?" 5 times)
3. Fishbone diagram (Categories: Code, Data, Config, Environment, Human)
4. Timeline of events
5. Root cause (The actual reason)
6. Contributing factors (What made it worse?)
7. Why tests missed it
8. Why monitoring missed it
9. Why the code was written this way (Context)
10. Corrective actions (Immediate fix)
11. Preventive actions (How to prevent recurrence)

Do not stop at the first symptom — go deep.
Focus on preventing recurrence, not just fixing the symptom.
Explain in beginner-friendly language.
```

### 11. `EXPERIMENT_TRACKER.md`
```text
You are a scientific debugging mentor.
Create an experiment tracker for this bug.

INPUTS:
Hypothesis Log: [PASTE HYPOTHESIS_LOG]

Provide a tracker template:
1. Experiment ID
2. Hypothesis being tested
3. Change made (Code, Config, Data)
4. Environment
5. Expected outcome
6. Actual outcome
7. Time taken
8. Side effects observed
9. Conclusion
10. Next experiment

Include at least 5 experiment examples.
Track everything — no experiment is wasted.
Explain in beginner-friendly language.
```

---

## Pillar 5: Resolve & Verify

### 12. `FIX_IMPLEMENTATION.md`
```text
You are a senior engineer.
Design the fix for this bug.

INPUTS:
Root Cause Analysis: [PASTE ROOT_CAUSE_ANALYSIS]

Provide:
1. Fix summary (One sentence)
2. Files to change
3. Code changes (High-level)
4. Why this fix addresses the root cause
5. Why we chose this fix over alternatives
6. Side effects to watch for
7. Rollback plan
8. Feature flag (If applicable)
9. Documentation updates needed
10. Commit message template
11. A pre-fix checklist

Keep the fix minimal and targeted.
Do not refactor unrelated code.
Explain in beginner-friendly language.
```

### 13. `REGRESSION_TEST_PLAN.md`
```text
You are a QA engineer specializing in regression testing.
Create a regression test plan for this fix.

INPUTS:
Fix Implementation: [PASTE FIX_IMPLEMENTATION]
Root Cause Analysis: [PASTE ROOT_CAUSE_ANALYSIS]

Provide:
1. Verification testing (Does the fix work?)
2. Regression testing (What might break?)
3. Edge case testing (Boundary conditions)
4. Integration testing (Cross-component)
5. Load testing (If applicable)
6. Test cases specific to this bug
7. Test cases for related functionality
8. Automated test coverage gaps
9. Manual test checklist
10. Sign-off criteria
11. A checklist to prevent the bug from shipping again

Focus on verifying the fix without introducing new bugs.
Explain in beginner-friendly language.
```

### 14. `DEPLOYMENT_PLAN.md`
```text
You are a DevOps engineer.
Create a deployment plan for this fix.

INPUTS:
Fix Implementation: [PASTE FIX_IMPLEMENTATION]
Regression Test Plan: [PASTE REGRESSION_TEST_PLAN]

Provide:
1. Pre-deployment verification
2. Deployment strategy (Blue-Green, Canary, Rolling)
3. Rollback plan
4. Feature flag strategy
5. Step-by-step deployment
6. Post-deployment monitoring
7. User communication (If needed)
8. Success criteria
9. Post-deployment verification
10. Deployment checklist
11. Common deployment mistakes to avoid

Keep the deployment simple and reversible.
Explain in beginner-friendly language.
```

---

## Pillar 6: Prevent & Learn

### 15. `POST_MORTEM.md`
```text
You are a senior incident review lead.
Create a blameless post-mortem for this bug.

INPUTS:
Root Cause Analysis: [PASTE ROOT_CAUSE_ANALYSIS]
Fix Implementation: [PASTE FIX_IMPLEMENTATION]

Provide:
1. Incident summary
2. Timeline of events
3. Root cause
4. Contributing factors
5. Impact (Users, Revenue, Trust)
6. What went well
7. What went wrong
8. Where we got lucky
9. Action items (Preventive, Detective, Mitigative)
10. Owners for each action item
11. Lessons learned

Blameless tone — focus on systems, not people.
Make action items specific, measurable, and time-bound.
Explain in beginner-friendly language.
```

### 16. `PREVENTION_CHECKLIST.md`
```text
You are a senior engineering lead.
Create a prevention checklist based on this bug.

INPUTS:
Post-Mortem: [PASTE POST_MORTEM]
Root Cause Analysis: [PASTE ROOT_CAUSE_ANALYSIS]

Provide:
1. Code-level prevention (Patterns, Linting rules, Type safety)
2. Test-level prevention (New tests, Coverage targets)
3. Monitoring prevention (New alerts, Dashboards)
4. Process prevention (Code review, Staging gates)
5. Documentation prevention (Runbooks, ADRs)
6. Architecture prevention (Design changes)
7. Dependency prevention (Updates, Pinning)
8. Team prevention (Knowledge sharing, Onboarding)
9. Tooling prevention (CI/CD improvements)
10. A 30-day follow-up checklist

Explain each prevention in beginner-friendly language.
Prioritize actions by impact and effort.
```

### 17. `TECH_DEBT_LOG.md`
```text
You are a senior engineer.
Log tech debt related to this bug.

INPUTS:
Post-Mortem: [PASTE POST_MORTEM]
Fix Implementation: [PASTE FIX_IMPLEMENTATION]

Provide:
1. Tech debt item
2. Origin (Why the shortcut was taken)
3. Impact on this bug
4. Impact on future velocity
5. Interest rate (How fast it grows)
6. Priority (High, Medium, Low)
7. Fix effort estimate
8. When to fix (Now, Next, Later, Never)
9. Owner
10. Related design decisions
11. A review cadence

Be honest about debt.
Do not accumulate — schedule fixes.
Explain in beginner-friendly language.
```

---

## Support Documents

### 18. `DEBUG_TOOLING.md`
```text
You are a debugging tools expert.
List all debugging tools relevant to this bug.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]

Provide:
1. Frontend tools (Chrome DevTools, React DevTools)
2. Backend tools (Node Inspector, Postman)
3. Database tools (DB Client, Query Profiler)
4. Network tools (Wireshark, Network tab)
5. Performance tools (Lighthouse, Profiler)
6. Error tracking (Sentry, LogRocket)
7. Logging tools (Winston, Loguru)
8. APM tools (New Relic, Datadog)
9. Which tools to use for this specific bug
10. Setup instructions
11. Common debugging workflows

Explain each tool in beginner-friendly language.
Keep the list minimal — only what is needed.
```

### 19. `GLOSSARY.md`
```text
You are a technical writer specializing in debugging.
Create a Glossary document.

INPUTS:
Symptom Report: [PASTE SYMPTOM_REPORT]
Root Cause Analysis: [PASTE ROOT_CAUSE_ANALYSIS]

Provide definitions for:
1. Debugging terms (Breakpoint, Stack Trace, Watch, Step Over)
2. Bug terms (Heisenbug, Race Condition, Memory Leak, Null Pointer)
3. Root cause terms (5 Whys, Fishbone, Regression)
4. Tooling terms (DevTools, Profiler, APM, Log Aggregator)
5. Metrics terms (MTTR, MTBF, Error Rate, Coverage)
6. Testing terms (Regression Test, Edge Case)
7. Project-specific terms
8. Acronyms

For each term:
- Simple definition (Beginner-friendly)
- Why it matters
- Example usage

Keep definitions concise.
```

---

## Footer (End of Category)

### 
### Thank You

Thank you for using this guide. Go build something amazing!

**Made by Siddiq**

*Credit: Hackathon Alchemy*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**

---
