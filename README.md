# AI-Assisted Project Template

### **Purpose: A streamlined workflow for developing with AI assistance.**

This repository is a template for starting new software projects using a structured, AI-assisted workflow. It provides a simple command-driven process that guides you from project idea to implementation.

## 🚀 Getting Started (2 minutes)

### **Step 1: Fork This Template**

**Create your project repository on GitHub:**

1. **Fork this repository:**
   - Click the **"Fork"** button at the top of this GitHub page
   - Choose your GitHub account as the destination
   - Name your fork (this becomes your project name)
   - ✅ **Uncheck "Copy the main branch only"** to get all template updates

2. **Clone YOUR fork locally:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
   cd YOUR-PROJECT-NAME
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

**✅ Benefits of Fork Approach:**
- **Professional GitHub workflow** - Industry standard for templates
- **Upstream template updates** - Get improvements automatically via upstream remote
- **Clean git history** - Proper project lineage and commit tracking
- **No file pollution** - GitHub handles everything correctly

## 🎯 Complete User Journey

```
1. Fork template on GitHub → your-username/your-project-name
2. Clone YOUR fork → local development
3. cd your-project-name (CRITICAL!)
4. /setup-project (one-time workspace setup + upstream remote)
5. Setup Chat AI Strategist (recommended)
6. /start-coding (foundation → PRD → tasks → implementation)
7. /start-coding (next feature: PRD → tasks → implementation)
8. /orient (anytime navigation)
```

### **What Each Command Does:**

- **`/setup-project`** - Transform template files, configure upstream remote, clean git history
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

- **Upstream Template Updates** - Pull improvements from template via `git pull upstream main`
- **Smart State Detection** - Commands know where you are in the workflow
- **Progressive Validation** - 4-level quality gates prevent error accumulation
- **Context Engineering** - AI assistants get comprehensive project context
- **Plan Mode Integration** - Safe exploration with Claude Code CLI
- **Multi-Feature Support** - Handle multiple features in same project
- **Recovery Handling** - Resume work after interruptions
- **Professional Git Workflow** - Fork → develop → sync with upstream

## 🔄 Getting Template Updates

### **Pull Latest Template Improvements:**
```bash
# Your /setup-project command configures this automatically
git pull upstream main

# Resolve any conflicts with your project-specific changes
# Your project customizations remain intact
```

**Benefits:**
- Get new AI rules and workflow improvements
- Enhanced commands and better error handling  
- New features and capabilities added to template
- Maintain your project's custom changes

## 🆘 Need Help?

### **Common Questions:**

**"What if I mess something up?"**
- Use `/orient` to check current state
- Commands include recovery guidance
- GitHub fork makes it easy to reset: re-clone your fork

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
- Should show `your-project-name`, not `ai-new-project-template`
- Run `/setup-project` to fix git configuration
- Check GitHub remote: `git remote -v` should show YOUR fork

**"How do I get template updates?"**
- Use `git pull upstream main` to get latest improvements
- `/setup-project` configures upstream remote automatically
- Resolve conflicts to keep your customizations

### **If You Get Stuck:**
1. Try `/orient` for current state and next steps
2. Check `WORKFLOW_GUIDE.md` for detailed explanations
3. Ensure you're in YOUR project directory: `pwd`
4. Verify git remotes: `git remote -v` (should show your fork + upstream)
5. Create fresh fork if needed

## 📚 Learn More

- **Complete Guide:** See `WORKFLOW_GUIDE.md` for detailed workflow
- **AI Instructions:** Explore `.ai-rules/` for AI command details
- **Context Engineering:** Built on proven AI collaboration principles
- **Template Evolution:** This template continuously improves - fork to benefit!

---

**Ready to build? Fork → Clone → `/setup-project` → `/start-coding`**

## 🎯 Why This Template Works

### **Context Engineering Excellence**
- AI assistants get comprehensive project context automatically
- Context accumulates across workflow steps for consistency
- Eliminates repetitive explanations and reduces errors

### **Professional Development Workflow**  
- GitHub fork pattern follows open-source best practices
- Upstream template updates keep your projects current
- Clean git history and proper project lineage

### **Simple, Lovable, Complete Framework**
- **Simple:** One command to start, clear next steps always
- **Lovable:** Delightful AI collaboration, minimal friction
- **Complete:** Production-ready implementations, not prototypes

**Start building with AI assistance that actually works.**