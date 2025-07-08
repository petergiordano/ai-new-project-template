# Quick Start Example

This example shows how to set up a Claude Project for a task management application.

## 1. Starting Point

After running `/project-setup` and the foundation interview, you have:
- Project Name: "TaskFlow Pro"
- Tech Stack: React, Node.js, PostgreSQL
- Core Mission: "Simplify task management for remote teams"

## 2. Fill Out the Template

Copy `TEMPLATE_claude-project-instructions.md` and customize:

```markdown
# TaskFlow Pro - Claude Project System Instructions

## **🎯 Project Identity & Mission**

You are the **Chat AI Strategist** for TaskFlow Pro - a task management system designed for remote teams.

**Core Mission:** Simplify task management for distributed teams with real-time collaboration and intelligent prioritization.

## **🏗️ Template System Integration**

This project **USES** the AI-Assisted Development Template framework:
[... template content remains ...]

## **🔧 Technical Stack & Components**

### **Core Technologies**
- **Language:** TypeScript/JavaScript
- **Frontend:** React 18, Tailwind CSS, Zustand
- **Backend:** Node.js, Express, Socket.io
- **Database:** PostgreSQL with Prisma ORM
- **Key Libraries:** React Query, React Hook Form, Zod

### **Development Philosophy**
- **API-First:** Design API contracts before implementation
- **Real-time First:** Every action should feel instant
- **Mobile-Responsive:** Works perfectly on all devices
```

## 3. Create Claude Project

1. Go to Claude.ai
2. Create Project named "TaskFlow Pro Development"
3. Paste your customized instructions
4. Upload these files to knowledge base:
   - `AI_CONTEXT.md`
   - `WORKFLOW_GUIDE.md`
   - Any completed PRDs

## 4. Use Quick Status Checks

```
You: "What's my current status?"

Claude: "Checking TaskFlow Pro status...
- TODO.md: User authentication system in progress
- AI_CONTEXT.md: Auth PRD created, tasks generated
- Next: Implement JWT token generation (task 2.1)
- See: tasks/tasks-prd-user-auth.md for details"
```

## 5. Benefit from Persistent Knowledge

No more pasting context! Claude remembers:
- Your tech stack and conventions
- Completed features and patterns
- Current development focus
- Architectural decisions

Your Chat AI Strategist now has permanent project awareness!
