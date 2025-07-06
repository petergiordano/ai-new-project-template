# AI-Assisted Project Template

### **Purpose: A streamlined workflow for developing with AI assistance.**

This repository is a template for starting new software projects using a structured, AI-assisted workflow. It provides a simple command-driven process that guides you from project idea to implementation.

## 🚀 Getting Started (3 minutes)

### **Step 1: Copy Template to Your Project**

**Create your project workspace:**

1. **Download/clone this template:**
   ```bash
   # Option A: Download and extract ZIP from GitHub
   # Option B: Clone the template
   git clone https://github.com/petergiordano/ai-new-project-template.git your-project-name
   ```

2. **Navigate to your project:**
   ```bash
   cd your-project-name
   ```

3. **Open in VS Code:**
   ```bash
   code .
   ```

### **Step 2: Essential Setup**

**Open terminal in VS Code and run these commands:**

```bash
# Start Claude Code CLI (make sure you're in YOUR project directory)
claude

# Set up your project workspace (one-time only)
/setup-project

# Begin feature development 
/start-coding
```

**⚠️ Critical:** Make sure your terminal is in YOUR project directory, not the original template directory!

## 🎯 Complete User Journey

```
1. Clone/copy template → your-project-directory
2. cd your-project-directory (IMPORTANT!)
3. /setup-project (one-time workspace setup & git cleanup)
4. Setup Chat AI Strategist (recommended)
5. /start-coding (foundation → PRD → tasks → implementation)
6. /start-coding (next feature: PRD → tasks → implementation)
7. /orient (anytime navigation)
```

### **What Each Command Does:**

- **`/setup-project`** - One-time cleanup, git reset, and workspace preparation
- **`/start-coding`** - Intelligent feature development orchestrator  
- **`/orient`** - Check current state and get guidance anytime

## 🧠 How It Works

### **3-Party Collaboration Model**
- **You:** Project director making decisions
- **Chat AI:** Strategic planning and context preparation
- **CLI AI:** Technical implementation and file operations

### **5-Step Workflow (Automated)**
1. **Project Foundation** - AI interview creates project context
2. **Dynamic Context** - Automatic context loading for AI assistants  
3. **Feature Planning** - PRD creation with validation criteria
4. **Task Generation** - Detailed implementation breakdown
5. **Quality Implementation** - Code execution with progressive validation

## 📂 Template Structure

After `/setup-project`, your workspace will look like:

```
your-project/
├── .claude/                    # Claude Code configuration
├── .ai-rules/                  # AI workflow instructions
├── .project-docs/              # Project planning documents
├── src/                        # Your application source code
├── tasks/                      # Feature PRDs and task lists
├── setup-claude-chat-ai/       # Chat AI Strategist setup instructions
├── README.md                   # Your project's README (this gets replaced)
├── TODO.md                     # Development task tracking
├── AI_CONTEXT.md              # AI assistant briefing
└── WORKFLOW_GUIDE.md          # Complete workflow documentation
```

## ⚡ Advanced Features

- **Smart State Detection** - Commands know where you are in the workflow
- **Progressive Validation** - 4-level quality gates prevent error accumulation
- **Context Engineering** - AI assistants get comprehensive project context
- **Plan Mode Integration** - Safe exploration with Claude Code CLI
- **Multi-Feature Support** - Handle multiple features in same project
- **Recovery Handling** - Resume work after interruptions
- **Git Cleanup** - Automatically resets git history for your project

## 🆘 Need Help?

### **Common Questions:**

**"What if I mess something up?"**
- Use `/orient` to check current state
- Commands include recovery guidance
- Safe to restart with fresh template copy

**"Can I use different AI assistants?"**
- Yes! Works with Claude, ChatGPT, Gemini
- Template provides context for any AI assistant
- CLI AI gets automatic project context

**"How do I add multiple features?"**
- Run `/start-coding` for each new feature
- System tracks multiple PRDs and task lists
- Maintains project-wide context

**"I'm getting git errors or wrong directory issues"**
- Make sure you're in YOUR project directory: `pwd`
- Run `/setup-project` to clean up git and file structure
- Check that terminal shows your project name, not 'ai-new-project-template'

### **If You Get Stuck:**
1. Try `/orient` for current state and next steps
2. Check `WORKFLOW_GUIDE.md` for detailed explanations
3. Ensure you're in the correct directory: `pwd`
4. Use fresh template copy if needed

## 📚 Learn More

- **Complete Guide:** See `WORKFLOW_GUIDE.md` for detailed workflow
- **AI Instructions:** Explore `.ai-rules/` for AI command details
- **Context Engineering:** Built on proven AI collaboration principles

---

**Ready to build? Clone → cd your-project → `/setup-project` → `/start-coding`**