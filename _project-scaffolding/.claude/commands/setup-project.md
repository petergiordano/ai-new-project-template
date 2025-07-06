# Setup Project

One-time project workspace setup after "Save As..." from ai-new-project-template.

## Command Purpose

Run **once only** after "Save As..." to convert ai-new-project-template into a clean project workspace. Includes safety checks to prevent accidental re-execution.

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
    echo "   • If you need to restart, use a fresh 'Save As...' copy"
    exit 1
fi

echo "✅ Fresh template detected - proceeding with setup..."
```

### Phase 2: File Management Operations

Execute these file operations in order:

1. **Copy template files to working positions:**
   ```bash
   echo "📁 Setting up project files..."
   cp "_project-scaffolding/README-project-template.md" "README-project.md"
   cp "_project-scaffolding/TODO-template.md" "TODO.md"
   echo "   ✅ Created README-project.md"
   echo "   ✅ Created TODO.md"
   ```

2. **Prepare Chat AI setup directory:**
   ```bash
   echo "🧹 Cleaning up template files..."
   # Keep setup-claude-chat-ai/ directory for user to configure Chat AI Strategist
   echo "   ✅ Preserved setup-claude-chat-ai/ (Chat AI setup instructions)"
   # Note: Keep original README.md as framework documentation
   ```

3. **Clean up scaffolding:**
   ```bash
   rm -rf "_project-scaffolding/"
   echo "   ✅ Removed _project-scaffolding/ (setup complete)"
   ```

### Phase 3: Enhanced Success Message & User Journey

After successful setup, provide clear guidance with journey visualization:

```bash
echo ""
echo "🎉 Project workspace setup complete!"
echo ""
echo "📁 Your clean project structure:"
echo "   ✅ README-project.md (customize for your project)"
echo "   ✅ TODO.md (track development tasks)"
echo "   ✅ AI_CONTEXT.md (ready for project context)"
echo "   ✅ .ai-rules/ (workflow instructions)"
echo "   ✅ .project-docs/ (planning templates)"
echo "   ✅ src/ (source code directory)"
echo "   📋 setup-claude-chat-ai/ (Chat AI Strategist setup)"
echo ""
echo "🚀 Your Development Journey:"
echo ""
echo "   1. ✅ 'Save As...' template → your-project-workspace"
echo "   2. ✅ /setup-project (one-time workspace setup) ← YOU ARE HERE"
echo "   3. 🔄 Setup Chat AI Strategist (see setup-claude-chat-ai/)"
echo "   4. 🔄 /start-coding (foundation → PRD → tasks → implementation)"
echo "   5. 🔄 /start-coding (next feature: PRD → tasks → implementation)"
echo "   6. 🧭 /orient (anytime navigation)"
echo ""
echo "💡 Next Steps:"
echo "   • RECOMMENDED: Set up Chat AI Strategist (see setup-claude-chat-ai/)"
echo "   • Run /start-coding to begin feature development"
echo "   • Run /orient anytime to check current state"
echo "   • Your project README is now README-project.md"
echo ""
echo "Ready to start building! 🚀"
```

## Safety Features

### **Prevents Double Execution**
- Checks for `_project-scaffolding/` directory existence
- Clear error message if already setup
- Guides user to appropriate next commands

### **State Detection Output**
When already setup, shows current project state:
```
❌ This project appears to already be set up.

🔍 Current project state:
-rw-r--r--  README-project.md
-rw-r--r--  TODO.md
drwxr-xr-x  .project-docs

💡 Next steps:
   • Use /orient to check your current state
   • Use /start-coding to develop features
   • If you need to restart, use a fresh 'Save As...' copy
```

### **Enhanced Success Messaging**
After successful setup, users get:
- Clear confirmation of what was accomplished
- Visual journey map showing where they are
- Specific next steps with command examples
- Context about their new project structure

## Error Handling

### **Fresh Template Validation**
```bash
if [ ! -d "_project-scaffolding/" ]; then
    # Already setup - guide to next steps
    exit 1
fi
```

### **File Operation Validation**
```bash
if [ ! -f "README-project.md" ]; then
    echo "❌ Error: File operation failed during setup"
    echo "Check file permissions and try again"
    exit 1
fi
```

### **Recovery Guidance**
If setup fails partway through:
```
⚠️ Setup incomplete. To recover:
1. Delete any created files (README-project.md, TODO.md)
2. Restore _project-scaffolding/ directory if needed
3. Run /setup-project again
```

## Command Positioning

### **One-Time Setup Command**
- Clear name indicates setup purpose
- Safety checks prevent accidental re-execution
- Prepares workspace for development workflow

### **Workflow Integration**
```
User journey:
"Save As..." → /setup-project → /start-coding (or /orient)
```

### **Clear Boundaries**
- **`/setup-project`** = One-time workspace preparation
- **`/start-coding`** = Feature development workflow (Steps 1-5)
- **`/orient`** = Navigation and state checking