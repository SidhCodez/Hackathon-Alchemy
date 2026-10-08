# Category 08: AR / VR / XR / Metaverse

This category focuses on building immersive experiences using tools like **Unity**, **Unreal Engine**, **Blender**, **WebXR**, **Three.js**, **A-Frame**, **ARKit**, **ARCore**, and **Meta Quest SDK**. It focuses purely on **3D environments, spatial computing, interaction design, and immersive storytelling** — the foundation of every AR/VR/XR hackathon.

Here is the exact list of documents we will prepare for the **AR / VR / XR / Metaverse** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core problem, target users, and existing gaps (Immersive focus).
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for an XR experience.
3. **`TRD.md`** (Technical Requirements Document) — Defines the XR stack (Unity, Unreal, WebXR), target device, and performance limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Device → SDK → Scene → Interaction → Backend (XR architecture).
5. **`SCENE_GRAPH.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines the 3D scene hierarchy, objects, prefabs, and assets.
6. **`INTERACTION_SPEC.md`** — (Replaces `API_SPECIFICATION.md`) Defines user interactions (Gaze, Controller, Hand Tracking, Gestures).
7. **`ASSET_PIPELINE.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines 3D models, textures, audio, and optimization workflow.
8. **`SPATIAL_MAPPING.md`** — Defines plane detection, anchors, occlusion, and world understanding.
9. **`PERFORMANCE_BUDGET.md`** — Defines frame rate, polygon count, draw calls, and memory limits.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — Spatial UI design, menus, HUD, and user flow.
11. **`ERROR_HANDLING.md`** — What happens when tracking is lost, a controller disconnects, or performance drops.
12. **`SECURITY.md`** — User data privacy, camera permissions, and microphone access.
13. **`TESTING.md`** — QA plan, device testing, user comfort, and edge cases.
14. **`EVALUATION.md`** — How you measure XR performance (FPS, Comfort, Immersion, Task completion).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Building and deploying to Quest, mobile AR, or WebXR.
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
17. **`GLOSSARY.md`** — Definitions of XR terms (FOV, 6DoF, Hand Tracking, Anchor, Prefab).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the problem and identify what can be solved through immersive technology.
```text
I am participating in an AR/VR/XR/Metaverse hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing solutions
6. Proposed AR/VR/XR solution ideas
7. Core immersive features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential XR platforms and tools that could be used (Unity, Unreal, WebXR, ARKit, ARCore, Meta Quest)

Do not assume I am an experienced XR developer.
Explain XR concepts (6DoF, Hand Tracking, Spatial Anchors, Prefabs) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear XR experience plan with interactions, scenes, and scope.
```text
You are a senior XR product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed XR solution
7. Product goals
8. User stories
9. Functional requirements (Include XR-specific requirements: Interactions, Spatial Mapping, Tracking, Rendering)
10. Non-functional requirements (Comfort, Latency, Frame Rate, Immersion)
11. Core immersive features
12. Nice-to-have features
13. User journeys (How a user enters, interacts, and exits the experience)
14. MVP scope (Which XR feature must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include XR metrics: Task completion, Comfort score, Frame rate, Immersion)
17. Risks and assumptions (Include XR risks: Motion sickness, Tracking loss, Device overheating)

