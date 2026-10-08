# Category 06: Web3 / Blockchain

This category focuses on building decentralized applications (dApps) using tools like **Solidity**, **Ethereum**, **Polygon**, **Hardhat**, **Foundry**, **IPFS**, and **MetaMask**. It strips away traditional centralized complexities and focuses purely on **smart contracts, wallets, tokens, and on-chain logic** — the foundation of every Web3 hackathon.

Here is the exact list of documents we will prepare for the **Web3 / Blockchain** category, organized into our 4 Phases:

### Phase 1: Problem Definition & Strategy
1. **`PROBLEM_ANALYSIS.md`** — Defines the core problem, target users, and existing gaps (Decentralization focus).
2. **`PRD.md`** (Product Requirements Document) — Outlines features, user stories, MVP scope, and success metrics for a dApp.
3. **`TRD.md`** (Technical Requirements Document) — Defines the blockchain stack (Ethereum, Polygon, Solana), smart contract language, and gas limits.

### Phase 2: Technical Blueprint
4. **`SYSTEM_ARCHITECTURE.md`** — High-level diagram of Frontend → Wallet → Smart Contract → Blockchain (dApp architecture).
5. **`SMART_CONTRACT_SPEC.md`** — (Replaces `DATABASE_SCHEMA.md`) Defines contract functions, state variables, events, and modifiers.
6. **`WALLET_INTEGRATION.md`** — (Replaces `API_SPECIFICATION.md`) Defines wallet connection (MetaMask, WalletConnect), network switching, and transaction signing.
7. **`TOKENOMICS.md`** — (Replaces `AUTHENTICATION_FLOW.md`) Defines token supply, distribution, utility, and incentives (if applicable).
8. **`GAS_OPTIMIZATION.md`** — Defines gas estimation, optimization strategies, and cost limits.

### Phase 3: Execution, Quality & Security
9. **`UI_SPEC.md`** — Frontend design, wallet connection UI, transaction states, and user flow.
10. **`ERROR_HANDLING.md`** — What happens when a transaction fails, gas is too low, or the wallet disconnects.
11. **`SECURITY.md`** — Reentrancy attacks, integer overflow, access control, and private key safety.
12. **`TESTING.md`** — QA plan, smart contract unit tests, testnet deployment, and edge cases.
13. **`EVALUATION.md`** — How you measure dApp performance (Gas cost, Transaction speed, User adoption).

### Phase 4: Delivery & Presentation
14. **`DEPLOYMENT.md`** — Deploying smart contracts to testnet/mainnet, hosting frontend, and verifying contracts.
15. **`DEMO_SCRIPT.md`** — The exact flow of the live presentation.
16. **`GLOSSARY.md`** — Definitions of Web3 terms (Wallet, Gas, Smart Contract, Testnet, dApp).

---

## Phase 1: Problem Definition & Strategy — Prompt Pack

### 1. PROBLEM_ANALYSIS.md
**Purpose:** To deeply understand the problem and identify what can be solved through decentralization.
```text
I am participating in a Web3/Blockchain hackathon and I am a beginner.

Analyze the following problem statement deeply.
[PASTE PROBLEM STATEMENT]

Explain it in very simple language.
Then provide:
1. The actual problem being solved
2. Target users
3. User pain points
4. Existing ways people might solve this problem (Centralized solutions)
5. Limitations of existing centralized solutions
6. Proposed Web3/Blockchain solution ideas
7. Core dApp features
8. Nice-to-have features
9. What should NOT be built during a short hackathon
10. What could make this solution unique
11. A realistic MVP that can be built during a hackathon
12. Potential blockchain platforms and tools that could be used (Ethereum, Polygon, Solana, Hardhat, etc.)

Do not assume I am an experienced blockchain developer.
Explain Web3 concepts (wallets, smart contracts, gas, testnet) in beginner-friendly language.
```

---

### 2. PRD.md (Product Requirements Document)
**Purpose:** To translate the problem analysis into a clear dApp plan with smart contracts, wallets, and scope.
```text
You are a senior Web3 product manager helping a beginner hackathon team.
Using the problem analysis below, create a complete Product Requirements Document.

PROBLEM ANALYSIS:
[PASTE PREVIOUS ANALYSIS]

Create the PRD with these sections:
1. Product name
2. One-line product description
3. Problem statement
4. Target users
5. User pain points
6. Proposed Web3 solution
7. Product goals
8. User stories
9. Functional requirements (Include Web3-specific requirements: Wallet connection, Smart contract calls, Transaction signing, Token logic)
10. Non-functional requirements (Gas efficiency, Transaction speed, Decentralization)
11. Core dApp features
12. Nice-to-have features
13. User journeys (Connect Wallet → Interact → Sign Transaction → Confirmation)
14. MVP scope (Which smart contract must work during the demo?)
15. Out-of-scope features
16. Success metrics (Include Web3 metrics: Transactions completed, Gas cost per action, Unique wallets)
17. Risks and assumptions (Include Web3 risks: Network congestion, Gas spikes, Testnet downtime)

Keep the MVP realistic for a 24-48 hour Web3 hackathon.
Do not add unnecessary contracts just to make the project sound impressive.
Prioritize features that can actually be demonstrated live on a testnet.
```

