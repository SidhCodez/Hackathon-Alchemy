# Category 12: Creative / Media / Gaming

This category focuses on building interactive experiences using tools like **Unity**, **Unreal Engine**, **Godot**, **WebGL**, **Three.js**, **Blender**, and **Adobe Creative Suite**. It focuses purely on **game design, interactive media, narrative, and digital art** — the foundation of every Creative/Media/Gaming hackathon.

Here is the exact list of documents we will prepare for the **Creative / Media / Gaming** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core creative/media problem, target audience, and existing gaps.
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for a creative project.
3. **`TRD.md`** (Technical Requirements Document) — Defines the tech stack (Unity, Unreal, WebGL), target platform, and performance limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of the system architecture (Game engine, backend, asset pipeline).
5. **`GAME_DESIGN_DOC.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines core mechanics, game loop, levels, and player progression.
6. **`NARRATIVE_SPEC.md`** — (Replaces `API_SPECIFICATION.md`) Defines story structure, characters, dialogue, and branching paths.
7. **`ASSET_PIPELINE.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines 3D models, textures, animations, and asset optimization.
8. **`SOUND_DESIGN.md`** — Defines music, sound effects, voice acting, and audio implementation.
9. **`INTERACTION_SPEC.md`** — Defines player controls, input mapping, and interaction states.

### Phase 3: Execution, Quality & Security
10. **`UI_SPEC.md`** — HUD design, menus, and user flow.
11. **`ERROR_HANDLING.md`** — What happens when assets fail to load, frame rate drops, or input breaks.
12. **`SECURITY.md`** — Asset protection, anti-cheat, and user data privacy.
13. **`TESTING.md`** — QA plan, playtesting, bug reporting, and edge cases.
14. **`EVALUATION.md`** — How you measure creative impact (Player engagement, FPS, Completion rate).

### Phase 4: Delivery & Presentation
15. **`DEPLOYMENT.md`** — Building and deploying to target platforms (WebGL, Steam, Mobile, Console).
16. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
17. **`GLOSSARY.md`** — Definitions of game and media terms (FPS, Shader, Prefab, Rigging, Foley).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the creative/gaming problem and identify what experience needs to be built.
```text
I am participating in a Creative/Media/Gaming hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual creative problem being solved
2. Target audience (Players, Viewers, Users)
3. User pain points
4. Existing ways people might solve this problem
5. Limitations of existing creative solutions
6. Proposed creative/media/gaming solution ideas
7. Core creative features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential tools and platforms that could be used (Unity, Unreal, Godot, Blender, WebGL)

Do not assume I am an experienced game developer or designer.
Explain creative concepts (Game Loop, Shaders, Prefabs, Narrative Design) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear creative product plan with features, mechanics, and scope.
```text
You are a senior creative product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target audience
5. User pain points
6. Proposed creative solution
7. Product goals
8. User stories
9. Functional requirements (Include creative-specific requirements: Mechanics, Levels, Narrative, Audio)
10. Non-functional requirements (Performance, FPS, Load Time)
11. Core creative features
12. Nice-to-have features
13. User journeys (Player/User experience flow)
14. MVP scope (Which mechanic must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include creative metrics: Engagement, Completion rate, Fun factor)
17. Risks and assumptions (Include creative risks: Scope creep, Asset delays, Performance drops)

