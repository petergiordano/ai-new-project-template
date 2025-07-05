# Rule: Task List Execution

## Goal

You are an AI assistant helping me implement a feature by following a provided task list. Your role is to provide the code for each sub-task. When a parent task is complete, you will **compose a detailed commit message** for me to use in my GitHub Desktop app.

## Process

1.  **Receive Task List:** I will provide you with the task list file content.
2.  **Enter Plan Mode (Recommended):** If using Claude Code CLI, press Shift+Tab twice to enter Plan Mode for initial analysis
3.  **Analyze Task Context:** In Plan Mode, examine the codebase, understand existing patterns, and review the specific sub-task requirements
4.  **Exit Plan Mode & Identify Next Sub-Task:** Exit Plan Mode (Shift+Tab) and find the very next sub-task in the list that is not marked as complete (`[ ]`).
5.  **Execute Sub-Task:** Provide the code or instructions needed to complete **only that single sub-task**.
6.  **Check for Parent Task Completion:** After providing the code for a sub-task, check if this was the final sub-task for a parent item.
    * **If it was the final sub-task**, you will then provide me with a formatted commit message, based on the "Commit Message Protocol" below.
7.  **PAUSE:** After providing the implementation (and a commit message, if necessary), you **MUST STOP** and wait for my next instruction.
8.  **Wait for "Go":** I will implement your suggestions. When I am ready to move on, I will send the message "Go", "Proceed", "y", or "yes".
9.  **Repeat:** When you receive my "Go" signal, repeat the process starting from step 2 (using Plan Mode for complex tasks when needed).

## Claude Code Plan Mode Integration

For enhanced task execution, leverage Plan Mode strategically:

### **When to Use Plan Mode During Execution:**

**Always Use Plan Mode For:**
- **Complex Parent Tasks:** Before starting any parent task with multiple sub-tasks
- **Architecture Changes:** Tasks that modify core structure or patterns
- **Integration Points:** Tasks that touch multiple files or systems
- **Debugging Issues:** When implementation doesn't work as expected

**Optional Plan Mode For:**
- **Simple Sub-Tasks:** Straightforward code additions or modifications
- **Repetitive Patterns:** Tasks following established patterns in the codebase

### **Recommended Plan Mode Workflow for Complex Tasks:**

1. **Enter Plan Mode:** Press Shift+Tab twice
2. **Analyze Current State:** 
   - Read relevant files mentioned in the task
   - Understand existing code patterns and architecture
   - Review any dependencies or integration points
3. **Plan Implementation Strategy:**
   - Determine the best approach for the specific sub-task
   - Identify potential issues or edge cases
   - Consider how this change fits with existing code
4. **Present Implementation Plan:** Exit Plan Mode and explain your approach before providing code
5. **Implement:** Provide the actual code implementation

### **Example Plan Mode Usage:**

```
# User provides task list with complex parent task
# AI enters Plan Mode first

[In Plan Mode - Analysis Phase]
"Let me analyze the codebase structure and understand how to implement the user authentication system..."

[Exits Plan Mode - Implementation Phase]
"Based on my analysis, I'll implement the authentication middleware by creating a new file at `src/middleware/auth.ts` that integrates with your existing Express setup..."
```

## Commit Message Protocol

When I complete the final sub-task of a parent task, you must generate a commit message for me to copy and paste into GitHub Desktop. The message should be formatted like this:

**Subject Line:**
`type: A short summary of the parent task`

**Body:**

- Detail of the first key change.
- Detail of the second key change.
- Add more details as needed.

Related to Task #[TaskNumber]

## Enhanced Workflow for Complex Features

For parent tasks with significant complexity, use this enhanced workflow:

### **Phase 1: Plan Mode Analysis**
1. Enter Plan Mode (Shift+Tab twice)
2. Analyze the entire parent task and its sub-tasks
3. Review existing codebase for patterns and integration points
4. Create implementation strategy
5. Exit Plan Mode

### **Phase 2: Structured Implementation**
1. Present overall strategy to user for approval
2. Implement sub-tasks one by one
3. Use Plan Mode again if unexpected complexity arises
4. Provide commit message when parent task is complete

### **Benefits of This Approach:**
- **Reduced Errors:** Better understanding before implementation
- **Consistent Patterns:** Alignment with existing codebase conventions
- **Fewer Iterations:** More thoughtful initial implementations
- **Better Integration:** Understanding of how changes affect the broader system

## My Role (The User)

-   I will tell you when to proceed.
-   I will handle all Git operations (staging, committing, pushing) using the **GitHub Desktop app**.
-   **I am responsible for updating the task list file and marking tasks as complete (`[x]`).**

Your job is to focus on one sub-task at a time, provide the code, provide a commit message when necessary, and then wait for my signal.

## Plan Mode Best Practices for Task Execution

- **Use "think harder" or "ultrathink"** in Plan Mode for complex architectural decisions
- **Read relevant documentation** in Plan Mode before implementing unfamiliar patterns
- **Examine test files** in Plan Mode to understand expected behavior
- **Check for existing utilities** that could be reused rather than rebuilding
- **Consider error handling patterns** established in the codebase
- **Verify security implications** for authentication, data handling, or API endpoints