---

### 3. TRD.md (Technical Requirements Document)
**Purpose:** To translate the PRD into technical specifications focused on blockchain choice, smart contracts, and wallet integration.
```text
You are a senior blockchain engineer helping a beginner hackathon team.
Using the PRD below, create a Technical Requirements Document (TRD).

PRD:
[PASTE PRD]

Create the TRD with these sections:
1. System overview
2. Blockchain platform choice (Ethereum, Polygon, Solana, Base — justify the choice)
3. Smart contract language and framework (Solidity + Hardhat/Foundry)
4. Contract architecture (Contracts, Inheritance, Libraries)
5. Wallet integration requirements (MetaMask, WalletConnect, Coinbase Wallet)
6. Token requirements (ERC-20, ERC-721, ERC-1155 — if applicable)
7. Storage requirements (On-chain vs IPFS vs The Graph)
8. Gas and performance requirements
9. Security requirements (Reentrancy, Access control, Overflow)
10. Frontend library requirements (Ethers.js, Wagmi, Viem, Web3.js)
11. Testing requirements (Unit tests, Testnet deployment)
12. Deployment requirements

Keep the blockchain stack simple and realistic for a 24-48 hour hackathon.
Explain all Web3 concepts in beginner-friendly language.
Do not introduce unnecessary chains or tools.
```

---

## Phase 2: Technical Blueprint — Prompt Pack

### 4. SYSTEM_ARCHITECTURE.md
**Purpose:** To design a realistic dApp architecture with clear data flow from frontend to blockchain.
```text
Act as a senior blockchain architect.
Using the following PRD and TRD, design a realistic hackathon dApp architecture.

PRD: [PASTE PRD]
TRD: [PASTE TRD]

Provide:
1. Recommended blockchain stack (Chain, Language, Framework)
2. Complete dApp architecture diagram (Text-based, showing User → Wallet → Frontend → Smart Contract → Blockchain)
3. Frontend architecture (React, Next.js, Wallet connect)
4. Smart contract architecture (Contracts, Functions, Events)
5. Wallet integration architecture (Connection, Network switch, Signing)
6. Storage architecture (On-chain, IPFS, The Graph)
7. Token architecture (If applicable)
8. Data flow (How a user action becomes a transaction)
9. Security considerations (Reentrancy, Access control)
10. Folder structure
11. Major components
12. Simplifications that can be made for a hackathon

Explain every technical decision in beginner-friendly language.
Do not introduce unnecessary tools. Prefer a simple architecture that can be explained easily to judges.
```

---

### 5. SMART_CONTRACT_SPEC.md
**Purpose:** To define the exact smart contract functions, state variables, events, and modifiers.
```text
Act as a senior smart contract engineer.
Using the PRD and System Architecture below, design the smart contract specification for this Web3 hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

For each smart contract, provide:
1. Contract name
2. Purpose of the contract
3. State variables (Name, Type, Visibility)
4. Functions (Name, Parameters, Visibility, Modifiers)
5. Events (Name, Parameters)
6. Modifiers (Access control, Validation)
7. Inheritance (If any)
8. External dependencies (Oracles, Other contracts)
9. Token standard (ERC-20, ERC-721, ERC-1155 — if applicable)
10. Example function calls
11. Gas estimate per function (Rough)
12. Access control rules (Who can call what?)

Explain why each function exists.
Keep the contract simple enough for a beginner hackathon team to understand and maintain.
```

---

### 6. WALLET_INTEGRATION.md
**Purpose:** To define wallet connection, network switching, and transaction signing.
```text
You are a senior Web3 frontend engineer.
Using the PRD and System Architecture below, create a Wallet Integration document for this Web3 hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Supported wallets (MetaMask, WalletConnect, Coinbase Wallet)
2. Wallet connection flow (Step-by-step)
3. Network detection and switching (Mainnet, Testnet)
4. Account change handling
5. Transaction signing flow (Step-by-step)
6. Reading data from the blockchain (Read-only calls)
7. Writing data to the blockchain (Transactions)
8. Listening to events (Contract events)
9. Error handling (User rejects, Network mismatch)
10. Frontend library choice (Ethers.js, Wagmi, Viem)
11. Example code snippets for connection and signing
12. A checklist for developers to verify wallet integration before the demo

Keep the integration simple and realistic for a hackathon.
Explain each step in beginner-friendly language.
```

