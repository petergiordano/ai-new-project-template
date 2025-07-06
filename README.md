# AI-Assisted Project Template (Manual Workflow)

### **Purpose: A step-by-step, human-guided workflow for developing with AI.**

This repository is a scaffolding template for starting new software projects using a structured, AI-assisted workflow. It is designed for a "human-in-the-loop" process where you guide an AI assistant through each step of development.

This template is ideal for:
- Smaller, well-defined features.
- Projects where you need precise control over every implementation detail.
- Learning a new codebase or framework with AI assistance.

## 🚀 Quick Start

### **Step 1: Set Up Your Project Workspace**

**Important:** This is a *template repository* - you'll create your actual project workspace from it.

#### **Option A: Save As New Project (Recommended for Personal Use)**
1. **Open this template directory** in your file manager
2. **Save entire folder as new project:**
   - Copy the entire `ai-new-project-template` folder
   - Rename the copy to your project name (e.g., `my-awesome-app`)
   - Navigate into your new project folder
3. **Initialize as new git repository:**
   ```bash
   cd your-project-name
   rm -rf .git  # Remove template git history
   git init
   git add .
   git commit -m "Initial commit from AI-assisted project template"
   ```

#### **Option B: Use GitHub Template**
1. **Click "Use this template"** button on GitHub
2. **Create your new repository** with your project name
3. **Clone your new project** to your local machine:
   ```bash
   git clone https://github.com/your-username/your-project-name.git
   cd your-project-name
   ```

### **Step 2: Prepare Your Workspace**

Once you have your project workspace set up:

1. **Verify template structure** is in place:
   ```
   your-project-name/
   ├── .ai-rules/              # AI instruction sets (copy from _project-scaffolding)
   ├── .project-docs/          # Planning documents (copy from _project-scaffolding)
   ├── src/                    # Your actual source code (initially empty)
   ├── AI_CONTEXT.md           # Master AI briefing document
   ├── README.md               # This file (customize for your project)
   └── WORKFLOW_GUIDE.md       # Workflow instructions
   ```

2. **Copy scaffolding files** to your workspace root:
   ```bash
   # Copy AI rules, project docs, and Claude config to workspace root
   cp -r _project-scaffolding/.ai-rules .
   cp -r _project-scaffolding/.claude .
   cp -r _project-scaffolding/.project-docs .
   
   # Optional: Remove the scaffolding directory after copying
   rm -rf _project-scaffolding
   ```

3. **Customize your README.md** - Replace this template README with your project-specific information

### **Step 3: Begin Development**

**You're now ready to start building!** Follow the complete workflow in **`WORKFLOW_GUIDE.md`**.

## 🚀 Getting Started: Your First 15 Minutes

### **You've Set Up Your Workspace - Now What?**

**Congratulations!** You have a new project workspace from the template. Here's exactly what to do next:

### **⚡ Immediate Actions (5 minutes)**

1. **📂 Open your project workspace** in VS Code:
   ```bash
   cd your-project-name
   code .
   ```

2. **✅ Verify setup** - Run the workspace checklist from WORKFLOW_GUIDE.md:
   ```bash
   pwd  # Should show your project path
   ls -la  # Should see .ai-rules/, .claude/, .project-docs/, src/, AI_CONTEXT.md
   ```

3. **🎯 Choose your path** based on your current needs:

### **📋 Path A: Start a New Project (Most Common)**
**⏱️ Time: 10 minutes**  
**Outcome:** Populated project documents + ready to build first feature

```
→ Follow Step 1 in WORKFLOW_GUIDE.md
→ AI-driven interview creates your project foundation  
→ Generates: Roadmap.md, VibeTesting.md, ComponentLibrary.md, SLC_Session_Notes.md, AI_CONTEXT.md
→ Ready to build features with Steps 2-5
→ Optional: Consider Claude Task Master integration for advanced task management
```

**Next Action:** Open WORKFLOW_GUIDE.md and go to "Step 1: Generate Project Context Documents"

### **📋 Path B: Add Template to Existing Project**
**⏱️ Time: 5 minutes**  
**Outcome:** Template integrated with your existing codebase

```
→ Move your existing code into src/ directory
→ Manually populate AI_CONTEXT.md with your project details
→ Skip to Step 2 in WORKFLOW_GUIDE.md
→ Ready to build new features with AI assistance
```

**Next Action:** Move existing code to `src/`, then populate `AI_CONTEXT.md` manually

### **📋 Path C: Explore and Learn**
**⏱️ Time: 15 minutes**  
**Outcome:** Understanding of the workflow without committing to a project

```
→ Read through WORKFLOW_GUIDE.md completely
→ Explore .ai-rules/ directory to understand AI instructions
→ Review .project-docs/ templates
→ Come back when ready to start a real project
```

**Next Action:** Open WORKFLOW_GUIDE.md and read the complete workflow

---

### **🎯 Success Indicators**

**You're ready to proceed when:**
- ✅ You're in your project workspace (not the template)
- ✅ All template files are present in your workspace
- ✅ You've chosen Path A, B, or C above
- ✅ You know your immediate next action

### **🆘 Need Help?**

**Common Issues:**
- **"I don't see .ai-rules/ directory"** → You're still in the template. Navigate to your project workspace.
- **"Which AI should I use?"** → Start with any Chat AI (Claude, ChatGPT, Gemini) for strategy, then use CLI AI for implementation.
- **"I don't know what to build"** → Follow Path A - the AI interview will help you define your project.

