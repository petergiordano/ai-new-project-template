# Project Scaffolding & AI-Assisted Workflow

This project follows a structured, AI-assisted development workflow. This guide explains how to use the templates and rules in this repository to build features efficiently and consistently.

## Guiding Philosophy

- **Vibe Coding**: We use natural language to direct AI assistants, but provide them with highly structured context to ensure quality results. This requires systematic thinking, rigorous version control, and detailed project documentation.
- **SLC Framework**: Instead of a Minimum Viable Product (MVP), we build features that are **Simple** (does one thing well), **Lovable** (has a great user experience), and **Complete** (fully delivers on its promise).

---

## Getting Started: The Project Context Documents

Before starting any coding, it's crucial to establish the project's foundation. Fill out the following documents in the `.project-docs/` directory. They provide essential context for both you and the AI assistant.

-   **`Roadmap.md`**: The high-level vision and plan for the entire project.
-   **`ComponentLibrary.md`**: The design system and UI components. You will paste relevant parts of this file to the AI when you need UI elements.
-   **`VibeTesting.md`**: Defines the emotional journey and target "vibe."
-   **`SLC_Session_Notes.md`**: Use this to plan a feature sprint to ensure it's simple, lovable, and complete.

---

## The 3-Step Development Workflow

For any new feature, follow this three-step process using the files in the `.ai-rules` directory.

### **Step 1: Create the Product Requirements Document (PRD)**

1.  **Goal**: Define the feature requirements clearly.
2.  **Action**:
    -   Open a new terminal session with your AI assistant (Gemini/Claude).
    -   Copy the entire contents of `.ai-rules/01_create-prd.md` and paste it into the AI prompt.
    -   The AI will now ask you a series of clarifying questions. Answer them thoroughly.
    -   The AI will generate a PRD. Save it in a new `tasks` directory (e.g., `tasks/prd-feature-name.md`).

### **Step 2: Generate the Task List**

1.  **Goal**: Break down the PRD into a detailed, step-by-step checklist.
2.  **Action**:
    -   In the same AI session, copy the contents of `.ai-rules/02_generate-tasks.md` and paste it into the prompt.
    -   Next, provide the content of the PRD you just created.
    -   The AI will generate a hierarchical task list. Review it for clarity and save it (e.g., `tasks/tasks-feature-name.md`).

### **Step 3: Execute the Task List**

1.  **Goal**: Implement the feature by completing one sub-task at a time, reviewing and testing at each step.
2.  **Action**:
    -   Copy the contents of `.ai-rules/03_execute-tasks.md` into the AI prompt.
    -   Provide the content of your task list file.
    -   The AI will begin working on the first sub-task and then **PAUSE**.
    -   Implement and test the AI's suggestion in VS Code.
    -   Once you are satisfied, go to your task list file, mark the sub-task as complete (`[x]`), and type **"Go"** in the AI prompt to proceed to the next one.
    -   Repeat this loop until all tasks are complete.