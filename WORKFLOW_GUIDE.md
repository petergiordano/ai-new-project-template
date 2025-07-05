# AI-Assisted Development: The Complete Workflow Guide

### **Purpose: A detailed guide for using this template with the 3-party collaboration model.**

This document explains the guiding philosophies, the roles of each participant, and the step-by-step instructions for building features with this template.

---

## Guiding Philosophy

This template is built upon two key concepts that ensure high-quality, consistent results from AI assistants.

-   **Vibe Coding**: We use natural language to direct AI assistants, but provide them with highly structured context. This requires systematic thinking, rigorous version control, and detailed project documentation.
-   **SLC Framework**: Instead of a Minimum Viable Product (MVP), we build features that are **Simple** (does one thing well), **Lovable** (has a great user experience), and **Complete** (fully delivers on its promise).

---

## The 3-Party Collaboration Model

This workflow splits responsibilities between you and two types of AI assistants to maximize efficiency.

#### 1. The User (You) - The Project Director
You are the ultimate authority. You drive the process, make final decisions, and are responsible for testing and validation.

#### 2. The Chat Assistant (e.g., Gemini, Claude) - The Strategist
This AI runs in a web browser. Its role is high-level thinking, planning, and preparing prompts. It does **not** write the final code.

#### 3. The CLI Assistant (e.g., Gemini CLI, Claude Code) - The Implementer
This AI runs in your VS Code terminal. It has access to your files and its only job is to execute the specific prompts you provide.

---

## The Development Workflow

### **Phase 1: Project Setup & Context**

Before starting any coding, it's crucial to establish the project's foundation.

1.  **Fill out the Project Context Documents:**
    In the `.project-docs/` directory, fill out the following templates. They provide essential context for both you and the AI assistant.
    -   **`Roadmap.md`**: The high-level vision and plan for the entire project.
    -   **`ComponentLibrary.md`**: The design system and UI components.
    -   **`VibeTesting.md`**: Defines the emotional journey and target "vibe."
    -   **`SLC_Session_Notes.md`**: Use this to plan a feature sprint.

2.  **Brief the AI Assistants (Step 0):**
    This is the most critical step. At the beginning of any new chat session, you must first provide the AI with the project's master context.
    -   **Action:** Copy the entire contents of the **`AI_CONTEXT.md`** file and paste it as your first message to the AI.

### **Phase 2: Feature Implementation (The 3 Steps)**

For any new feature, follow this process.

#### **Step 1: Create the Product Requirements Document (PRD)**

-   **Goal**: To define the feature requirements clearly enough for a junior developer to understand.
-   **Process**:
    1.  **You to Chat Assistant:** "I need to build [feature]. Help me think through the requirements."
    2.  **Chat Assistant to You:** Helps you brainstorm and prepares a detailed prompt for the CLI Assistant, using the rules from `.ai-rules/01_create-prd.md`.
    3.  **You to CLI Assistant:** Paste the prepared prompt into the terminal. The CLI assistant will ask clarifying questions.
    4.  **You:** Answer the questions. The CLI Assistant will then generate the final PRD.
    5.  **You:** Save the PRD in a new `tasks/` directory (e.g., `tasks/prd-feature-name.md`).

#### **Step 2: Generate the Task List**

-   **Goal**: To break down the PRD into a detailed, step-by-step checklist.
-   **Process**:
    1.  **You to Chat Assistant:** "Here is the PRD we just created. Prepare the prompt to turn this into a task list."
    2.  **Chat Assistant to You:** Provides a prompt containing the rules from `.ai-rules/02_generate-tasks.md` and the PRD content.
    3.  **You to CLI Assistant:** Paste the prepared prompt into the terminal.
    4.  **CLI Assistant to You:** Generates a hierarchical task list.
    5.  **You:** Review the task list and save it (e.g., `tasks/tasks-feature-name.md`).

#### **Step 3: Execute the Task List**

-   **Goal**: To implement the feature by completing one sub-task at a time, reviewing and testing at each step.
-   **Process**:
    1.  **You to CLI Assistant:** Paste the rules from `.ai-rules/03_execute-tasks.md` into the terminal, followed by the content of your task list file.
    2.  **CLI Assistant to You:** Provides the code for the **first sub-task** and then **PAUSES**.
    3.  **You:** Implement and test the AI's suggestion in VS Code.
    4.  **You:** If the code works, mark the task as complete (`[x]`) in your task file.
    5.  **You to CLI Assistant:** Type **"Go"** to proceed to the next sub-task.
    6.  **Loop:** Repeat steps 2-5 until all tasks are complete.