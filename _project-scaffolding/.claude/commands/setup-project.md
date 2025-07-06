# Setup Project

One-time project workspace setup after forking ai-new-project-template.

## Command Purpose

Run **once only** after forking and cloning the template to convert ai-new-project-template into a clean project workspace. Includes upstream remote configuration, file transformation, and safety checks to prevent accidental re-execution.

## Execution Process

### Phase 1: Safety Validation

First, check if this project has already been set up:

```bash
# Check for scaffolding directory (indicates fresh template)
if [ ! -d "_project-scaffolding/" ]; then
    echo "❌ This project appears to already be set up."
    echo ""
    echo "🔍 Current project state:"
    ls -la | grep -E "(README\.md|TODO\.md|\.project-docs)"
    echo ""
    echo "💡 Next steps:"
    echo "   • Use /orient to check your current state"
    echo "   • Use /start-coding to develop features"
    echo "   • Get template updates: git pull upstream main"
    exit 1
fi

echo "✅ Fresh template detected - proceeding with setup..."
```

### Phase 2: Smart Git Configuration

Configure git remotes properly for fork workflow with upstream template updates:

```bash
echo "🔧 Configuring git for template updates..."

# Check current git status
CURRENT_REMOTE=$(git remote get-url origin 2>/dev/null || echo "none")
echo "   📡 Current origin: $CURRENT_REMOTE"

# Add upstream remote to original template (if not already exists)
if ! git remote get-url upstream 2>/dev/null; then
    echo "   🔗 Adding upstream remote for template updates..."
    git remote add upstream https://github.com/petergiordano/ai-new-project-template.git
    echo "   ✅ Upstream remote added: ai-new-project-template"
else
    echo "   ✅ Upstream remote already configured"
fi

# Verify remote configuration
echo "   📋 Git remote configuration:"
git remote -v | sed 's/^/      /'

# Fetch upstream to enable template updates
echo "   ⬇️  Fetching upstream template for future updates..."
git fetch upstream --quiet
echo "   ✅ Template update capability configured"
```

### Phase 3: File Management Operations

Execute these file operations in order:

1. **Copy template files to working positions:**
   ```bash
   echo "📁 Setting up project files..."
   cp "_project-scaffolding/README-project-template.md" "README.md"
   cp "_project-scaffolding/TODO-template.md" "TODO.md"
   echo "   ✅ Created README.md (project-focused)"
   echo "   ✅ Created TODO.md (project task tracking)"
   ```

2. **Clean up scaffolding but preserve important directories:**
   ```bash
   echo "🧹 Cleaning up template files..."
   # Remove scaffolding directory (setup complete)
   rm -rf "_project-scaffolding/"
   echo "   ✅ Removed _project-scaffolding/ (setup complete)"
   
   # Keep setup-claude-chat-ai/ directory for user to configure Chat AI Strategist
   echo "   ✅ Preserved setup-claude-chat-ai/ (Chat AI setup instructions)"
   
   # Keep all other template files for upstream merging capability
   echo "   ✅ Preserved template files (enables upstream updates)"
   ```

3. **Commit the project setup:**
   ```bash
   echo "💾 Creating setup commit..."
   git add README.md TODO.md
   git add -u  # Add removal of _project-scaffolding/
   git commit -m "feat: convert template to project workspace

- Transform README-project-template.md → README.md
- Transform TODO-template.md → TODO.md  
- Remove _project-scaffolding/ (setup complete)
- Configure upstream for template updates

Template source: $(git remote get-url upstream)
Setup date: $(date '+%Y-%m-%d %H:%M:%S')"
   echo "   ✅ Project setup committed to git history"
   ```

### Phase 4: Template Update Instructions & Success Message

```bash
echo ""
echo "🎉 Project workspace setup complete!"
echo ""
echo "📁 Your clean project structure:"
echo "   ✅ README.md (your project documentation)"
echo "   ✅ TODO.md (development task tracking)"  
echo "   ✅ AI_CONTEXT.md (ready for project context)"
echo "   ✅ .ai-rules/ (workflow instructions)"
echo "   ✅ .project-docs/ (planning templates)"
echo "   ✅ src/ (source code directory)"
echo "   📋 setup-claude-chat-ai/ (Chat AI setup instructions)"
echo "   🔗 Git remotes configured (origin + upstream)"
echo ""
echo "🔄 Template Update Capability:"
echo "   📡 Origin: $(git remote get-url origin)"
echo "   ⬆️  Upstream: $(git remote get-url upstream)"
echo "   💡 Get updates anytime: git pull upstream main"
echo ""
echo "🚀 Your Development Journey:"
echo ""
echo "   1. ✅ Fork template on GitHub → your-username/your-project-name"
echo "   2. ✅ Clone YOUR fork → local development"
echo "   3. ✅ /setup-project (workspace setup + upstream) ← YOU ARE HERE"
echo "   4. 🔄 Setup Chat AI Strategist (see setup-claude-chat-ai/)"
echo "   5. 🔄 /start-coding (foundation → PRD → tasks → implementation)"
echo "   6. 🔄 /start-coding (next feature: PRD → tasks → implementation)"
echo "   7. 🧭 /orient (anytime navigation)"
echo ""
echo "💡 Next Steps:"
echo "   • RECOMMENDED: Set up Chat AI Strategist (see setup-claude-chat-ai/)"
echo "   • Run /start-coding to begin feature development"
echo "   • Run /orient anytime to check current state"
echo ""
echo "🔄 Getting Template Updates:"
echo "   • New AI rules: git pull upstream main"
echo "   • Enhanced commands: git pull upstream main"  
echo "   • Workflow improvements: git pull upstream main"
echo "   • Resolve conflicts to keep your customizations"
echo ""
echo "Ready to start building with continuous template updates! 🚀"
```