Keep the MVP realistic for a 24-48 hour XR hackathon.
Do not add unnecessary 3D scenes just to make the project sound impressive.
Prioritize features that can actually be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on XR engine, device, and performance.
```text
You are a senior XR engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. XR platform and engine choice (Unity, Unreal, WebXR, ARKit, ARCore — justify the choice)
3. Target device (Meta Quest, HoloLens, Mobile AR, WebXR Browser)
4. Rendering requirements (URP, HDRP, Built-in)
5. Interaction requirements (Controllers, Hand Tracking, Gaze, Gestures)
6. Spatial mapping requirements (Plane detection, Anchors, Occlusion)
7. 3D asset requirements (Poly count, Texture resolution, Format)
8. Audio requirements (Spatial audio, Voice)
9. Performance and latency requirements (Target FPS, Draw calls, Memory)
10. Backend/Cloud requirements (If applicable)
11. Testing requirements (Device testing, User comfort)
12. Deployment requirements

Keep the XR stack simple and realistic for a 24-48 hour hackathon.
Explain all XR concepts in beginner-friendly language.
Do not introduce unnecessary tools.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic XR architecture with clear data flow from device to user experience.
```text
Act as a senior XR architect.
Using the following PRD and TRD, design a realistic hackathon XR architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended XR stack (Engine, SDK, Target device)
2. Complete XR architecture diagram (Text-based, showing User → Device → SDK → Scene → Interaction → Backend)
3. Scene architecture (Scenes, Prefabs, Controllers)
4. Interaction architecture (Input system, Hand tracking, Controllers)
5. Spatial mapping architecture (Anchors, Plane detection)
6. Rendering architecture (Pipeline, Shaders, Lighting)
7. Asset pipeline architecture (Import, Optimization, Loading)
8. Audio architecture (Spatial audio, Voice)
9. Backend/Cloud architecture (If applicable)
10. Data flow (How a user action becomes a scene change)
11. Performance considerations
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools. Prefer a simple architecture that can be explained easily to judges.
```

---

### 5. SCENE_GRAPH.md
**Purpose:** To define the 3D scene hierarchy, objects, prefabs, and assets.
```text
Act as a senior XR scene designer.
Using the PRD and System Architecture below, design the scene graph for this XR hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Scene list (Main Menu, Experience, Settings, etc.)
2. Scene hierarchy (Parent-Child relationships)
3. GameObjects/Actors (Name, Type, Purpose)
4. Prefabs (Reusable objects)
5. UI elements (Canvas, Menus, HUD)
6. Lighting setup (Directional, Point, Ambient)
7. Camera setup (Main Camera, XR Rig)
8. Interaction zones (Where the user can interact)
9. Spawn points and anchors
10. Example scene layout
11. A checklist for verifying the scene before the demo

Explain why each object exists.
Keep the scene simple enough for a beginner hackathon team to understand and maintain.
```

---

### 6. INTERACTION_SPEC.md
**Purpose:** To define user interactions (Gaze, Controller, Hand Tracking, Gestures).
```text
You are a senior XR interaction designer.
Using the PRD and Scene Graph below, create an Interaction Specification document for this XR hackathon project.

PRD: [PASTE PRD]
SCENE_GRAPH: [PASTE SCENE_GRAPH]

Provide:
1. Interaction methods (Controllers, Hand Tracking, Gaze, Voice, Gestures)
2. Primary interaction (Select, Grab, Point, Teleport)
3. Secondary interaction (Menu, Rotate, Scale, Throw)
4. Input mappings (Button, Trigger, Grip, Joystick)
5. Hand tracking gestures (Pinch, Point, Grab)
6. Gaze interaction (Dwell time, Retical)
7. Haptic feedback (Vibration patterns)
8. Audio feedback (Sounds for interactions)
9. Visual feedback (Highlight, Outline, Cursor)
10. Interaction states (Idle, Hover, Selected, Active)
11. Example interaction flow
12. A checklist for verifying interactions before the demo

Explain each interaction in beginner-friendly language.
Keep the interaction design simple and intuitive for a hackathon.
```

---

### 7. ASSET_PIPELINE.md
**Purpose:** To define 3D models, textures, audio, and optimization workflow.
```text
Act as a senior XR technical artist.
Using the PRD and Scene Graph below, create an Asset Pipeline document for this XR hackathon project.

PRD: [PASTE PRD]
SCENE_GRAPH: [PASTE SCENE_GRAPH]

Provide:
1. 3D model requirements (Format, Poly count, Scale)
2. Texture requirements (Resolution, Format, Compression)
3. Material and shader requirements
4. Animation requirements (Rigging, Clips, Blend trees)
5. Audio requirements (Format, Spatial audio, Compression)
6. Asset import workflow (Blender → Engine)
7. Asset optimization (LODs, Occlusion culling, Batching)
8. Naming conventions
9. Folder structure for assets
10. Free asset sources (Sketchfab, Poly Haven, Mixamo)
11. A checklist for verifying assets before the demo