Keep the MVP realistic for a 24-48 hour creative hackathon.
Do not add unnecessary mechanics just to make the project sound impressive.
Prioritize features that can actually be demonstrated live.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on game engine, platform, and performance.
```text
You are a senior game engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Game engine choice (Unity, Unreal, Godot, WebGL — justify the choice)
3. Target platform (PC, Mobile, Web, Console)
4. Rendering requirements (2D, 3D, Art style)
5. Physics requirements
6. Input requirements (Keyboard, Controller, Touch, Gesture)
7. Audio requirements
8. Asset pipeline requirements
9. Performance and latency requirements (Target FPS, Memory limits)
10. Backend/Multiplayer requirements (If applicable)
11. Testing requirements
12. Deployment requirements

Keep the game stack simple and realistic for a 24-48 hour hackathon.
Explain all game dev concepts in beginner-friendly language.
Do not introduce unnecessary engines or tools.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic game/media architecture with clear data flow.
```text
Act as a senior game architect.
Using the following PRD and TRD, design a realistic hackathon game architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended game engine stack (Engine, Language, Tools)
2. Complete architecture diagram (Text-based, showing Input → Game Loop → Systems → Rendering → Output)
3. Core systems architecture (Input, Physics, AI, Audio, UI)
4. Scene management architecture
5. Asset pipeline architecture
6. Data persistence architecture (Save games, High scores)
7. Multiplayer/Backend architecture (If applicable)
8. Data flow (How a player action becomes a visual result)
9. Performance considerations
10. Folder structure
11. Major components
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools. Prefer a simple architecture that can be explained easily to judges.
```

---

### 5. GAME_DESIGN_DOC.md
**Purpose:** To define core mechanics, game loop, levels, and player progression.
```text
Act as a senior game designer.
Using the PRD and System Architecture below, create a Game Design Document (GDD) for this creative hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Core gameplay loop (What does the player do repeatedly?)
2. Game mechanics (Movement, Combat, Puzzle, Exploration)
3. Player progression (Levels, Upgrades, Rewards)
4. Level design (Layout, Objectives, Difficulty curve)
5. Game states (Menu, Playing, Paused, Game Over, Victory)
6. Win/Lose conditions
7. Enemy/NPC behavior (If applicable)
8. Scoring system
9. Replayability factors
10. Example player session (Step-by-step)
11. A checklist for verifying game design before the demo

Explain each mechanic in beginner-friendly language.
Keep the design simple and achievable for a hackathon.
Focus on one core mechanic done well, rather than many done poorly.
```

---

### 6. NARRATIVE_SPEC.md
**Purpose:** To define story structure, characters, dialogue, and branching paths.
```text
You are a senior narrative designer.
Using the PRD and Game Design Document below, create a Narrative Specification document for this creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Story premise (One-paragraph summary)
2. Setting and world-building
3. Main characters (Protagonist, Antagonist, Supporting)
4. Character arcs (Brief)
5. Story structure (Beginning, Middle, End)
6. Dialogue system (Linear, Branching, Choices)
7. Branching paths (If applicable)
8. Environmental storytelling
9. Narrative pacing (How story is revealed)
10. Example dialogue script (For one scene)
11. A checklist for verifying narrative before the demo

If the project is not narrative-driven (e.g., a tool or abstract game), explain how narrative elements can still enhance the experience.
Keep the narrative simple and impactful for a hackathon.
```

---

### 7. ASSET_PIPELINE.md
**Purpose:** To define 3D models, textures, animations, and asset optimization.
```text
Act as a senior technical artist.
Using the PRD and Game Design Document below, create an Asset Pipeline document for this creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Art style (Realistic, Stylized, Pixel, Low-poly)
2. 3D model requirements (Poly count, Format, Scale)
3. 2D asset requirements (Sprites, UI, Textures)
4. Texture requirements (Resolution, Format, Compression)
5. Animation requirements (Rigging, Clips, Blend trees)
6. VFX requirements (Particles, Shaders, Post-processing)
7. Asset import workflow (Blender → Engine)
8. Asset optimization (LODs, Batching, Atlasing)
9. Naming conventions
10. Folder structure for assets
11. Free asset sources (Kenney, Sketchfab, Mixamo, itch.io)
12. A checklist for verifying assets before the demo