---

### 7. TOKENOMICS.md
**Purpose:** To define token supply, distribution, utility, and incentives (if applicable).
```text
Act as a tokenomics expert.
Using the PRD and Smart Contract Specification below, create a Tokenomics document for this Web3 hackathon project.

PRD: [PASTE PRD]
SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]

Provide:
1. Token name and symbol
2. Token standard (ERC-20, ERC-721, ERC-1155)
3. Total supply
4. Distribution (Team, Users, Liquidity, Rewards)
5. Utility (What can the token be used for?)
6. Minting and burning rules
7. Transfer rules
8. Incentive mechanisms (Staking, Rewards, Governance)
9. Vesting schedule (If applicable)
10. Contract functions related to the token
11. A checklist for developers to verify token logic before the demo

If the project does not require a token, explain why and suggest alternative incentive mechanisms.
Keep the tokenomics simple and realistic for a hackathon.
Explain concepts in beginner-friendly language.
```

---

### 8. GAS_OPTIMIZATION.md
**Purpose:** To define gas estimation, optimization strategies, and cost limits.
```text
You are a senior smart contract optimization expert.
Using the Smart Contract Specification and System Architecture below, create a Gas Optimization document for this Web3 hackathon project.

SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Gas estimation per function (Read and Write)
2. Gas optimization techniques used (Packing variables, Avoiding loops, Using events instead of storage)
3. Storage vs Memory vs Calldata usage
4. Efficient data structures
5. Batch operations (If applicable)
6. Gas cost comparison (Before vs After optimization)
7. Gas limits for the demo
8. Fallback if gas spikes during the demo
9. Tools used for gas analysis (Hardhat Gas Reporter, Etherscan)
10. A checklist for developers to verify gas optimization before the demo

Explain each optimization in beginner-friendly language.
Keep the optimizations simple and achievable within a hackathon timeframe.
```

---

## Phase 3: Execution, Quality & Security — Prompt Pack

### 9. UI_SPEC.md
**Purpose:** To define the frontend components, wallet connection UI, and transaction states.
```text
Act as a senior UI/UX designer specializing in Web3.
Using the PRD and System Architecture below, create a UI Specification document for a Web3 hackathon project.

PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Design system (Colors, typography, spacing)
2. Component hierarchy (Wallet button, Transaction modal, Contract interaction forms)
3. Screen-by-screen breakdown (Landing, Connect Wallet, Dashboard, Transaction History)
4. Wallet connection states (Disconnected, Connecting, Connected, Wrong Network)
5. Transaction states (Pending, Success, Failed)
6. Loading states (Skeletons, spinners)
7. Error states (Transaction failed, User rejected)
8. Empty states (No transactions yet)
9. Responsive design guidelines (Mobile and Desktop)
10. Accessibility considerations (Contrast, keyboard navigation)

Keep the UI simple, clean, and realistic for a 24-48 hour Web3 hackathon.
Focus on demonstrating the core dApp journey.
```

---

### 10. ERROR_HANDLING.md
**Purpose:** To define what happens when a transaction fails, gas is too low, or the wallet disconnects.
```text
You are a senior Web3 developer.
Using the System Architecture and Wallet Integration document below, create an Error Handling document for a Web3 hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
WALLET_INTEGRATION: [PASTE WALLET_INTEGRATION]

Provide:
1. Common failure modes (User rejects transaction, Insufficient gas, Network congestion, Contract revert)
2. Frontend error display (Toasts, inline errors, modals)
3. Transaction error handling (Revert reasons, Gas estimation errors)
4. Wallet error handling (Disconnected wallet, Wrong network)
5. Contract error handling (Require statements, Custom errors)
6. Fallback responses (What to show if the transaction fails)
7. Retry logic (If applicable)
8. A checklist for developers to verify error handling before the demo

Focus on making the dApp resilient so the live demo does not crash.
Explain each error handling approach in beginner-friendly language.
```

---

### 11. SECURITY.md
**Purpose:** To secure smart contracts, wallets, and user data against common Web3 attacks.
```text
Act as a smart contract security auditor.
Using the Smart Contract Specification and System Architecture below, create a Security document for a Web3 hackathon project.

SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide:
1. Reentrancy protection (Checks-Effects-Interactions pattern)
2. Integer overflow/underflow protection (SafeMath, Solidity 0.8+)
3. Access control (Ownable, Roles, Modifiers)
4. Front-running protection (If applicable)
5. Oracle manipulation protection (If applicable)
6. Private key safety (Never commit private keys)
7. Environment variable protection (.env, .gitignore)
8. Wallet security best practices for users
9. Audit checklist before deployment
10. A pre-submission security checklist

Keep the security measures practical and easy to implement within a hackathon timeframe.
Explain each vulnerability and mitigation in beginner-friendly language.
```

