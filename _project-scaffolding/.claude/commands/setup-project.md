# Setup Project

One-time project workspace setup after copying from ai-new-project-template.

## Command Purpose

Run **once only** after copying the template to convert ai-new-project-template into a clean project workspace. Includes git cleanup, file transformation, and safety checks to prevent accidental re-execution.

## Execution Process

### Phase 1: Safety Validation

First, check if this project has already been set up:

```bash
# Check for scaffolding directory (indicates fresh template)
if [ ! -d "_project-scaffolding/" ]; then
    echo "❌ This project appears to already be set up."
    echo ""
    echo "🔍 Current project state:"
    ls -la | grep -E "(README-project|TODO\.md|\.project-docs)"
    echo ""
    echo "💡 Next steps:"
    echo "   • Use /orient to check your current state"
    echo "   • Use /start-coding to develop features"
    echo "   • If you need to restart, copy fresh template"
    exit 1
fi

echo "✅ Fresh template detected - proceeding with setup..."
```

### Phase 2: Git Cleanup (Critical!)

Clean up template's git history and remote:

```bash
echo "🔧 Cleaning up git configuration..."

# Remove template's git remote if it exists
if git remote get-url origin 2>/dev/null | grep -q "ai-new-project-template"; then
    echo "   🗑️  Removing template's git remote..."
    git remote remove origin
    echo "   ✅ Template remote removed"
else
    echo "   ℹ️  No template remote found"
fi

# Reset git history to clean slate
echo "   🔄 Resetting git history..."
rm -rf .git
git init
echo "   ✅ Fresh git repository initialized"

# Stage all files for initial commit
git add .
git commit -m "Initial commit from ai-new-project-template

Template version: $(date '+%Y-%m-%d')
Source: https://github.com/petergiordano/ai-new-project-template"

echo "   ✅ Clean git history created"
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

2. **Remove template files:**
   ```bash
   echo "🧹 Cleaning up template files..."
   # Remove template's README (framework instructions)
   rm -f "README-template.md" 2>/dev/null || true
   # Keep setup-claude-chat-ai/ directory for user to configure Chat AI Strategist
   echo "   ✅ Preserved setup-claude-chat-ai/ (Chat AI setup instructions)"
   ```

3. **Clean up scaffolding:**
   ```bash
   rm -rf "_project-scaffolding/"
   echo "   ✅ Removed _project-scaffolding/ (setup complete)"
   ```

### Phase 4: Enhanced Success Message & User Journey

After successful setup, provide clear guidance with journey visualization:

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
echo "   🔧 Fresh git repository initialized"
echo ""
echo "🚀 Your Development Journey:"
echo ""
echo "   1. ✅ Clone/copy template → your-project-directory"
echo "   2. ✅ /setup-project (cleanup & workspace setup) ← YOU ARE HERE"
echo "   3. 🔄 Setup Chat AI Strategist (see setup-claude-chat-ai/)"
echo "   4. 🔄 /start-coding (foundation → PRD → tasks → implementation)"
echo "   5. 🔄 /start-coding (next feature: PRD → tasks → implementation)"
echo "   6. 🧭 /orient (anytime navigation)"
echo ""
echo "💡 Next Steps:"
echo "   • RECOMMENDED: Set up Chat AI Strategist (see setup-claude-chat-ai/)"
echo "   • Connect to GitHub: Create repo, then 'git remote add origin [url]'"
echo "   • Run /start-coding to begin feature development"
echo "   • Run /orient anytime to check current state"
echo ""
echo "Ready to start building! 🚀"
```

## Safety Features

### **Prevents Double Execution**
- Checks for `_project-scaffolding/` directory existence
- Clear error message if already setup
- Guides user to appropriate next commands

### **Git Safety**
- Only removes remote if it points to template repository
- Creates clean git history with attribution to template
- Preserves any existing work if accidentally run twice

### **State Detection Output**
When already setup, shows current project state:
```
❌ This project appears to already be set up.

🔍 Current project state:
-rw-r--r--  README.md
-rw-r--r--  TODO.md
drwxr-xr-x  .project-docs

💡 Next steps:
   • Use /orient to check your current state
   • Use /start-coding to develop features
   • If you need to restart, copy fresh template
```

### **Enhanced Success Messaging**
After successful setup, users get:
- Clear confirmation of what was accomplished
- Visual journey map showing where they are
- Specific next steps with command examples
- GitHub setup guidance

## Error Handling

### **Fresh Template Validation**
```bash
if [ ! -d "_project-scaffolding/" ]; then
    # Already setup - guide to next steps
    exit 1
fi
```

### **Git Error Handling**
```bash
# Safe remote removal
if git remote get-url origin 2>/dev/null | grep -q "ai-new-project-template"; then
    git remote remove origin
fi

# Safe file operations
rm -f "README-template.md" 2>/dev/null || true
```

### **File Operation Validation**
```bash
if [ ! -f "README.md" ]; then
    echo "❌ Error: File operation failed during setup"
    echo "Check file permissions and try again"
    exit 1
fi
```

### **Recovery Guidance**
If setup fails partway through:
```
⚠️ Setup incomplete. To recover:
1. Delete any created files (README.md, TODO.md)
2. Restore _project-scaffolding/ directory if needed
3. Run /setup-project again
```

## Command Positioning

### **One-Time Setup Command**
- Clear name indicates setup purpose
- Safety checks prevent accidental re-execution
- Prepares workspace for development workflow
- **Now includes git cleanup** for complete project transformation

### **Workflow Integration**
```
User journey:
Clone template → cd your-project → /setup-project → /start-coding (or /orient)
```

### **Clear Boundaries**
- **`/setup-project`** = One-time workspace preparation + git cleanup
- **`/start-coding`** = Feature development workflow (Steps 1-5)
- **`/orient`** = Navigation and state checking