Explain each concept in beginner-friendly language.
Keep the asset pipeline simple and realistic for a hackathon.
Prioritize free and fast assets over custom work.
```

---

### 8. SOUND_DESIGN.md
**Purpose:** To define music, sound effects, voice acting, and audio implementation.
```text
You are a senior sound designer.
Using the PRD and Game Design Document below, create a Sound Design document for this creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Audio style (Orchestral, Electronic, Ambient, Retro)
2. Music requirements (Menu, Gameplay, Boss, Victory)
3. Sound effects list (Movement, Combat, UI, Environment)
4. Voice acting requirements (If applicable)
5. Audio implementation (Engine audio system)
6. Spatial audio (3D sound, Distance, Occlusion)
7. Audio mixing (Volume levels, Ducking)
8. Audio optimization (Compression, Format, Streaming)
9. Free audio sources (Freesound, Pixabay, incompetech, ZapSplat)
10. A checklist for verifying audio before the demo

Explain each concept in beginner-friendly language.
Keep the sound design simple and impactful for a hackathon.
Prioritize free and fast audio assets over custom work.
```

---

### 9. INTERACTION_SPEC.md
**Purpose:** To define player controls, input mapping, and interaction states.
```text
You are a senior interaction designer.
Using the PRD and Game Design Document below, create an Interaction Specification document for this creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Input methods (Keyboard, Mouse, Controller, Touch)
2. Input mappings (What button does what)
3. Character/Player movement (Walk, Run, Jump, Crouch)
4. Camera controls (Follow, Orbit, First-person, Third-person)
5. Interaction mechanics (Select, Grab, Use, Talk)
6. Combat mechanics (Attack, Block, Dodge — if applicable)
7. UI interactions (Menu navigation, Inventory)
8. Feedback (Visual, Audio, Haptic)
9. Input buffering and responsiveness
10. Accessibility controls (Remappable keys, Sensitivity)
11. Example interaction flow
12. A checklist for verifying interactions before the demo

Explain each interaction in beginner-friendly language.
Keep the interaction design simple and intuitive for a hackathon.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 10. UI_SPEC.md
**Purpose:** To define the HUD design, menus, and user flow.
```text
Act as a senior game UI/UX designer.
Using the PRD and Game Design Document below, create a UI Specification document for a creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Design system (Colors, typography, spacing)
2. HUD design (Health, Score, Ammo, Minimap)
3. Menu screens (Main Menu, Pause, Settings, Game Over)
4. Component hierarchy
5. Screen-by-screen breakdown
6. Interaction states (Idle, Hover, Selected, Disabled)
7. Loading states (Skeletons, progress bars)
8. Error states (Save failed, Connection lost)
9. Empty states (No saves yet)
10. Responsive design guidelines (PC, Mobile)
11. Accessibility considerations (Contrast, Text size, Color blindness)

Keep the UI simple, clean, and realistic for a 24-48 hour hackathon.
Focus on demonstrating the core gameplay journey.
```

---

### 11. ERROR_HANDLING.md
**Purpose:** To define what happens when assets fail to load, frame rate drops, or input breaks.
```text
You are a senior game developer.
Using the System Architecture and Game Design Document below, create an Error Handling document for a creative hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Common failure modes (Asset load failure, Frame drop, Input loss, Crash)
2. Asset loading error handling (Fallback assets, Retry)
3. Performance error handling (Dynamic resolution, Quality scaling)
4. Input error handling (Reconnect controller, Reset input)
5. Save/Load error handling
6. Audio error handling (Missing sound, Fallback silence)
7. Frontend error display (Error modals, In-game notifications)
8. Crash recovery (Auto-save, State restore)
9. A checklist for developers to verify error handling before the demo

Focus on making the game resilient so the live demo does not crash.
Explain each error handling approach in beginner-friendly language.
```

---

