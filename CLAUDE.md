# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

APM (Agentic Project Management) is a framework for managing complex projects using AI assistants. This enhanced version is specifically optimized for Claude Code, leveraging its unique features like slash commands, file management, and context handling while maintaining the powerful multi-agent architecture.

**Key Enhancement:** This version enhances APM's multi-agent workflow with Claude Code-specific commands and features, enabling seamless coordination between multiple Claude Code instances acting as specialized agents.

## Architecture

### APM Multi-Agent System (Preserved & Enhanced)
```
User (Project Owner)
    ↕
Manager Agent (Claude Code Instance 1)
    ↕
Implementation Agents (Claude Code Instances 2, 3, 4...)
    ↕
Memory Bank (Shared Project Files)
```

Each Claude Code instance operates as a dedicated agent with specific roles and responsibilities, coordinated through the Memory Bank and APM protocols.

## Claude Code Slash Commands for APM

### Agent Initialization Commands

#### `/apm-init [role]` - Initialize Agent Role
Initializes a Claude Code instance with a specific APM role.
- **Usage**: `/apm-init [manager|implement|review|debug|test]`
- **Examples**:
  - `/apm-init manager` - Initialize as Manager Agent
  - `/apm-init implement` - Initialize as Implementation Agent
  - `/apm-init review` - Initialize as Review Specialist

### Manager Agent Commands

#### `/manager` - Manager Operations
Available only when initialized as Manager Agent.
- **Usage**: `/manager [discover|plan|assign|review|handover]`
- **Sub-commands**:
  - `discover` - Run project discovery phase
  - `plan` - Create/update Implementation Plan
  - `assign` - Generate task assignment for Implementation Agent
  - `review` - Review Implementation Agent work
  - `handover` - Prepare Manager handover artifacts

#### `/task-prompt` - Generate Task Assignment
Creates a formatted task assignment prompt for Implementation Agents.
- **Usage**: `/task-prompt <task-id>`
- **Example**: `/task-prompt task-2.1`
- Outputs ready-to-copy prompt for new Implementation Agent

### Implementation Agent Commands

#### `/implement` - Implementation Operations
Available only when initialized as Implementation Agent.
- **Usage**: `/implement [start|status|complete]`
- **Sub-commands**:
  - `start` - Begin work on assigned task
  - `status` - Report current progress
  - `complete` - Mark task complete and generate Memory Bank entry

#### `/load-task` - Load Task Assignment
Loads task details from clipboard or file.
- **Usage**: `/load-task [clipboard|file:<path>]`
- Parses Manager's task assignment prompt

### Memory Bank Commands (All Agents)

#### `/memory` - Memory Bank Operations
Manages the project's Memory Bank system.
- **Usage**: `/memory [read|log|validate|sync]`
- **Sub-commands**:
  - `read` - Display relevant Memory Bank entries
  - `log` - Add new entry (follows APM format)
  - `validate` - Check Memory Bank structure
  - `sync` - Ensure Memory Bank consistency

### Cross-Agent Commands

#### `/apm-status` - Project Status
Shows project status from current agent's perspective.
- Manager sees: Overall progress, agent assignments, pending reviews
- Implementation sees: Current task, dependencies, blockers
- All see: Recent Memory Bank activity

#### `/apm-context` - Context Management
Manages context for long-running operations.
- **Usage**: `/apm-context [save|load|prepare-handover]`
- Creates context artifacts in `.apm/context/`

#### `/apm-sync` - Synchronize with Project
Refreshes understanding of project state.
- Reads latest Implementation Plan
- Checks recent Memory Bank entries
- Updates internal state

## Key Workflows (Multi-Agent Claude Code)

### 1. Project Initialization (Manager Agent)
```bash
# In Claude Code Instance 1
/apm-init manager
/manager discover

# Claude guides through project discovery
# Then creates Implementation Plan and Memory Bank
/manager plan
```

### 2. Task Assignment Flow
```bash
# Manager Agent (Instance 1)
/task-prompt task-1.1
# Generates formatted prompt with task details

# Copy prompt to new Claude Code Instance 2
# Implementation Agent (Instance 2)
/apm-init implement
/load-task clipboard
/implement start
# ... performs work ...
/implement complete
```

### 3. Review Cycle
```bash
# Manager Agent (Instance 1)
/apm-sync
/manager review
# Reviews Memory Bank entries
# Provides feedback via new task assignments
```

### 4. Specialized Agent Integration
```bash
# Debug Agent (Instance 3)
/apm-init debug
/memory read Phase_1/Task_1.2_Log.md
# Analyzes specific implementation
# Logs findings to Memory Bank
```

## Important Implementation Details

### 1. Multi-Instance Coordination
- Each Claude Code instance maintains its agent role
- Memory Bank serves as single source of truth
- Implementation Plan defines task ownership
- Regular `/apm-sync` keeps agents aligned

### 2. Memory Bank as Communication Hub
- All significant actions logged to Memory Bank
- Standardized format ensures readability across agents
- File-based persistence enables true async work
- Validation prevents structure drift

