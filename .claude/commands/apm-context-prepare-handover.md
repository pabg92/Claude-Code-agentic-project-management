# Prepare Context for Handover

Create a comprehensive handover package combining saved context with handover documentation. This ensures smooth transition to a new agent instance when context limits are reached or role changes are needed.

## Handover Preparation Process

### 1. Assess Current Situation

Determine handover needs:
- **Reason**: Context limit | Role change | Task completion | Shift change
- **Urgency**: Immediate | Planned | Precautionary
- **Target**: Same role new instance | Different role | Any available agent

### 2. Save Current Context

First, save your current state:
```bash
# This creates the context snapshot
/apm-context save
```

### 3. Create Handover Package

Combine context with handover documentation:

```markdown
# Agent Handover Package
Date: [Current timestamp]
From: [Your agent type and ID]
To: [Target agent type]
Reason: [Why handover needed]

## Quick Start for New Agent
1. Initialize as [Role]: `/apm-init [role]`
2. Load this handover: `/apm-context load`
3. Review critical items below
4. Continue with [Specific next action]

## Critical Information

### Immediate Attention Required
🚨 **URGENT**: [Any urgent items]
⚠️ **Important**: [Important but not urgent]
ℹ️ **Note**: [Good to know]

### Current Task Status
- **Task ID**: [Current task]
- **Progress**: [Percentage] complete
- **Next Step**: [Specific action needed]
- **Blockers**: [Any blockers]

### Recent User Directives
Must know from recent conversation:
- [Directive 1]: User wants [specific requirement]
- [Directive 2]: Changed approach to [what]
- [Directive 3]: Priority is now [what]

## Work in Progress

### Active Development
```[language]
// Code being worked on
// Include current state
// Note any issues
```

### Uncommitted Changes
Files modified but not committed:
- [File 1]: [What was changed]
- [File 2]: [What was changed]

### Partial Implementations
- [Feature 1]: [Status and next steps]
- [Feature 2]: [Status and next steps]

## Context Summary

### Project Understanding
Key insights about this project:
- Architecture: [Key points]
- Patterns: [Important patterns]
- Preferences: [User/project preferences]
- Constraints: [Important limitations]

### Technical Decisions
Recent decisions and rationale:
1. [Decision]: [Why made]
2. [Decision]: [Why made]

### Relationships
- Dependencies: [What this depends on]
- Dependents: [What depends on this]
- Related work: [Connected tasks]

## Memory Bank Status
- Last update: [When]
- Location: [Path to current logs]
- Pending logs: [What needs to be logged]

## Handover Checklist
Before taking over, ensure:
- [ ] Read this complete handover
- [ ] Load referenced context
- [ ] Check Memory Bank entries
- [ ] Understand current task
- [ ] Know next steps
- [ ] Aware of blockers
- [ ] Understand urgencies

## Environment State
- Working directory: [Path]
- Key files: [List important files]
- Tools in use: [Any special tools]
- Configurations: [Important settings]

## Continuation Guide

### If Manager Agent:
1. Check all agent statuses
2. Review pending reviews
3. Plan next assignments
4. Address any blockers

### If Implementation Agent:
1. Continue current task
2. Check dependencies
3. Update Memory Bank
4. Complete implementation

### If Specialized Agent:
1. Focus on specific issue
2. Apply expertise
3. Document findings
4. Coordinate with others

## Recovery Commands
```bash
# Initialize role
/apm-init [role]

# Load this handover
/apm-context load [path]

# Sync with project
/apm-sync

# Check status
/apm-status

# Continue work
/[role-specific command]
```

## Contact & Escalation
If issues arise:
1. Check Memory Bank for patterns
2. Review Implementation Plan
3. Consult previous handovers
4. Ask user for clarification

## Final Notes from Outgoing Agent
[Any personal observations, tips, or warnings that might help]

---
Handover prepared by: [Agent ID]
Ready for transition: ✅
```

### 4. Create Handover Index

Update handover registry:
```markdown
# Handover Registry

## Recent Handovers
| Date | From | To | Reason | Status |
|------|------|----|--------|---------|
| [Date] | [Agent] | [Agent] | [Reason] | [Active/Complete] |
```

### 5. Package All Materials

Create complete handover package:
```
Handover/
├── [timestamp]_handover/
│   ├── README.md           # Handover document
│   ├── context.md          # Full context
│   ├── current_task.md     # Task details
│   ├── memory_recent.md    # Recent logs
│   └── quick_start.md      # Quick reference
```

### 6. Validate Handover

Check completeness:
- [ ] All current work documented
- [ ] User directives captured
- [ ] Decisions explained
- [ ] Next steps clear
- [ ] No missing context
- [ ] Recovery steps included

### 7. Notify Handover Ready

Inform about handover:
```markdown
## Handover Ready

✅ Handover package complete
📁 Location: Handover/[timestamp]_handover/
📋 Includes: Context, tasks, decisions, guide
🎯 Target: [Intended recipient]
⏱️ Prepared: [Timestamp]

### Handover Instructions
1. New agent should initialize with correct role
2. Load handover with: `/apm-context load [path]`
3. Review README.md first
4. Follow quick start guide
5. Continue work seamlessly

### Reason for Handover
[Explain why handover is needed]

Ready for smooth transition.
```

### 8. Best Practices

#### Include Everything:
- Current understanding
- Work in progress
- Recent conversations
- Decisions made
- Next steps

#### Make It Actionable:
- Clear next steps
- Specific commands
- Exact file paths
- Concrete examples

#### Anticipate Questions:
- Why decisions were made
- Where to find things
- How to handle issues
- Who to contact

Prepare a comprehensive handover package for seamless agent transition.