### 12. SECURITY.md
**Purpose:** To secure asset protection, anti-cheat, and user data privacy.
```text
Act as a game security engineer.
Using the System Architecture and PRD below, create a Security document for a creative hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PRD: [PASTE PRD]

Provide:
1. Asset protection (Anti-rip, Encryption, Obfuscation)
2. Anti-cheat (If multiplayer or leaderboard)
3. Save file integrity (Prevent tampering)
4. User data privacy (What data is collected?)
5. Network security (If multiplayer)
6. API key protection (If using external services)
7. Age-appropriate content (If targeting younger audiences)
8. Compliance considerations (COPPA, GDPR for games)
9. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each concept in beginner-friendly language.
```

---

### 13. TESTING.md
**Purpose:** To create a manual testing checklist for games, playtesting, and edge cases.
```text
Act as a QA engineer specializing in games.
Using the PRD and Game Design Document below, create a Testing document for a creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Testing strategy for games
2. Functional testing (Core mechanics)
3. Progression testing (Levels, Save/Load)
4. Performance testing (FPS, Memory, Load times)
5. Input testing (All controls, Remapping)
6. Audio testing (Music, SFX, Spatial audio)
7. UI testing (Menus, HUD, Settings)
8. Edge cases (Spamming inputs, Pausing mid-action, Alt-tab)
9. Playtesting checklist (Fun factor, Confusion points, Difficulty)
10. Bug reporting template
11. A manual testing checklist for the demo
12. How to document known limitations for judges

Keep the testing plan simple enough for beginner developers to execute under time pressure.
Focus on testing the core gameplay loop.
```

---

### 14. EVALUATION.md
**Purpose:** To define how the team measures creative impact and prepares for judge questions.
```text
You are a game evaluation expert.
Using the PRD and Game Design Document below, create an Evaluation document for a creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]

Provide:
1. Evaluation metrics (FPS, Player engagement, Completion rate, Fun factor)
2. Evaluation methods (Playtesting, Surveys, Telemetry)
3. Benchmarking (What is the baseline?)
4. Known limitations of the game
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about games and how to answer them

Focus on demonstrating that the team understands the game's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 15. DEPLOYMENT.md
**Purpose:** To define how to build and deploy to target platforms.
```text
Act as a game deployment engineer.
Using the System Architecture and PRD below, create a Deployment document for a creative hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
PRD: [PASTE PRD]

Provide:
1. Target platform (WebGL, PC, Mobile, Console)
2. Build settings (Development, Release, Optimization)
3. Deployment steps for each platform (itch.io, Steam, Web host, App Store)
4. Environment variables for production
5. How to test the deployed build
6. Fallback plan if deployment fails during the hackathon
7. A pre-deployment checklist
8. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working live demo as early as possible.
For WebGL, prioritize fast loading and browser compatibility.
```

---

### 16. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the game is shown off perfectly.
```text
Act as an expert hackathon presentation coach specializing in games.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]
DEMO FLOW: [PASTE PLAYER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem/Concept
3. Why it matters
4. Existing limitations
5. Our creative solution
6. How it works (Core game loop, Tech)
7. Technology (Unity, Unreal, WebGL, etc.)
8. Demo (The most important part — show live gameplay)
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
Include a backup plan for demo failure (video recording, screenshots, pre-recorded gameplay).
```

---

### 17. GLOSSARY.md
**Purpose:** To define all game and media terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Game Design Document, and Architecture below, create a Glossary document for a creative hackathon project.

PRD: [PASTE PRD]
GAME_DESIGN_DOC: [PASTE GAME_DESIGN_DOC]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Game design terms (Game Loop, Mechanic, Level Design, Progression)
2. Technical terms (FPS, Draw Call, Shader, Prefab, LOD)
3. Art terms (Rigging, Skinning, Texture, Sprite, VFX)
4. Audio terms (SFX, OST, Foley, Spatial Audio, Ducking)
5. Narrative terms (Branching, Dialogue Tree, Arc, Lore)
6. Engine terms (Unity, Unreal, Godot, GameObject, Scene)
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

## Footer (End of Category)

### Thank You

Thank you for using this guide. Go build something amazing!

**Made by Siddiq**

*Credit: Hackathon Alchemy*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**

---
