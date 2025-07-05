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
   # Copy AI rules and project docs to workspace root
   cp -r _project-scaffolding/.ai-rules .
   cp -r _project-scaffolding/.project-docs .
   
   # Optional: Remove the scaffolding directory after copying
   rm -rf _project-scaffolding
   ```

3. **Customize your README.md** - Replace this template README with your project-specific information

### **Step 3: Begin Development**

**You're now ready to start building!** Follow the complete workflow in **`WORKFLOW_GUIDE.md`**.

---

## Template Structure

This scaffolding provides a set of rule files and document templates to guide your development process. The key documents in your workspace are:

- **`README.md`**: (This file) Project overview - customize for your specific project
- **`WORKFLOW_GUIDE.md`**: The primary user manual. **Your complete development guide.**
- **`AI_CONTEXT.md`**: The master briefing document to provide context to your AI assistant

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
├── .project-docs/          # High-level project planning documents
│   ├── Roadmap.md                      # Project vision and strategy
│   ├── ComponentLibrary.md            # Design system and UI patterns
│   ├── VibeTesting.md                  # User experience and emotional design
│   └── SLC_Session_Notes.md           # Sprint planning (Simple, Lovable, Complete)
├── src/                    # Your project's source code
├── tasks/                  # PRDs and task lists (created during workflow)
├── AI_CONTEXT.md          # Dynamic project context (accumulates as you build)
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

## Support & Resources

- **Primary Guide:** See `WORKFLOW_GUIDE.md` for complete instructions
- **AI Rules:** Explore `.ai-rules/` directory for detailed AI instruction templates
- **Context Engineering:** Built on proven context engineering principles for reliable AI collaboration

---

**Ready to build something amazing with AI assistance? Start with `WORKFLOW_GUIDE.md`!**
