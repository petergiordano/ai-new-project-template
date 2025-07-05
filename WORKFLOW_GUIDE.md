# AI-Assisted Development: The Complete Workflow Guide

### **Purpose: A detailed guide for using this template with the 3-party collaboration model.**

This document explains the guiding philosophies, the roles of each participant, and the step-by-step instructions for building features with this template.

---

## Using Plan Mode Effectively

*This section applies when using Claude Code CLI and leverages its built-in Plan Mode feature.*

### **What is Plan Mode?**

Plan Mode is Claude Code's read-only analysis mode that prevents accidental file modifications while allowing comprehensive codebase exploration and planning. Access it by pressing Shift+Tab twice, and it creates a safe environment where Claude can research, analyze, and plan without making any changes to your files.

### **Plan Mode Benefits for This Workflow**

- **Safe Exploration:** Analyze existing code without risk of accidental changes
- **Better Planning:** Ask Claude to make a plan before coding and explicitly tell it not to code until you've confirmed its plan looks good
- **Architectural Alignment:** Understand existing patterns before implementing new features
- **Reduced Iterations:** More thoughtful analysis leads to better initial implementations

### **Plan Mode Integration Points**

**Step 1 - Project Initialization:**
- Use Plan Mode to safely explore any existing project structure
- Analyze current dependencies and configuration files
- Better informed questions based on discovered project context

**Step 3 - PRD Creation:**
- Enter Plan Mode to understand how the new feature fits into existing architecture
- Research similar implementations in the codebase
- Plan integration points before defining requirements

**Step 4 - Task Generation:**
- Use Plan Mode to thoroughly analyze the PRD and existing codebase
- Understand dependencies and architectural constraints
- Create more accurate task breakdowns

**Step 5 - Task Execution:**
- Enter Plan Mode before complex parent tasks
- Use for debugging when implementations don't work as expected
- Plan integration strategies for multi-file changes

### **Plan Mode Best Practices**

1. **Always Plan First:** Use Plan Mode for initial analysis - the 2 minutes spent planning saves 20 minutes of refactoring later
2. **Use Thinking Modes:** Use "think", "think hard", "think harder", or "ultrathink" to trigger extended thinking mode for better analysis
3. **Exit to Execute:** Remember to exit Plan Mode (Shift+Tab) before actual implementation
4. **Strategic Usage:** Use Plan Mode for complex tasks, skip for simple repetitive patterns

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

#### 2. The Chat Assistant (e.g., ChatGPT, Gemini, Claude) - The Strategist
This AI runs in a web browser. Its role is high-level thinking, planning, and preparing prompts. It does **not** write the final code.

#### 3. The CLI Assistant (e.g., Gemini CLI, Claude Code) - The Implementer
This AI runs in your VS Code terminal. It has access to your files and its only job is to execute the specific prompts you provide.

---

## The Development Workflow

### **Phase 1: Project Setup & Context**

Before starting any coding, it's crucial to establish the project's foundation.

#### **Step 1: Generate Project Context Documents**
Instead of manually filling out the planning documents, use the AI-assisted initialization process to create your project foundation.

1.  **You to Chat Assistant:** "Help me initialize a new project using the template."
2.  **Chat Assistant to You:** Provides the initialization prompt based on `.ai-rules/00_project-initialization.md`.
3.  **You to CLI Assistant:** Paste the initialization prompt into the terminal.
4.  **CLI Assistant:** **Enters Plan Mode (Shift+Tab twice)** to safely explore any existing project structure and dependencies
5.  **CLI Assistant to You:** Conducts a structured interview through five phases:
    -   **Phase A:** Project Vision & Strategy (→ `Roadmap.md`)
    -   **Phase B:** User Experience & Emotional Design (→ `VibeTesting.md`)
    -   **Phase C:** Design System & Visual Identity (→ `ComponentLibrary.md`)
    -   **Phase D:** First Sprint Planning (→ `SLC_Session_Notes.md`)
    -   **Phase E:** Technical Foundation & AI Context (→ `AI_CONTEXT.md`)
6.  **You:** Answer the questions thoughtfully - these become your project's foundation.
7.  **CLI Assistant:** **Exits Plan Mode** and generates all five populated documents with project-specific Plan Mode guidance.
8.  **You:** Save the generated documents in your project (`.project-docs/` for the first four, root directory for `AI_CONTEXT.md`).

**Alternative Option:** If you prefer to fill out the context documents manually, you can skip Step 1 and complete the templates yourself, but you'll need to manually create your project-specific `AI_CONTEXT.md`.

### **Phase 2: Feature Implementation**

For any new feature, follow this process. **Important:** Always begin new AI sessions by providing your project-specific `AI_CONTEXT.md` to the AI assistant.

#### **Step 2: Brief AI Assistants with Dynamic Context (Context Convergence)**

**Goal**: Ensure all AI assistants have current, accumulated project context for optimal collaboration.

**Enhanced Context Loading Process**:

