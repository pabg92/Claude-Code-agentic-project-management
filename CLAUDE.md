# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This workspace contains the Agentic Project Management (APM) framework - a Claude Code-enhanced system for managing complex projects using multiple AI agents. APM implements a multi-agent architecture where specialized Claude Code instances collaborate through structured workflows and a shared Memory Bank.

## Architecture

### Multi-Agent System
```
User (Project Owner)
    ↕
Manager Agent (Claude Code Instance 1)
    ↕
Implementation Agents (Claude Code Instances 2, 3, 4...)
    ↕
Memory Bank (Shared Project Files)
```

## Key Commands

### Common Development Tasks

Since APM is a methodology framework rather than a software application, there are no traditional build/test/lint commands. Instead, the development workflow uses APM-specific slash commands:

#### Initialize Agent Roles
```bash
/apm-init manager      # Initialize as Manager Agent
/apm-init implement    # Initialize as Implementation Agent
/apm-init debug        # Initialize as Debug Specialist
```

#### Manager Operations
```bash
/manager discover      # Run project discovery phase
/manager plan         # Create/update Implementation Plan
/task-prompt <id>     # Generate task assignment for Implementation Agent
/manager review       # Review completed work
```

#### Implementation Operations
```bash
/load-task clipboard  # Load task assignment from clipboard
/implement start      # Begin work on assigned task
/implement complete   # Mark task complete and log to Memory Bank
```

#### Memory Bank Operations
```bash
/memory read          # Display relevant Memory Bank entries
/memory log          # Add new entry following APM format
/memory validate     # Check Memory Bank structure
/apm-sync           # Synchronize with latest project state
```

## High-Level Architecture

### Core Components

1. **Manager Agent**: The project coordinator that creates implementation plans, assigns tasks, and reviews work. Always operates in Instance 1.

2. **Implementation Agents**: Specialized workers that execute assigned tasks. Each operates in a separate Claude Code instance.

3. **Memory Bank**: A structured file system that serves as the single source of truth for all agents:
   - `Implementation_Plan.md`: Master planning document
   - `Memory_Bank.md` or `Memory/` directory: Project activity logs
   - Structured logs for each task and phase

4. **Handover Protocols**: Mechanisms for managing context limits by transferring state between agent instances.

### Key Workflows

1. **Project Initialization**: Manager discovers requirements → creates Implementation Plan → sets up Memory Bank
2. **Task Assignment**: Manager generates task prompt → Implementation Agent loads task → executes work
3. **Review Cycle**: Implementation logs work → Manager reviews → provides feedback → updates plan
4. **Context Management**: Agents track usage → prepare handover artifacts → new instance continues work

### Important Design Principles

- **Role Separation**: Each agent has specific responsibilities and commands
- **Memory Bank as Truth**: All significant actions are logged to persistent files
- **Structured Communication**: Agents communicate through formatted prompts and logs
- **Context Awareness**: Built-in mechanisms for handling Claude's context limits

## APM Framework Structure

### Prompt Templates (`/prompts/`)
- Initial setup prompts for Manager Agent
- Core operational guides for all agent types
- Utility prompts and format definitions

### Documentation (`/docs/`)
- Workflow overview and getting started guides
- Core concepts and architecture details
- Cursor IDE integration guide
- Troubleshooting resources

### Cursor Rules (`/rules/`)
- Optional enhancements for Cursor IDE users
- Memory validation and format enforcement
- Implementation plan consistency checks
- Task assignment guidance

## Best Practices

1. **Always initialize agent role** when starting a new Claude Code instance
2. **Sync regularly** with `/apm-sync` to maintain awareness of project state
3. **Let Manager coordinate** - avoid direct implementation plan changes
4. **Log everything significant** to Memory Bank for team visibility
5. **Validate structure** before major operations with `/memory validate`
6. **Prepare handovers proactively** when approaching context limits