## Template Update Workflow

### **How Users Get Template Updates:**

1. **Automatic upstream configuration** - `/setup-project` adds upstream remote
2. **Simple update command** - `git pull upstream main` 
3. **Smart conflict resolution** - Git preserves user customizations
4. **Selective updates** - Users can review changes before merging

### **What Gets Updated:**
- **AI rule files** (`.ai-rules/`) - Improved workflow instructions
- **Command enhancements** (`.claude/commands/`) - Better automation
- **Template files** (`.project-docs/`) - Enhanced planning documents
- **Documentation** (`WORKFLOW_GUIDE.md`) - Latest best practices

### **What Stays Custom:**
- **Project files** (`README.md`, `TODO.md`) - User's specific content
- **Source code** (`src/`) - User's application
- **Project context** (`AI_CONTEXT.md`) - User's project specifics
- **Tasks and PRDs** (`tasks/`) - User's feature work

### **Conflict Resolution Example:**
```bash
# User gets template updates
git pull upstream main

# If conflicts exist, git will prompt
# User resolves conflicts keeping their customizations
# Template improvements merge with user's project
```

## Safety Features

### **Prevents Double Execution**
- Checks for `_project-scaffolding/` directory existence
- Clear error message if already setup
- Guides user to appropriate next commands including update instructions

### **Git Safety & Fork Preservation**
- **Preserves fork relationship** - Keeps connection to user's GitHub repo
- **Adds upstream remote** - Enables template updates via upstream
- **Maintains git history** - Proper fork lineage for GitHub
- **Smart remote detection** - Verifies and reports git configuration

### **Template Update Safety**
- **Preserves user changes** - Git merge respects customizations
- **Clear update instructions** - Users know exactly how to get updates
- **Conflict resolution** - Standard git workflow for handling conflicts
- **Selective updates** - Users can review before accepting changes

### **Enhanced State Detection**
When already setup, shows current project state and update capability:
```
❌ This project appears to already be set up.

🔍 Current project state:
-rw-r--r--  README.md
-rw-r--r--  TODO.md
drwxr-xr-x  .project-docs

💡 Next steps:
   • Use /orient to check your current state
   • Use /start-coding to develop features  
   • Get template updates: git pull upstream main
```

## Error Handling

### **Git Configuration Validation**
```bash
# Verify git repository exists
if [ ! -d ".git" ]; then
    echo "❌ Error: Not in a git repository"
    echo "Make sure you cloned your fork: git clone [your-fork-url]"
    exit 1
fi

# Verify we're in a fork (has origin remote)
if ! git remote get-url origin 2>/dev/null; then
    echo "❌ Error: No origin remote found" 
    echo "Make sure you cloned your fork properly"
    exit 1
fi
```

### **Upstream Remote Handling**
```bash
# Safe upstream remote addition
if ! git remote get-url upstream 2>/dev/null; then
    git remote add upstream https://github.com/petergiordano/ai-new-project-template.git
    echo "✅ Upstream remote added"
else
    echo "ℹ️ Upstream remote already exists"
fi

# Verify upstream fetch capability
if ! git fetch upstream --dry-run 2>/dev/null; then
    echo "⚠️ Warning: Could not fetch from upstream"
    echo "Template updates may not work - check internet connection"
fi
```

### **File Operation Validation**
```bash
# Verify file transformation succeeded
if [ ! -f "README.md" ] || [ ! -f "TODO.md" ]; then
    echo "❌ Error: File transformation failed"
    echo "Check file permissions and template integrity"
    exit 1
fi

# Verify scaffolding cleanup
if [ -d "_project-scaffolding/" ]; then
    echo "⚠️ Warning: Scaffolding directory still exists"
    echo "Setup may be incomplete"
fi
```

### **Recovery Guidance**
If setup fails or user needs template updates:
```
🔄 Template Update Recovery:
1. Check remotes: git remote -v
2. Add upstream if missing: git remote add upstream [template-url] 
3. Fetch updates: git fetch upstream
4. Merge updates: git pull upstream main
5. Resolve conflicts keeping your customizations
```

## Command Positioning

### **Fork-Aware Setup Command**
- Preserves GitHub fork relationship for professional workflow
- Configures upstream remote for continuous template improvements
- Maintains git history for proper project lineage
- **Enables template evolution inheritance**

### **Workflow Integration**
```
User journey:
Fork template → Clone YOUR fork → cd your-project → /setup-project → /start-coding
                                                        ↓
                                            Configures template updates
```

### **Template Evolution Support**
- **`/setup-project`** = One-time workspace preparation + upstream configuration
- **`git pull upstream main`** = Get latest template improvements
- **`/start-coding`** = Feature development workflow (Steps 1-5)
- **`/orient`** = Navigation and state checking

## Key Benefits

### **Continuous Template Improvement**
- Users get AI rule enhancements automatically
- Command improvements flow to existing projects  
- Workflow optimizations benefit all users
- Bug fixes reach users without manual intervention

### **Professional Git Workflow**
- Proper fork relationship maintained
- GitHub integration preserved
- Standard open-source contribution model
- Clean git history with template attribution

### **User Customization Protection**
- Project-specific files remain untouched by updates
- Git merge preserves user modifications
- Conflict resolution for overlapping changes
- User maintains full control over their project