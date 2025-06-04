# APM Claude Code Commands

This directory contains project-specific slash commands for the Agentic Project Management (APM) framework. These commands enable efficient multi-agent coordination in Claude Code.

## Usage

In Claude Code, use these commands with the `/project:` prefix:

```
/project:apm-init-manager
/project:task-prompt task-2.1
/project:memory-read Phase_1/Task_1.1_Log.md
```

## Available Commands

### Agent Initialization
- `/project:apm-init-manager` - Initialize as Manager Agent
- `/project:apm-init-implement` - Initialize as Implementation Agent
- `/project:apm-init-debug` - Initialize as Debug Agent
- `/project:apm-init-review` - Initialize as Review Agent
- `/project:apm-init-test` - Initialize as Test Agent

### Manager Operations
- `/project:manager-discover` - Run project discovery
- `/project:manager-plan` - Create/update Implementation Plan
- `/project:manager-review` - Review completed work
- `/project:manager-handover` - Prepare Manager handover
- `/project:task-prompt <task-id>` - Generate task assignment

### Implementation Operations
- `/project:implement-start` - Begin assigned task
- `/project:implement-status` - Report progress
- `/project:implement-complete` - Complete task & log
- `/project:load-task-clipboard` - Load task from clipboard
- `/project:load-task-file <path>` - Load task from file

### Memory Bank Operations
- `/project:memory-read [path]` - Read Memory Bank entries
- `/project:memory-log` - Add new entry
- `/project:memory-validate` - Validate structure
- `/project:memory-sync` - Synchronize Memory Bank

### Cross-Agent Commands
- `/project:apm-status` - Show project status
- `/project:apm-sync` - Sync with project
- `/project:apm-context-save` - Save context
- `/project:apm-context-load` - Load context
- `/project:apm-context-prepare-handover` - Prepare handover

## Command Arguments

Some commands accept arguments using `$ARGUMENTS`:
- `task-prompt` - Requires task ID (e.g., `task-2.1`)
- `load-task-file` - Requires file path
- `memory-read` - Optional path to specific entry

## Quick Start Example

### Manager Agent (Instance 1)
```bash
/project:apm-init-manager
/project:manager-discover
# Answer questions about your project
/project:manager-plan
/project:task-prompt task-1.1
```

### Implementation Agent (Instance 2)
```bash
/project:apm-init-implement
/project:load-task-clipboard
/project:implement-start
# Do the work
/project:implement-complete
```

## Best Practices

1. Always initialize your agent role first
2. Use `/project:apm-sync` frequently to stay updated
3. Let the Manager coordinate all planning
4. Log all significant work to Memory Bank
5. Prepare handovers before hitting context limits

## See Also

- [CLAUDE.md](../../CLAUDE.md) - Complete command reference
- [claude-guide.md](../../Claude-Code-agentic-project-management/claude-guide.md) - Beginner's guide
- [APM Documentation](../../Claude-Code-agentic-project-management/docs/) - Full framework docs