---

### 12. TESTING.md
**Purpose:** To create a manual testing checklist for smart contracts, wallet integration, and edge cases.
```text
Act as a QA engineer specializing in Web3 applications.
Using the PRD and Smart Contract Specification below, create a Testing document for a Web3 hackathon project.

PRD: [PASTE PRD]
SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]

Provide:
1. Testing strategy for smart contracts
2. Unit testing (Hardhat/Foundry tests for each function)
3. Integration testing (Frontend + Contract)
4. Wallet testing (Connect, Disconnect, Network switch, Sign)
5. Transaction testing (Success, Failure, Revert)
6. Edge cases (Zero values, Large values, Unauthorized access)
7. Testnet deployment testing
8. User acceptance testing checklist
9. A manual testing checklist for the demo
10. How to document known limitations for judges

Keep the testing plan simple enough for beginner developers to execute under time pressure.
Include example test cases for each core function.
```

---

### 13. EVALUATION.md
**Purpose:** To define how the team measures dApp performance and prepares for judge questions.
```text
You are a Web3 evaluation expert.
Using the PRD and Smart Contract Specification below, create an Evaluation document for a Web3 hackathon project.

PRD: [PASTE PRD]
SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]

Provide:
1. Evaluation metrics (Gas cost per transaction, Transaction speed, Number of unique wallets, Contract security)
2. Evaluation methods (Testnet testing, Gas analysis, User feedback)
3. Benchmarking (What is the baseline?)
4. Known limitations of the dApp or blockchain
5. How to explain these limitations to judges honestly
6. A checklist of evidence to gather for the presentation
7. Common judge questions about Web3 and how to answer them

Focus on demonstrating that the team understands the dApp's capabilities and boundaries.
```

---

## Phase 4: Delivery & Presentation — Prompt Pack

### 14. DEPLOYMENT.md
**Purpose:** To define how to deploy smart contracts to testnet/mainnet and host the frontend.
```text
Act as a Web3 DevOps engineer.
Using the System Architecture and Smart Contract Specification below, create a Deployment document for a Web3 hackathon project.

ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]

Provide:
1. Blockchain network for deployment (Testnet: Sepolia, Goerli, Mumbai, Devnet)
2. Smart contract deployment steps (Hardhat/Foundry commands)
3. Contract verification (Etherscan, Polygonscan)
4. Frontend hosting (Vercel, Netlify)
5. Environment variables for production (RPC URLs, Contract addresses, API keys)
6. Wallet setup for deployment (Deployer wallet, Private key safety)
7. How to test the deployed dApp
8. Fallback plan if deployment fails during the hackathon
9. A pre-deployment checklist
10. Common deployment mistakes and how to avoid them

Keep the deployment process simple and achievable within a 24-48 hour hackathon.
Focus on getting a working dApp on testnet as early as possible.
```

---

### 15. DEMO_SCRIPT.md
**Purpose:** To create the exact flow of the live presentation, ensuring the dApp is shown off perfectly.
```text
Act as an expert hackathon presentation coach.
Using the following project information:
PRD: [PASTE PRD]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]
SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]
DEMO FLOW: [PASTE USER JOURNEY]

Create a compelling hackathon presentation script.
The presentation should follow:
1. Hook
2. Problem
3. Why the problem matters
4. Existing limitations (Centralized solutions)
5. Our Web3 solution
6. How it works (Wallet → Contract → Blockchain)
7. Technology (Ethereum, Solidity, Hardhat, Ethers.js)
8. Demo (The most important part — show a live transaction)
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

### 16. GLOSSARY.md
**Purpose:** To define all Web3 terms so every team member can explain the tech to judges without confusion.
```text
You are a technical writer.
Using the PRD, Smart Contract Specification, and Architecture below, create a Glossary document for a Web3 hackathon project.

PRD: [PASTE PRD]
SMART_CONTRACT_SPEC: [PASTE SMART_CONTRACT_SPEC]
ARCHITECTURE: [PASTE SYSTEM_ARCHITECTURE]

Provide definitions for all key terms used in the project, including:
1. Blockchain terms (Block, Transaction, Gas, Testnet, Mainnet, Consensus)
2. Smart contract terms (Solidity, Function, Modifier, Event, Revert, State Variable)
3. Wallet terms (MetaMask, WalletConnect, Private Key, Public Address, Seed Phrase)
4. Token terms (ERC-20, ERC-721, ERC-1155, Mint, Burn, Staking)
5. Web3 frontend terms (Ethers.js, Wagmi, Viem, RPC, ABI)
6. Security terms (Reentrancy, Overflow, Access Control, Audit)
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

**Made by Siddiq**

*Credit: Hackathon Alchemy*

[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/SidhCodez)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/siddiq-dev/)

🔗 **[Link to Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)**