Explain each concept in beginner-friendly language.
Keep the asset pipeline simple and realistic for a hackathon.
```

---

### 8. SPATIAL_MAPPING.md
**Purpose:** To define plane detection, anchors, occlusion, and world understanding.
```text
You are a senior AR/XR spatial computing engineer.
Using the PRD and System Architecture below, create a Spatial Mapping document for this XR hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Spatial mapping requirements (Plane detection, Mesh, Depth)
2. Anchor types (Plane, Point, Image, Object)
3. Occlusion handling (Real-world objects blocking virtual objects)
4. Raycasting (For placement and interaction)
5. World origin and coordinate system
6. Tracking modes (3DoF, 6DoF, Inside-out, Outside-in)
7. Persistent anchors (If applicable)
8. Lighting estimation (If applicable)
9. Limitations of spatial mapping on target device
10. A checklist for verifying spatial mapping before the demo

Explain each concept in beginner-friendly language.
Keep the spatial mapping simple and realistic for a hackathon.
```

---

### 9. PERFORMANCE_BUDGET.md
**Purpose:** To define frame rate, polygon count, draw calls, and memory limits.
```text
Act as a senior XR performance engineer.
Using the PRD and Scene Graph below, create a Performance Budget document for this XR hackathon project.

PRD: [PASTE PRD]
SCENE_GRAPH: [PASTE SCENE_GRAPH]

Provide:
1. Target frame rate (72Hz, 90Hz, 120Hz)
2. Polygon budget (Total, Per object)
3. Draw call budget
4. Texture memory budget
5. Material and shader budget
6. Lighting budget (Real-time vs Baked)
7. Physics budget
8. Audio budget
9. Memory budget (RAM, VRAM)
10. Performance profiling tools (Unity Profiler, RenderDoc)
11. Optimization techniques (LODs, Batching, Occlusion culling)
12. A checklist for verifying performance before the demo

Explain each concept in beginner-friendly language.
Keep the performance budget realistic for a hackathon.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define spatial UI design, menus, HUD, and user flow.
```text
Act as a senior spatial UI/UX designer.
Using the PRD and System Architecture below, create a UI Specification document for an XR hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spatial spacing)
2. Spatial UI components (World-space menus, HUD, Panels)
3. Component hierarchy (Menus, Buttons, Sliders, Cards)
4. Screen-by-screen breakdown (Main Menu, Experience, Settings, Exit)
5. Interaction states (Idle, Hover, Selected, Active)
6. Loading states (Skeletons, spinners)
7. Error states (Tracking lost, Controller disconnected)
8. Empty states (No content yet)
9. Comfort considerations (Distance, Size, Placement)
10. Accessibility considerations (Contrast, Text size, Audio cues)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the core immersive journey.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when tracking is lost, a controller disconnects, or performance drops.
```text
You are a senior XR developer.
Using the System Architecture and Interaction Spec below, create an Error Handling document for an XR hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
INTERACTION_SPEC: [PASTE INTERACTION_SPEC]

Provide:
1. Common failure modes (Tracking loss, Controller disconnect, Low battery, Performance drop)
2. Tracking error handling (Recenter, Pause, Fallback)
3. Controller error handling (Pause, Notify user, Switch to hand tracking)
4. Spatial mapping error handling (Re-scan, Anchor loss)
5. Performance error handling (Reduce quality, Pause rendering)
6. Frontend error display (In-world notifications, HUD alerts)
7. Recovery procedures (Auto-recenter, Manual reset)
8. A checklist for developers to verify error handling before the demo

