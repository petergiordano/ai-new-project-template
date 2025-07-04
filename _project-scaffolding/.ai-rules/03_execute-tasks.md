# Rule: Task List Execution

## Goal

You are an AI assistant helping me implement a feature by following a provided task list. Your role is to provide the code for each sub-task. When a parent task is complete, you will **compose a detailed commit message** for me to use in my GitHub Desktop app.

## Process

1.  **Receive Task List:** I will provide you with the task list file content.
2.  **Identify Next Sub-Task:** Find the very next sub-task in the list that is not marked as complete (`[ ]`).
3.  **Execute Sub-Task:** Provide the code or instructions needed to complete **only that single sub-task**.
4.  **Check for Parent Task Completion:** After providing the code for a sub-task, check if this was the final sub-task for a parent item.
    * **If it was the final sub-task**, you will then provide me with a formatted commit message, based on the "Commit Message Protocol" below.
5.  **PAUSE:** After providing the implementation (and a commit message, if necessary), you **MUST STOP** and wait for my next instruction.
6.  **Wait for "Go":** I will implement your suggestions. When I am ready to move on, I will send the message "Go", "Proceed", "y", or "yes".
7.  **Repeat:** When you receive my "Go" signal, repeat the process starting from step 2.

---

## Commit Message Protocol

When I complete the final sub-task of a parent task, you must generate a commit message for me to copy and paste into GitHub Desktop. The message should be formatted like this:

**Subject Line:**
`type: A short summary of the parent task`

**Body:**


  - Detail of the first key change.
  - Detail of the second key change.
  - Add more details as needed.

Related to Task \#[TaskNumber]



---

## My Role (The User)

-   I will tell you when to proceed.
-   I will handle all Git operations (staging, committing, pushing) using the **GitHub Desktop app**.
-   **I am responsible for updating the task list file and marking tasks as complete (`[x]`).**

Your job is to focus on one sub-task at a time, provide the code, provide a commit message when necessary, and then wait for my signal.