### 3. Context Window Management
- Each agent tracks its own context usage
- Handover protocols for agent replacement
- Memory Bank provides persistent context
- Context artifacts in `.apm/context/` for recovery

### 4. Enhanced Features for Claude Code
- **File Validation**: Auto-check against Implementation Plan
- **Smart Prompts**: Commands generate APM-compliant outputs
- **Progress Tracking**: Visual indicators per agent role
- **Error Recovery**: Graceful handling of sync issues

## Directory Structure (Multi-Agent Enhanced)

```
project/
├── .apm/                           # APM configuration
│   ├── config.json                 # Project settings
│   ├── agents/                     # Agent tracking
│   │   ├── manager.json           # Manager state
│   │   ├── impl_1.json            # Implementation Agent 1 state
│   │   └── impl_2.json            # Implementation Agent 2 state
│   ├── context/                    # Saved contexts per agent
│   │   ├── manager/               
│   │   └── implementations/       
│   └── templates/                  # Custom prompt templates
├── Implementation_Plan.md          # Master planning document
├── Memory_Bank.md                  # Single-file memory (simple)
├── Memory/                         # Multi-file memory (complex)
│   ├── README.md                   # Memory Bank overview
│   ├── Phase_1/                    # Phase-specific logs
│   │   ├── Task_1.1_Log.md        # Agent A's work
│   │   └── Task_1.2_Log.md        # Agent B's work
│   └── Reviews/                    # Manager review logs
└── Handover/                       # Agent handover artifacts
    ├── Manager/                    # Manager handovers
    └── Implementations/            # Implementation handovers
```

## Claude Code Specific Optimizations

### 1. Agent Awareness
- Each instance knows its role via `/apm-init`
- Commands adapt based on agent type
- Role-specific prompts and validations
- Clear indication of current agent role

### 2. Efficient Task Distribution
- Manager generates Claude-ready task prompts
- Implementation Agents parse assignments cleanly
- Automatic task ID tracking
- Dependencies clearly communicated

### 3. Synchronized Logging
- Timestamps include agent identifier
- Automatic format compliance
- Conflict detection for simultaneous edits
- Merge assistance for Memory Bank updates

### 4. Handover Automation
- Role-specific handover templates
- Context compression per agent type
- Automatic state preservation
- Clear handover instructions

## Usage Examples

### Starting a New Project (Manager)
```
User: /apm-init manager
Claude: Initialized as Manager Agent for APM project. Ready to begin project discovery.

User: /manager discover
Claude: Let me guide you through APM project discovery...
[Continues with structured discovery per APM protocols]
```

### Receiving Task Assignment (Implementation)
```
User: /apm-init implement
Claude: Initialized as Implementation Agent. Please provide task assignment.

User: [Pastes task prompt from Manager]
Claude: /load-task clipboard
Task loaded: Task 2.1 - Create User Model
Reading Implementation Plan context...
Ready to begin implementation.

User: /implement start
Claude: Starting Task 2.1 implementation...
[Executes task following APM protocols]
```

### Reviewing Work (Manager)
```
User: /apm-sync
Claude: Synchronizing with project state...
- Found 3 new Memory Bank entries
- 2 tasks completed since last sync
- 1 task in progress

User: /manager review
Claude: Reviewing completed work for Phase 1...
[Reviews against Implementation Plan criteria]
```

## Best Practices

1. **Always initialize agent role** with `/apm-init` when starting new instance
2. **Sync regularly** with `/apm-sync` to maintain awareness
3. **Let Manager coordinate** - avoid direct implementation changes
4. **Log everything significant** to Memory Bank
5. **Validate Memory Bank** structure before major operations
6. **Prepare handovers proactively** when approaching context limits

## Inter-Agent Communication

### Manager → Implementation
- Task assignments via `/task-prompt`
- Feedback through Memory Bank reviews
- Plan updates affect all agents

### Implementation → Manager
- Work logs in Memory Bank
- Blocker reports in status updates
- Completion notifications

### Implementation ↔ Implementation
- Coordinate through Memory Bank
- Reference each other's work
- Maintain clear boundaries

## Version Notes

Current version: Claude Code APM v1.0.0

Key enhancements over standard APM:
- Claude Code slash commands for each agent role
- Multi-instance coordination support
- Enhanced Memory Bank validation
- Automated handover generation
- Role-aware context management

## Troubleshooting

### Common Issues

**Agent Role Confusion**
- Solution: `/apm-init [role]` to re-establish
- Check: Current role shown in `/apm-status`

**Memory Bank Conflicts**
- Solution: `/memory validate` to check structure
- Use: `/apm-sync` before making changes

**Context Limit Approaching**
- Manager: `/manager handover` to prepare artifacts
- Implementation: `/implement complete` then handover

**Lost Task Context**
- Implementation: `/memory read` relevant logs
- Manager: Review Implementation Plan section

**Sync Issues**
- All agents: `/apm-sync` to refresh
- Check: `.apm/agents/` for state files