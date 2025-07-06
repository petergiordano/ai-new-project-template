# Start Project Setup

Transform "Save As..." template into ready-to-code project workspace.

## Command Purpose

Run **once** after "Save As..." to convert ai-new-project-template into a clean project workspace. Handles file management and kicks off Step 1 initialization.

## Execution Process

### Phase 1: Validation & Safety Checks

First, verify this is a fresh template ready for conversion:

```bash
# Check for scaffolding directory
ls -la _project-scaffolding/
```

If `_project-scaffolding/` doesn't exist, stop and inform user this doesn't appear to be a fresh template.

### Phase 2: File Management Operations

Execute these file operations in order:

1. **Copy template files to working positions:**
   ```bash
   cp "_project-scaffolding/README-project-template.md" "README-project.md"
   cp "_project-scaffolding/TODO-template.md" "TODO.md"
   ```

2. **Remove template development files:**
   ```bash
   rm -rf "claude-project/"
   # Note: Keep original README.md as framework documentation
   ```

3. **Clean up scaffolding:**
   ```bash
   rm -rf "_project-scaffolding/"
   ```

### Phase 3: Verification

Confirm the project structure is correct:

```bash
ls -la
```

Expected structure after cleanup:
- ✅ `README-project.md` (new project README)
- ✅ `TODO.md` (clean project task tracker)
- ✅ `AI_CONTEXT.md` (template ready for population)
- ✅ `.ai-rules/` (workflow instructions preserved)
- ✅ `.project-docs/` (planning templates preserved)
- ✅ `src/` (source directory preserved)
- ❌ `claude-project/` (removed)
- ❌ `_project-scaffolding/` (removed)

### Phase 4: Initialize Project (Step 1)

After successful file management, automatically start the project initialization process:

```markdown
🎉 Project setup complete! Now let's initialize your project foundation.

I'll guide you through a structured interview to create your project context. This creates 5 key documents through a systematic Q&A process:

📋 **Documents to be created:**
- `Roadmap.md` - Project vision, goals, and technical approach
- `VibeTesting.md` - User experience and emotional design
- `ComponentLibrary.md` - Design system and visual identity  
- `SLC_Session_Notes.md` - Development sprint planning
- `AI_CONTEXT.md` - AI assistant briefing (populated from template)

⏱️ **Time required:** 10-15 minutes
🎯 **Result:** Complete project foundation ready for development

Ready to begin the initialization interview? This follows the process from `.ai-rules/00_project_initialization_rule.md`.
```

Load and execute the project initialization rule:

1. Read `.ai-rules/00_project_initialization_rule.md`
2. Follow the 5-phase structured interview process
3. Generate all project foundation documents
4. Populate `AI_CONTEXT.md` with project-specific context

## Success Indicators

At completion, the user should have:

- [ ] Clean project workspace (template files removed/repositioned)
- [ ] Project-specific README (`README-project.md`)
- [ ] Clean task tracker (`TODO.md`)
- [ ] All 5 foundation documents created and populated
- [ ] `AI_CONTEXT.md` ready for Step 2 context loading
- [ ] Clear next steps for continuing the 5-step workflow

## Error Handling

**If scaffolding directory missing:**
```
❌ Error: This doesn't appear to be a fresh template.

Expected: _project-scaffolding/ directory should exist
Found: Directory missing or already processed

Solution: Start with a fresh "Save As..." copy of ai-new-project-template
```

**If file operations fail:**
```
❌ Error: File operation failed during project setup.

Check:
- File permissions in current directory
- Available disk space
- No files currently open in editor

Try: Close VS Code, reopen, and run /start-project again
```

**If initialization interview interrupted:**
```
⚠️ Setup incomplete: Project files cleaned up but initialization not finished.

To complete setup:
1. Use /orient to check current state
2. Manually run Step 1 initialization if needed
3. Follow standard 5-step workflow from Step 2
```

## Post-Command User Guidance

After successful completion:

```
✅ Project setup and initialization complete!

📁 Your project workspace:
   - README-project.md (customize this for your project)
   - TODO.md (track your development tasks)
   - .project-docs/ (your completed foundation documents)
   
🔄 Next steps in the 5-step workflow:
   Step 2: Load project context for AI assistants
   Step 3: Create PRD for your first feature
   Step 4: Generate task list
   Step 5: Execute tasks

💡 Use /orient anytime to check your current state and get guidance.
```