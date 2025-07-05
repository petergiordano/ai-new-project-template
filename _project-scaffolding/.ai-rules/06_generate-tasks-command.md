# Command: Generate Tasks

Create a detailed, executable task list from an existing PRD with validation loops.

## Usage
```
/generate-tasks tasks/prd-[feature-name].md
```

## Process

### Phase 1: Plan Mode Analysis
1. **Enter Plan Mode** (Shift+Tab twice) for comprehensive analysis
2. **Context Loading:**
   - Read the specified PRD file thoroughly
   - Analyze existing codebase for similar patterns
   - Review project conventions from AI_CONTEXT.md
   - Identify dependencies and integration points
3. **Architecture Planning:**
   - Understand how new feature fits into existing structure
   - Research similar implementations in codebase
   - Plan file structure and component organization

### Phase 2: Task Structure Generation
4. **Generate Parent Tasks:**
   - Create 4-6 high-level tasks covering complete feature implementation
   - Include setup, core functionality, testing, and integration
   - Present parent tasks to user for approval
5. **Wait for "Go" Confirmation:**
   - Pause after presenting parent tasks
   - Wait for user to respond with "Go" to proceed

### Phase 3: Detailed Task Breakdown
6. **Exit Plan Mode** after confirmation
7. **Generate Sub-Tasks:**
   - Break each parent task into specific, actionable sub-tasks
   - Include file creation, modification, and testing steps
   - Add validation checkpoints and success criteria
8. **Create Complete Task List** using this structure:

```markdown
# Tasks: [Feature Name]

## Relevant Files
- `path/to/file1.ts` - [Description and purpose]
- `path/to/file1.test.ts` - Unit tests for file1.ts
- `path/to/file2.tsx` - [Description and purpose]
- `path/to/file2.test.tsx` - Unit tests for file2.tsx

### Notes
- [Testing patterns and conventions]
- [Validation commands to run]

## Tasks

- [ ] 1.0 **Setup & Foundation**
  - [ ] 1.1 [Specific setup task]
  - [ ] 1.2 [Specific setup task]
  
- [ ] 2.0 **Core Functionality Implementation**
  - [ ] 2.1 [Specific implementation task]
  - [ ] 2.2 [Specific implementation task]
  - [ ] 2.3 [Specific implementation task]
  
- [ ] 3.0 **Validation & Testing**
  - [ ] 3.1 Create unit tests for [component]
  - [ ] 3.2 Add integration tests for [workflow]
  - [ ] 3.3 Validate error handling scenarios
  
- [ ] 4.0 **Integration & Polish**
  - [ ] 4.1 [Integration task]
  - [ ] 4.2 [Documentation task]

## Validation Checkpoints
### After Each Parent Task:
- [ ] Code compiles without errors
- [ ] All new tests pass: `[test command]`
- [ ] Linting passes: `[lint command]`
- [ ] Integration points work correctly

### Final Validation:
- [ ] All tests pass: `[full test suite command]`
- [ ] No linting errors: `[full lint command]`
- [ ] Feature works end-to-end
- [ ] Success criteria from PRD are met
```

9. **Save Task List** as `tasks/tasks-[feature-name].md`

## Command-Driven Benefits
- **Thorough Analysis:** Plan Mode ensures comprehensive understanding
- **Human Approval:** User confirms parent tasks before detailed breakdown
- **Validation Integration:** Built-in checkpoints prevent errors
- **Clear Transitions:** Ready for `/execute-tasks` command

## Next Step
After task list is approved, user can run: `/execute-tasks tasks/tasks-[feature-name].md`