Focus on making the experience resilient so the live demo does not crash.
Explain each error handling approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** To secure user data privacy, camera permissions, and microphone access.
```text
Act as an XR security and privacy engineer.
Using the System Architecture and PRD below, create a Security document for an XR hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PRD: [PASTE PRD]

Provide:
1. Camera and microphone permissions (When and why)
2. User data privacy (What data is collected?)
3. Spatial data privacy (Room mapping, Location data)
4. Voice data privacy (If using voice input)
5. Biometric data (If using eye tracking, hand tracking)
6. Data storage and transmission security
7. Backend security (If applicable)
8. Compliance considerations (GDPR, COPPA if applicable)
9. A pre-submission privacy checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist for XR experiences, device testing, and edge cases.
```text
Act as a QA engineer specializing in XR applications.
Using the PRD and Interaction Spec below, create a Testing document for an XR hackathon project.

PRD: [PASTE PRD]
INTERACTION_SPEC: [PASTE INTERACTION_SPEC]

Provide:
1. Testing strategy for XR
2. Device testing (Headset, Controllers, Hand tracking)
3. Scene testing (Does every scene load correctly?)
4. Interaction testing (Do interactions work as intended?)
5. Spatial mapping testing (Plane detection, Anchors)
6. Performance testing (FPS, Comfort)
7. Audio testing (Spatial audio, Volume)
8. Edge cases (Tracking loss, Controller disconnect, Low battery)
9. User comfort testing (Motion sickness, Fatigue)
10. User acceptance testing checklist
11. A manual testing checklist for the demo
12. How to document known XR limitations for judges

Keep the testing plan simple enough for beginner XR developers to execute under time pressure.
```

---

### 14. EVALUATION.md
**Purpose:** To define how the team measures XR performance and prepares for judge questions.
```text
You are an XR evaluation expert.
Using the PRD and Interaction Spec below, create an Evaluation document for an XR hackathon project.

PRD: [PASTE PRD]
INTERACTION_SPEC: [PASTE INTERACTION_SPEC]

Provide:
1. Evaluation metrics (FPS, Comfort score, Task completion, Immersion)
2. Evaluation methods (User testing, Surveys, Profiling)
3. Benchmarking (What is the baseline?)
4. Known limitations of the XR experience
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about XR and how to answer them

Focus on demonstrating that the team understands the experience's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To define how to build and deploy to Quest, mobile AR, or WebXR.
```text
Act as an XR deployment engineer.
Using the System Architecture and PRD below, create a Deployment document for an XR hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PRD: [PASTE PRD]

Provide:
1. Target platform (Meta Quest, Mobile AR, WebXR)
2. Build settings (Development build, Release build)
3. Deployment steps (SideQuest, ADB, TestFlight, Web hosting)
4. Environment variables for production
5. How to test the deployed experience
6. Fallback plan if deployment fails during the hackathon
7. A pre-deployment checklist
8. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working live demo as early as possible.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the XR experience works perfectly.
```text
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
INTERACTION_SPEC: [PASTE INTERACTION_SPEC]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem
3. Why the problem matters
4. Existing limitations
5. Our XR solution
6. How it works (Device → Scene → Interaction)
7. Technology (Unity, Unreal, WebXR, Quest)
8. Demo (The most important part — show the live immersive experience)
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
Include a backup plan for hardware failure during the demo (video recording, screenshots).
```

---

### 17. GLOSSARY.md
**Purpose:** To define all XR terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Interaction Spec, and Architecture below, create a Glossary document for an XR hackathon project.

PRD: [PASTE PRD]
INTERACTION_SPEC: [PASTE INTERACTION_SPEC]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. XR terms (AR, VR, MR, XR, Metaverse, Immersion, Presence)
2. Tracking terms (3DoF, 6DoF, Inside-out, Outside-in, Hand Tracking, Eye Tracking)
3. Interaction terms (Gaze, Controller, Gesture, Haptic, Raycast)
4. Spatial terms (Anchor, Plane Detection, Occlusion, Spatial Mapping, World Origin)
5. Rendering terms (FOV, Frame Rate, Draw Call, LOD, Shader)
6. Engine terms (Unity, Unreal, Prefab, GameObject, Scene)
7. Comfort terms (Motion Sickness, Latency, Comfort Score)
8. Project-specific terms (Any custom terminology used in the PRD)
9. Acronyms and abbreviations

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