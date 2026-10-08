## 🛠️ How Can I Contribute?

### 1. Adding a New Category Prompt Book

If you want to contribute a prompt book for a category that doesn't have one yet:

1. Check the list of 16 categories in [`CATEGORIES.md`](CATEGORIES.md).
2. Create a new folder in the root directory with the exact category name (e.g., `Automation and Workflow/`).
3. Inside that folder, create a file named `PROMPT-BOOK FOR [CATEGORY].md`.
4. Follow the **4-Phase structure Or you can go more phases and additional documents  if you fell to add**
   - **Phase 1:** Problem Definition & Strategy (`PROBLEM_ANALYSIS`, `PRD`, `TRD`)
   - **Phase 2:** Technical Blueprint & AI Core (`SYSTEM_ARCHITECTURE`, `DATABASE_SCHEMA`, `API_SPECIFICATION`, `AI_RULES`, `AI_MEMORY`, `PROMPT_LIBRARY`, `CACHE_SCHEMA`, `EVIDENCE_MODEL`)
   - **Phase 3:** Execution, Quality & Security (`UI_SPEC`, `ERROR_HANDLING`, `SECURITY`, `TESTING`, `EVALUATION`)
   - **Phase 4:** Delivery & Presentation (`DEPLOYMENT`, `DEMO_SCRIPT`, `GLOSSARY`)

### 2. Improving Existing Prompt Books

If you have a better prompt for an existing document (e.g., `PRD.md`, `AI_RULES.md`):

1. Navigate to the relevant category folder (e.g., `AI-ML/`).
2. Open the `PROMPT-BOOK FOR [CATEGORY].md` file.
3. Ensure the prompt follows our **5-Part Blueprint**:
   - **The Role** (e.g., "Act as a senior product manager...")
   - **The Input** (e.g., "[PASTE PROBLEM ANALYSIS]")
   - **The Task** (e.g., "Create a PRD...")
   - **The Sections** (Numbered list of required sections)
   - **The Constraints** (e.g., "Keep the MVP realistic for a 24-hour hackathon.")

### 3. Reporting Bugs or Typos

If you find a broken link, a typo, or an outdated prompt:

- Open an issue describing the problem.
- If possible, submit a Pull Request with the fix.

## 🚀 Pull Request Process

1. **Fork** the repository: [https://github.com/SidhCodez/Hackathon-Alchemy/fork](https://github.com/SidhCodez/Hackathon-Alchemy/fork)
2. **Clone** your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/Hackathon-Alchemy.git
   ```
3. **Create a branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Commit your changes**:
   ```bash
   git commit -m "Add: Prompt book for Automation & Workflow category"
   ```
5. **Push to the branch**:
   ```bash
   git push origin feature/your-feature-name
   ```
6. **Open a Pull Request** against the `main` branch of the original repository.

## 📝 Style Guide

- Use **Markdown** for all documents.
- Keep the language **beginner-friendly**.
- Use **tables** where comparisons are needed.
- Always include a **Log Entry** at the end of each category.
- Follow the existing naming convention: `PROMPT-BOOK FOR [CATEGORY].md`

## 📋 Naming Conventions

| Type | Convention | Example |
| :--- | :--- | :--- |
| Category Folder | Exact category name from `CATEGORIES.md` | `AI-ML/`, `Non-AI Traditional Software/` |
| Prompt Book File | `PROMPT-BOOK FOR [CATEGORY].md` | `PROMPT-BOOK FOR AI-ML.md` |
| Document Section | UPPERCASE with underscores | `PROBLEM_ANALYSIS.md`, `PRD.md` |

## 🔗 Connect with the Creator

**Made by Siddiq**

- **GitHub:** [SidhCodez](https://github.com/SidhCodez)
- **LinkedIn:** [Siddiq Dev](https://www.linkedin.com/in/siddiq-dev/)
- **Repository:** [Hackathon Alchemy](https://github.com/SidhCodez/Hackathon-Alchemy.git)

---

*Thank you for contributing! Let's build the ultimate hackathon resource together.*