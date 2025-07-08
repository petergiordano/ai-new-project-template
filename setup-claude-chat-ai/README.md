# Claude Project Setup Guide

## 🎯 Purpose

This guide helps you create a dedicated Claude Project companion for your development work, providing persistent project knowledge and enhanced AI assistance throughout the development lifecycle.

## 🚀 Quick Setup

### 1. Create Your Claude Project
1. Go to [Claude.ai](https://claude.ai)
2. Click "Create Project" 
3. Name it: `[YourProjectName] Development`
4. Add project description

### 2. Configure Project Instructions
1. Copy `TEMPLATE_claude-project-instructions.md`
2. Fill in all `[bracketed sections]` with your project details
3. Paste into your Claude Project's instructions field

### 3. Add Knowledge Base Documents
Add these files to your Claude Project's knowledge base:
- `AI_CONTEXT.md` - Your dynamic project context
- `WORKFLOW_GUIDE.md` - Development workflow reference
- Key PRDs from `tasks/` folder
- Any project-specific reference documents

### 4. Set Up Quick Status Reference
The template includes a "Quick Project Status Reference" section that helps you:
- Quickly orient yourself at the start of each session
- Find current work status without searching
- Identify next steps immediately
- Access detailed task information

## 📋 Template Customization Guide

### Project Identity & Mission
- Replace `[PROJECT NAME]` with your actual project name
- Write a clear, one-sentence mission statement
- Keep the core mission focused and actionable

### Technical Stack & Components
- List your actual technologies, not aspirational ones
- Include version numbers for languages and frameworks
- Focus on core dependencies, not every library

### Development Philosophy
- State your actual development principles
- Make them specific to your project's needs
- Keep them actionable and measurable

### Success Metrics & Validation
- Define what "done" looks like for your project
- Include both technical and user experience metrics
- Make metrics specific and measurable

### Critical Constraints
- List real limitations you must work within
- Include technical, time, and resource constraints
- Be honest about what you cannot do

### Essential Reference Documents
- List only documents that are frequently needed
- Include their location and primary purpose
- Keep the list focused and relevant

## 🔄 Maintenance & Updates

### When to Update Project Instructions
- After completing major features
- When architectural decisions change
- When new constraints or requirements emerge
- When switching development focus areas

### What to Update
1. **Quick Project Status Reference** - Keep examples current
2. **Active Features** - Reflect current development state
3. **Success Metrics** - Adjust based on learnings
4. **Essential Documents** - Add new critical references

## 🎯 Benefits of Claude Project Integration

### Persistent Knowledge
- Project context survives between sessions
- No need to re-explain project details
- Accumulated learnings are preserved

### Quick Orientation
- Start each session with immediate context
- Find current status in seconds
- Know exactly what to work on next

### Consistent Guidance
- Architectural decisions are remembered
- Coding patterns are maintained
- Quality standards are enforced

### Enhanced Collaboration
- Better prompts for Claude Code CLI
- More strategic planning assistance
- Clearer context for decision-making

## 📚 Integration with Template Workflow

### During `/project-setup`
- Create Claude Project after workspace setup
- Use foundation interview answers for instructions
- Add initial planning documents to knowledge base

### During `/start-coding`
- Claude Project provides strategic guidance
- Prepares context-rich prompts for CLI
- Maintains architectural consistency

### During Development
- Quick status checks at session start
- Context accumulation after each feature
- Knowledge base updates with new PRDs

## 🚨 Important Notes

### Keep Instructions Focused
- Don't duplicate WORKFLOW_GUIDE.md content
- Focus on project-specific information
- Reference template documentation, don't repeat it

### Regular Maintenance
- Review and update monthly
- Keep current with project evolution
- Remove outdated information

### Knowledge Base Management
- Don't overload with every document
- Focus on frequently referenced materials
- Update key documents as they evolve

## 🎯 Next Steps

1. **Copy the template** from `TEMPLATE_claude-project-instructions.md`
2. **Customize it** with your project details
3. **Create your Claude Project** and add instructions
4. **Upload key documents** to knowledge base
5. **Start using** for enhanced AI assistance

Remember: A well-configured Claude Project acts as your persistent AI partner, maintaining context and providing consistent guidance throughout your development journey.