**Next Steps:** Open `WORKFLOW_GUIDE.md` and follow your chosen path!

---

## Template Structure

This scaffolding provides a set of rule files and document templates to guide your development process. The key documents in your workspace are:

- **`README.md`**: (This file) Project overview - customize for your specific project
- **`WORKFLOW_GUIDE.md`**: The primary user manual. **Your complete development guide.**
- **`AI_CONTEXT.md`**: The master briefing document to provide context to your AI assistant
- **`CLAUDE.md`**: Claude Code CLI context file (automatically loads AI_CONTEXT.md)
- **`GEMINI.md`**: Gemini CLI context file (automatically loads AI_CONTEXT.md)

### **Workspace Structure After Setup:**
```
your-project-name/
├── .ai-rules/              # Specific instruction sets for the AI
│   ├── 00_project-initialization.md     # AI-driven project setup
│   ├── 01_create-prd.md                # Product Requirements creation
│   ├── 02_generate-tasks.md            # Task breakdown from PRDs
│   ├── 03_execute-tasks.md             # Task execution with validation
│   ├── 04_plan-mode-best-practices.md  # Claude Code Plan Mode guide
│   ├── 05_generate-prd-command.md      # Enhanced PRD generation
│   ├── 06_generate-tasks-command.md    # Enhanced task generation
│   ├── 07_context-validation-checkpoints.md  # Context validation
│   └── 08_validation-loops.md          # Progressive validation system
├── .claude/                # Claude Code configuration and commands
│   ├── commands/
│   │   └── orient.md                   # Universal project navigation command
│   └── settings.local.json             # Claude Code permissions
├── .project-docs/          # High-level project planning documents
│   ├── Roadmap.md                      # Project vision and strategy
│   ├── ComponentLibrary.md            # Design system and UI patterns
│   ├── VibeTesting.md                  # User experience and emotional design
│   └── SLC_Session_Notes.md           # Sprint planning (Simple, Lovable, Complete)
├── src/                    # Your project's source code
├── tasks/                  # PRDs and task lists (created during workflow)
├── AI_CONTEXT.md          # Dynamic project context (accumulates as you build)
├── CLAUDE.md              # Claude Code CLI automatic context loading
├── GEMINI.md              # Gemini CLI automatic context loading
├── README.md              # Project overview (customize this!)
└── WORKFLOW_GUIDE.md      # Complete development workflow guide
```

### **Template vs. Project Workspace**

**🔍 Understanding the Distinction:**

- **This Template Repository:** Contains the scaffolding, rules, and workflow guides
- **Your Project Workspace:** Where you'll actually build your application using the template

**Template Structure (what you're looking at now):**
```
ai-new-project-template/           # ← Template repository
├── _project-scaffolding/          # ← Scaffolding to copy to projects
│   ├── .ai-rules/                # ← AI instruction files
│   ├── .project-docs/            # ← Planning document templates
│   └── src/                      # ← Empty source directory
├── README.md                     # ← Template instructions (this file)
├── WORKFLOW_GUIDE.md             # ← Workflow documentation
└── AI_CONTEXT.md                 # ← AI context template
```

**Your Project Workspace (after setup):**
```
your-awesome-app/                  # ← Your actual project
├── .ai-rules/                    # ← Copied from template
├── .project-docs/                # ← Copied from template  
├── src/                          # ← Your actual application code
├── tasks/                        # ← Created during development
├── AI_CONTEXT.md                 # ← Populated with your project details
├── README.md                     # ← Customized for your project
└── WORKFLOW_GUIDE.md             # ← Your development guide
```

## Getting Started

To begin using this template, follow these steps:

1. **✅ Set up your workspace** (Steps 1-2 above)
2. **📖 Read the complete workflow** in **`WORKFLOW_GUIDE.md`**
3. **🚀 Start building** with the 5-step AI-assisted development process

---

## Advanced Features

This template includes advanced context engineering capabilities:

- **🔄 Dynamic Context Accumulation:** AI_CONTEXT.md evolves with your project
- **✅ Progressive Validation Loops:** 4-level validation prevents error accumulation
- **🎯 Context Convergence:** AI assistants maintain project awareness across sessions
- **⚡ Command-Driven Workflow:** Structured commands for PRD → Tasks → Implementation
- **🛡️ Plan Mode Integration:** Safe exploration and analysis with Claude Code CLI
- **🔧 CLI Context Integration:** CLAUDE.md and GEMINI.md automatically load project context
- **⚡ Zero-Setup CLI Assistance:** Claude Code and Gemini CLI get full project context on startup
- **🧠 Universal `/orient` Command:** Get re-oriented and see next best actions from anywhere in your project
- **🚀 Claude Task Master Integration:** Optional advanced task management with dependency tracking and complexity analysis

## Support & Resources

- **Primary Guide:** See `WORKFLOW_GUIDE.md` for complete instructions
- **AI Rules:** Explore `.ai-rules/` directory for detailed AI instruction templates
- **Context Engineering:** Built on proven context engineering principles for reliable AI collaboration
- **Advanced Task Management:** Optional Claude Task Master integration for sophisticated task execution (see WORKFLOW_GUIDE.md)

---

**Ready to build something amazing with AI assistance? Start with `WORKFLOW_GUIDE.md`!**