1. **Context Validation Checkpoint:**
   - **Action:** Copy the entire contents of your **dynamic** `AI_CONTEXT.md` file and paste it as your first message to any AI assistant
   - **Validation:** AI assistant should respond: "Context loaded. Project: [NAME], Current stage: [STAGE], Active features: [LIST]. Ready to assist with [CURRENT_TASK]."
   - **Confirm:** Verify the AI's understanding matches your current project state

2. **Context Convergence Benefits:**
   - **Accumulated Knowledge:** AI_CONTEXT.md now contains lessons learned from previous features
   - **Architecture Awareness:** AI knows existing patterns and decisions made
   - **Integration Intelligence:** AI understands how new features fit with existing code
   - **Validation Continuity:** AI knows what validation approaches work for your project

3. **Role-Specific Context Loading:**
   
   **For Chat AI (Strategist):**
   ```
   "I've loaded the project context. I understand:
   - Project goals and current workflow stage
   - Existing architecture and patterns
   - Active features and their status
   - My role as strategist for planning and prompt preparation
   Ready to help with [current need: PRD creation, task planning, etc.]"
   ```
   
   **For CLI AI (Implementer):**
   ```
   "Context loaded via AI_CONTEXT.md. Current state:
   - Project: [name], Stage: [stage]
   - Tech stack: [details]
   - Active features: [list]
   - Role: CLI implementer for code execution
   Ready for specific implementation tasks."
   ```

4. **Context Handoff Protocol:**
   - **Between Sessions:** Always start with fresh AI_CONTEXT.md loading
   - **Between AI Types:** Chat AI prepares context-rich prompts for CLI AI
   - **Progress Updates:** Update AI_CONTEXT.md as features move through workflow stages

**Critical Success Factors:**
- ✅ AI demonstrates understanding of current project state
- ✅ AI references existing patterns and architecture decisions
- ✅ AI knows which features are active and their current status
- ✅ AI follows established validation and testing approaches
#### **Step 3: Create the Product Requirements Document (PRD)**

-   **Goal**: To define the feature requirements clearly enough for a junior developer to understand.
-   **Process**:
    1.  **You to Chat Assistant:** "I need to build [feature]. Help me think through the requirements."
    2.  **Chat Assistant to You:** Helps you brainstorm and prepares a detailed prompt for the CLI Assistant, using the rules from `.ai-rules/01_create-prd.md`.
    3.  **You to CLI Assistant:** Paste the prepared prompt into the terminal. 
    4.  **CLI Assistant:** **Enters Plan Mode** to understand how the feature fits into existing architecture and research similar implementations
    5.  **CLI Assistant:** **Exits Plan Mode** and asks clarifying questions about the feature requirements
    6.  **You:** Answer the questions. The CLI Assistant will then generate the final PRD.
    7.  **You:** Save the PRD in a new `tasks/` directory (e.g., `tasks/prd-feature-name.md`).

#### **Step 4: Generate the Task List**

-   **Goal**: To break down the PRD into a detailed, step-by-step checklist.
-   **Process**:
    1.  **You to Chat Assistant:** "Here is the PRD we just created. Prepare the prompt to turn this into a task list."
    2.  **Chat Assistant to You:** Provides a prompt containing the rules from `.ai-rules/02_generate-tasks.md` and the PRD content.
    3.  **You to CLI Assistant:** Paste the prepared prompt into the terminal.
    4.  **CLI Assistant:** **Enters Plan Mode** to thoroughly analyze the PRD and examine existing codebase patterns
    5.  **CLI Assistant:** **Exits Plan Mode** and generates a hierarchical task list based on the analysis
    6.  **You:** Review the task list and save it (e.g., `tasks/tasks-feature-name.md`).

#### **Step 5: Execute the Task List**

-   **Goal**: To implement the feature by completing one sub-task at a time, reviewing and testing at each step.
-   **Process**:
    1.  **You to CLI Assistant:** Paste the rules from `.ai-rules/03_execute-tasks.md` into the terminal, followed by the content of your task list file.
    2.  **CLI Assistant:** **Uses Plan Mode strategically** - enters Plan Mode for complex parent tasks to analyze context and plan implementation approach
    3.  **CLI Assistant to You:** Provides the code for the **first sub-task** and then **PAUSES**.
    4.  **You:** Implement and test the AI's suggestion in VS Code.
    5.  **You:** If the code works, mark the task as complete (`[x]`) in your task file.
    6.  **You to CLI Assistant:** Type **"Go"** to proceed to the next sub-task.
    7.  **Loop:** Repeat steps 2-6 until all tasks are complete. The CLI Assistant will use Plan Mode again for complex tasks, debugging, or when issues arise.

---

## Summary: Complete Workflow

1. **Step 1:** Generate project context documents (includes creating project-specific `AI_CONTEXT.md`)
2. **Step 2:** Brief AI with your populated `AI_CONTEXT.md` (at start of each new session)
3. **Step 3:** Create PRD for your feature
4. **Step 4:** Generate task list from PRD
5. **Step 5:** Execute tasks one by one

This systematic approach ensures that both you and the AI have comprehensive context at every stage, leading to more consistent, higher-quality results.