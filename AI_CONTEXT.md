# AI Project Context & Master Rulebook

### **Purpose: This document is the master briefing for any AI assistant working on this project. It must be provided at the beginning of any new development session.**

### CLI Context Files
- This file can be used as a source for context files for claude code (claude.md) and gemini cli (gemini.md)

---

## 1. Project Overview & Goal

- **Project Name:** [Your Project Name]
- **Core Goal:** [A one-sentence summary of what this project does, taken from your Roadmap.md]
- **Target Vibe:** [e.g., "Intuitive and powerful," "Playful and simple," taken from your VibeTesting.md]

---

## 2. Tech Stack

- **Frontend:** [e.g., React, Next.js, Tailwind CSS]
- **Backend:** [e.g., Node.js, Express, FastAPI]
- **Database:** [e.g., Firestore, Supabase, PostgreSQL]
- **Key Libraries:** [e.g., Pydantic for validation, Auth.js for authentication]

---

## 3. File & Folder Structure

- **`/src`**: Contains all application source code.
- **`/src/components`**: Reusable UI components.
- **`/src/lib`**: Core logic, API clients, and utility functions.
- **`/tests`**: All Pytest/Jest tests, mirroring the `/src` structure.
- **`.project-docs/`**: Contains high-level planning documents (Roadmap, etc.). Do not write code here.
- **`.ai-rules/`**: Contains the specific, step-by-step instruction templates for the development workflow (e.g., creating PRDs, generating tasks).

---

## 4. Coding Conventions & Style

- **Language:** [e.g., Python 3.11, TypeScript]
- **Formatting:** All code must be formatted with [e.g., `black` for Python, `prettier` for JS/TS].
- **Naming:** Use `snake_case` for variables and functions, `PascalCase` for classes.
- **Docstrings:** All functions must have Google-style docstrings.
- **Error Handling:** All external API calls must be wrapped in a `try...except` block to handle potential errors gracefully.

---

## 5. Global AI Instructions

- **Always Create Tests:** Every new feature or function must be accompanied by a corresponding unit test in the `/tests` directory.
- **No New Dependencies:** Do not add any new libraries or packages without explicit permission.
- **Follow Existing Patterns:** Before writing new code, review the existing files in `/src` to understand and replicate the established patterns.
- **Ask Before Overwriting:** Never delete or significantly refactor existing code without asking for confirmation first.