# Claude Code APM - Beginner's Setup Guide

A step-by-step guide to using the Agentic Project Management (APM) framework with Claude Code.

## Table of Contents
1. [What is APM with Claude Code?](#what-is-apm-with-claude-code)
2. [Prerequisites](#prerequisites)
3. [Initial Setup](#initial-setup)
4. [Understanding CLAUDE.md and Slash Commands](#understanding-claudemd-and-slash-commands)
5. [The APM Workflow Loop](#the-apm-workflow-loop)
6. [Step-by-Step Tutorial](#step-by-step-tutorial)
7. [Common Scenarios](#common-scenarios)
8. [Tips for Success](#tips-for-success)
9. [Troubleshooting](#troubleshooting)

## What is APM with Claude Code?

APM is like having a project management team where:
- **Manager Agent** = Your project coordinator (plans and assigns work)
- **Implementation Agents** = Your developers (do the actual work)
- **Memory Bank** = Your project documentation (keeps everyone in sync)

With Claude Code, each team member is a separate Claude instance working together through shared files.

## Prerequisites

Before starting, ensure you have:
1. **Claude Code access** at [claude.ai/code](https://claude.ai/code)
2. **This APM repository** cloned or accessible
3. **A project idea** you want to build
4. **Basic understanding** of opening multiple browser tabs/windows

## Initial Setup

### Step 1: Prepare Your Workspace

1. Create a new folder for your project:
   ```
   my-awesome-project/
   ```

2. Copy the APM framework into your project (or keep it separate - your choice):
   ```
   my-awesome-project/
   ├── APM/                    # (optional) Copy of APM framework
   └── ... (your project files will go here)
   ```

### Step 2: Open Your First Claude Code Instance (Manager)

1. Open [claude.ai/code](https://claude.ai/code) in a browser tab
2. Label this tab "Manager Agent" (helps keep track!)
3. Navigate to your project folder

**Important**: If your project has a `CLAUDE.md` file in the root directory, Claude Code automatically loads it. This means:
- Claude instantly knows all APM commands and workflows
- No need to manually explain the system
- Commands work immediately without setup

## Understanding CLAUDE.md and Slash Commands

### What is CLAUDE.md?

CLAUDE.md is a special file that Claude Code automatically loads when you open a project. Think of it as Claude's "instruction manual" for your project. When present, it:

- **Loads automatically**: No need to manually reference it
- **Provides instant context**: Claude immediately knows all available commands
- **Defines workflows**: Contains the complete APM system documentation

### Using Slash Commands

APM includes pre-built slash commands that make complex operations simple. These commands are stored in `.claude/commands/` and appear when you type `/project:` in Claude Code.

#### Two Ways to Use Commands:

**1. Traditional Method (Manual):**
```
# Navigate to prompts folder
# Copy entire content of 01_Initiation_Prompt.md
# Paste into Claude
```

**2. Slash Command Method (Automatic):**
```
/project:apm-init-manager
```

#### Benefits of Slash Commands:

| Aspect | Manual Method | Slash Commands |
|--------|---------------|----------------|
| **Speed** | Navigate → Find → Copy → Paste | Type → Enter |
| **Accuracy** | Risk of partial copying | Always complete |
| **Updates** | May use old versions | Always current |
| **Discovery** | Need to know file locations | Auto-complete helps |

#### Available Command Categories:

**Initialization Commands:**
- `/project:apm-init-manager` - Initialize as Manager Agent
- `/project:apm-init-implement` - Initialize as Implementation Agent
- `/project:apm-init-debug` - Initialize as Debug Agent
- `/project:apm-init-test` - Initialize as Test Agent
- `/project:apm-init-review` - Initialize as Review Agent

**Manager Commands:**
- `/project:manager-discover` - Start project discovery
- `/project:manager-plan` - Create implementation plan
- `/project:manager-review` - Review completed work
- `/project:manager-handover` - Prepare Manager handover

**Implementation Commands:**
- `/project:implement-start` - Begin task implementation
- `/project:implement-status` - Report progress
- `/project:implement-complete` - Complete and log task

**Task Management:**
- `/project:task-prompt` - Generate task assignment
- `/project:load-task-clipboard` - Load task from clipboard
- `/project:load-task-file` - Load task from file

**Memory Bank Commands:**
- `/project:memory-read` - Read Memory Bank entries
- `/project:memory-log` - Add to Memory Bank
- `/project:memory-validate` - Check Memory Bank integrity
- `/project:memory-sync` - Synchronize Memory Bank

**Utility Commands:**
- `/project:apm-status` - Check current state
- `/project:apm-sync` - Synchronize project
- `/project:apm-context-save` - Save context
- `/project:apm-context-load` - Load saved context

## The APM Workflow Loop

Here's how the workflow cycles:

```
┌─────────────────────────────────────────────────────┐
│                   THE APM LOOP                      │
├─────────────────────────────────────────────────────┤
│                                                     │
│  1. Manager Plans        →  2. Manager Assigns     │
│     (/manager plan)          (/task-prompt)        │
│          ↓                         ↓                │
│                                                     │
│  4. Manager Reviews      ←  3. Implementation Does │
│     (/manager review)          (/implement)        │
│          ↓                         ↓                │
│                                                     │
│  5. Update Plan/Repeat   →  Memory Bank Updated    │
│                                 (automatic)         │
└─────────────────────────────────────────────────────┘
```

## Step-by-Step Tutorial

### Phase 1: Initialize Your Manager Agent

**In your Manager Agent tab:**

1. Initialize the Manager role (choose one method):
   
   **Using Slash Command (Recommended):**
   ```
   /project:apm-init-manager
   ```
   
   **Traditional Method:**
   ```
   # Copy content from prompts/00_Initial_Manager_Setup/01_Initiation_Prompt.md
   # Paste into Claude
   ```
   
   Claude responds: "Initialized as Manager Agent for APM project..."

2. Start project discovery:
   
   **Using Slash Command:**
   ```
   /project:manager-discover
   ```
   
   **Traditional Method:**
   ```
   /manager discover
   ```
   
   Claude will ask you questions about your project. For example:
   - What are you building?
   - What technologies do you want to use?
   - What are your main requirements?

3. Let Claude create the Implementation Plan:
   
   **Using Slash Command:**
   ```
   /project:manager-plan
   ```
   
   **Traditional Method:**
   ```
   /manager plan
   ```
   
   This creates two key files:
   - `Implementation_Plan.md` - Your project roadmap
   - `Memory_Bank.md` (or `Memory/` folder) - Your project log

### Phase 2: Assign Your First Task

**Still in Manager Agent tab:**

1. Generate a task assignment:
   
   **Using Slash Command:**
   ```
   /project:task-prompt task-1.1
   ```
   
   Claude will output a formatted prompt like:
   ```
   # APM Task Assignment: Setup Project Structure
   
   ## Task ID: task-1.1
   ## Assigned to: Implementation Agent A
   
   [Details about what needs to be done...]
   ```

2. **Copy this entire prompt** to your clipboard

### Phase 3: Create Your First Implementation Agent

**Open a NEW Claude Code instance (new tab/window):**

1. Label this tab "Implementation Agent A"
2. Navigate to the same project folder
3. Initialize as Implementation Agent:
   
   **Using Slash Command:**
   ```
   /project:apm-init-implement
   ```
   
   **Traditional Method:**
   ```
   # Copy content from prompts/02_Utility_Prompts_And_Format_Definitions/Implementation_Agent_Onboarding.md
   # Paste into Claude
   ```

4. Load the task you copied:
   
   **Using Slash Command:**
   ```
   /project:load-task-clipboard
   ```
   
   Claude responds with task details and readiness.

5. Start working:
   
   **Using Slash Command:**
   ```
   /project:implement-start
   ```
   
   Claude begins implementing the task.

6. When done, complete the task:
   
   **Using Slash Command:**
   ```
   /project:implement-complete
   ```
   
   This automatically logs the work to Memory Bank.

### Phase 4: Review and Continue

**Back in your Manager Agent tab:**

1. Sync with latest changes:
   
   **Using Slash Command:**
   ```
   /project:apm-sync
   ```

2. Review the completed work:
   
   **Using Slash Command:**
   ```
   /project:manager-review
   ```
   
   Claude examines the Memory Bank and provides feedback.

3. Assign the next task:
   
   **Using Slash Command:**
   ```
   /project:task-prompt task-1.2
   ```

And the loop continues!

## Common Scenarios

### Scenario 1: Simple Web App (2 Agents)
- **Manager Agent**: Plans and coordinates
- **Implementation Agent**: Builds everything

### Scenario 2: Complex Project (4+ Agents)
- **Manager Agent**: Overall coordination
- **Frontend Agent**: UI/UX implementation
- **Backend Agent**: API and database
- **Testing Agent**: Writing and running tests

### Scenario 3: Adding a Specialist
Need to debug something complex? Add a Debug Agent:
```
# New Claude instance
/apm-init debug
/memory read Phase_1/Task_1.3_Log.md
# Analyzes and fixes issues
```

## Tips for Success

### 1. Keep Tabs Organized
```
Browser Setup:
┌─────────────┬─────────────┬─────────────┐
│  Manager    │   Impl A    │   Impl B    │
│   (Tab 1)   │   (Tab 2)   │   (Tab 3)   │
└─────────────┴─────────────┴─────────────┘
```

### 2. Sync Frequently
Before any major operation:
```
/apm-sync
```

### 3. Let Manager Coordinate
- Don't have Implementation Agents modify the Implementation Plan
- Always go through Manager for task assignments
- Keep clear boundaries between agents

### 4. Use the Status Command
Not sure where you are? Use:
```
/apm-status
```

### 5. Save Context Before Long Breaks
```
/apm-context save
```

## Workflow Examples

### Example 1: Starting a TODO App

**Manager Agent:**
```
User: /apm-init manager
User: /manager discover
User: I want to build a TODO app with React and Node.js
[Claude asks clarifying questions]
User: [Provides answers]
User: /manager plan
[Claude creates Implementation_Plan.md and Memory_Bank.md]
```

**First Implementation:**
```
Manager: /task-prompt task-1.1
[Copy the output]

# New tab
Implementation: /apm-init implement
Implementation: /load-task clipboard
Implementation: /implement start
[Claude sets up project structure]
Implementation: /implement complete
```

### Example 2: Parallel Development

Once you're comfortable, run multiple Implementation Agents:

```
Manager: /task-prompt task-2.1  # Frontend task
Manager: /task-prompt task-2.2  # Backend task

# Implementation Agent A gets task-2.1
# Implementation Agent B gets task-2.2
# Both work simultaneously!
```

## Troubleshooting

### "I don't know what role I am"
```
/apm-status
```
If that doesn't work:
```
/apm-init [role]
```

### "Memory Bank seems out of date"
```
/apm-sync
/memory validate
```

### "Context limit approaching"
**For Manager:**
```
/manager handover
```
Then start a new Manager instance with the handover files.

**For Implementation:**
```
/implement complete
/apm-context save
```
Then start fresh Implementation Agent if needed.

### "Tasks seem confused or overlapping"
1. In Manager: `/apm-sync`
2. Check Implementation Plan: `/memory read Implementation_Plan.md`
3. Ensure each task has clear boundaries
4. Re-assign if necessary

### "I closed a tab by accident"
No problem! Open new Claude Code instance:
1. `/apm-init [previous role]`
2. `/apm-sync`
3. `/apm-status` to see where you left off

## Quick Reference Card

### Manager Commands (Slash Command → Traditional)
- `/project:apm-init-manager` → `/apm-init manager`
- `/project:manager-discover` → `/manager discover`
- `/project:manager-plan` → `/manager plan`
- `/project:task-prompt` → `/task-prompt <id>`
- `/project:manager-review` → `/manager review`
- `/project:manager-handover` → `/manager handover`

### Implementation Commands (Slash Command → Traditional)
- `/project:apm-init-implement` → `/apm-init implement`
- `/project:load-task-clipboard` → `/load-task clipboard`
- `/project:implement-start` → `/implement start`
- `/project:implement-status` → `/implement status`
- `/project:implement-complete` → `/implement complete`

### Universal Commands (Slash Command → Traditional)
- `/project:apm-sync` → `/apm-sync`
- `/project:apm-status` → `/apm-status`
- `/project:memory-read` → `/memory read`
- `/project:apm-context-save` → `/apm-context save`

**Pro Tip**: Start typing `/project:` in Claude Code to see all available commands with auto-complete!

## Next Steps

1. **Start Small**: Try a simple project first
2. **Practice the Loop**: Get comfortable with the workflow
3. **Add Complexity**: Gradually add more agents
4. **Customize**: Adapt the workflow to your needs

Remember: APM is a framework, not rigid rules. Adjust it to work best for your projects!

## Getting Help

- **APM Issues**: Check the [APM GitHub](https://github.com/sdi2200262/agentic-project-management)
- **Claude Code Issues**: Visit [claude.ai/help](https://claude.ai/help)
- **Command Reference**: See the main `CLAUDE.md` file

Happy building with APM and Claude Code! 🚀