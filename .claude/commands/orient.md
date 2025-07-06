# Orient - Project Status & Navigation

Get oriented in your current project and see your next best actions based on current context.

## Purpose

This command helps you get re-oriented when returning to a project after time away. It combines system status with project analysis to show:
- Where you are in the 5-step AI-assisted development workflow
- What options are available based on your current project state  
- Exact commands to run for your next best actions

## Process

1. **System Status Check**
   - Display Claude Code system information
   - Show available MCP servers and integrations
   - Confirm working directory and technical setup

2. **Project State Analysis**
   - Scan current directory for key project files
   - Determine which workflow stage you're in
   - Identify available tools and capabilities

3. **Contextual Guidance**
   - Show your current position in the workflow
   - Provide 3-5 numbered next action options
   - Include exact commands and file references

4. **Self-Teaching Phase**
   - Read relevant project context files
   - Load appropriate workflow documentation
   - Ensure understanding of current project state

## Implementation

### Phase 1: System Status
First, gather technical context about the current environment:

```bash
Working Directory: [show current path]
IDE Integration: [VS Code status] 
MCP Servers: [list active servers]
Account: [current login info]
Model: [current model and limits]
```

### Phase 2: Project Analysis
Analyze the current directory structure and files:

**Key Files to Check:**
- `AI_CONTEXT.md` - Project context and accumulated knowledge
- `CLAUDE.md` / `GEMINI.md` - CLI context configuration  
- `.ai-rules/` directory - Workflow instruction files
- `.project-docs/` directory - Planning documents
- `tasks/` directory - PRD and task files
- `src/` directory - Source code structure

**Workflow Stage Detection Logic:**
```
IF no AI_CONTEXT.md exists:
  → "Template Setup Mode" - need to copy scaffolding files

ELIF AI_CONTEXT.md exists but no PRD files in tasks/:
  → "Step 3: PRD Creation" - ready to create requirements

ELIF PRD exists but no task files:
  → "Step 4: Task Generation" - ready to break down PRD into tasks

ELIF task files exist with uncompleted tasks:
  → "Step 5: Task Execution" - active development mode

ELIF all tasks appear complete:
  → "Feature Complete" - ready for next feature or quality check
```

### Phase 3: Contextual Action Menu

Based on detected stage, provide numbered options:

**Template Setup Mode:**
```
📍 Status: Template Setup Required
🎯 Next Actions:
1. Copy scaffolding files to project root
2. Run project initialization interview 
3. View complete setup instructions
4. Learn about the 5-step workflow
```

**Step 3 - PRD Creation:**
```
📍 Status: Step 3 - Product Requirements Document
🎯 Next Actions:
1. Create PRD for new feature (/generate-prp)
2. View existing project context (read AI_CONTEXT.md)
3. Review workflow guidance (WORKFLOW_GUIDE.md)
4. Start with example PRD template
```

**Step 4 - Task Generation:**
```
📍 Status: Step 4 - Task List Generation  
🎯 Next Actions:
1. Generate tasks from existing PRD (/generate-tasks)
2. Use Task Master for enhanced task breakdown
3. Review and refine PRD before task generation
4. View task generation examples
```

**Step 5 - Task Execution:**
```
📍 Status: Step 5 - Active Development
🎯 Next Actions:
1. Execute next task from task list (/execute-tasks)
2. Review current task progress
3. Run validation checks on completed work
4. View commit message templates
```

**Feature Complete:**
```
📍 Status: Feature Complete
🎯 Next Actions:
1. Start new feature (create new PRD)
2. Run final quality checks and testing
3. Review project documentation
4. Plan next development cycle
```

### Phase 4: Self-Teaching Integration

Based on detected project state, instruct Claude Code to read relevant context:

```
For any project state:
- Read AI_CONTEXT.md for project-specific context
- Read CLAUDE.md for coding standards and patterns
- Read current workflow stage documentation

For specific stages:
- PRD Creation: Read .ai-rules/01_create-prd.md
- Task Generation: Read .ai-rules/02_generate-tasks.md  
- Task Execution: Read .ai-rules/03_execute-tasks.md
```

## Output Format

```
🔄 CLAUDE CODE SYSTEM STATUS
[Display key system information]

📁 PROJECT STATE ANALYSIS  
Current Directory: [path]
Workflow Stage: [detected stage]
Key Files Found: [list relevant files]

📍 WHERE YOU ARE
[Clear description of current position]

🎯 YOUR NEXT BEST OPTIONS
1. [Action 1 with exact command]
2. [Action 2 with exact command] 
3. [Action 3 with exact command]
4. [Action 4 with exact command]

💡 NEED MORE HELP?
- Type /orient detailed for full project analysis
- Type /orient help for all available commands
- Read WORKFLOW_GUIDE.md for complete workflow documentation
```

## Notes

- This command should work regardless of project state
- Always provide actionable next steps with exact commands
- Use progressive disclosure - start simple, offer more detail if needed
- Ensure AI has full context before making recommendations
