# AI-Assisted Project Template

This repository serves as a robust scaffolding template for initiating new software projects that leverage an AI-assisted workflow. It is optimized for use with large language models like Google's Gemini or Anthropic's Claude within a terminal interface, such as the one in Visual Studio Code.

The foundational principle of this template is to treat AI as a collaborative development partner. By providing the AI with clear, structured rules and comprehensive context, we can build features that are well-architected, thoroughly planned, and precisely aligned with a strategic vision.

> This workflow is heavily inspired by the methodologies and best practices for AI-assisted development shared by leaders like Ryan Carson.

## Core Philosophies

This template is built upon two key modern development concepts:

1.  **Vibe Coding**: A development paradigm where engineers use natural language to direct AI assistants, focusing on high-level specifications and outcomes rather than line-by-line implementation. Success in this paradigm is contingent on providing the AI with structured thinking and rich, relevant context.
2.  **Simple, Lovable, Complete (SLC)**: An alternative to the traditional Minimum Viable Product (MVP). The objective is to ship products or features that are **Simple** (focused on a core value proposition), **Lovable** (providing a delightful user experience), and **Complete** (fully delivering on their primary promise), ensuring value from the very first release.

---
## What's Inside This Template?

This scaffolding provides a set of rule files and document templates to guide your development process.

```
/
├── .ai-rules/
│   ├── 01_create-prd.md        # Rule for guiding an AI to create a PRD
│   ├── 02_generate-tasks.md    # Rule for breaking a PRD into a task list
│   └── 03_execute-tasks.md     # Rule for executing a task list step-by-step
│
├── .project-docs/
│   ├── Roadmap.md              # Template for project vision, goals, and phases
│   ├── ComponentLibrary.md     # Template for your design system and UI components
│   ├── VibeTesting.md          # Template for defining and testing user experience
│   └── SLC_Session_Notes.md    # Template for planning an SLC-focused work session
│
├── src/
│   └── (Your project's source code lives here)
│
└── README-START-HERE.md        # A detailed guide on how to use this template
```
---

## The 3-Step AI-Assisted Workflow

For any new feature, follow this iterative, three-step process to ensure a structured and predictable development cycle.

### Step 1: Create the Product Requirements Document (PRD)

-   **Goal**: To work with an AI assistant to generate a detailed PRD that is clear enough for a junior developer to understand and execute.
-   **Action**: Use the rules in `.ai-rules/01_create-prd.md` to have the AI prompt you with clarifying questions about the feature's purpose, scope, and user stories.

### Step 2: Generate the Task List

-   **Goal**: To have the AI break down the completed PRD into a detailed, hierarchical task list.
-   **Action**: Use the rules in `.ai-rules/02_generate-tasks.md`. The AI will analyze the PRD and produce a checklist of actionable steps.

### Step 3: Execute the Task List

-   **Goal**: To implement the feature by having the AI complete one sub-task at a time, allowing for human review, testing, and validation at each step.
-   **Action**: Use the rules in `.ai-rules/03_execute-tasks.md`. The AI will work on a single sub-task and then **stop and wait** for your confirmation (e.g., "y" or "yes") before proceeding. You will mark each task as complete (`[x]`) in your task file as you go.

## How to Use This Template

1.  On GitHub, click the "**Use this template**" button to create a new repository for your project.
2.  Clone your new repository to your local machine (`git clone <your-repo-url>`).
3.  Open the project in VS Code and read the **`README-START-HERE.md`** file for a detailed walkthrough on initiating the workflow.
4.  Begin building your first feature by following the 3-step workflow.

