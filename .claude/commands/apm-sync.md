# APM Full Project Synchronization

Perform a comprehensive synchronization with the project state. This ensures your agent has the latest information from all project artifacts.

## Synchronization Process

### 1. Read Core Documents

Load and analyze key project files:

#### Implementation Plan
- Read `Implementation_Plan.md`
- Note current phase
- Identify task statuses
- Check agent assignments

#### Memory Bank
- Read recent entries
- Check for updates since last sync
- Note completed work
- Identify new decisions

#### Configuration
- Check `.apm/config.json` if exists
- Review agent configurations
- Note project settings

### 2. Analyze Project State

Based on documents read:

```markdown
## Project State Analysis

### Current Status
- Active Phase: [Identify from plan]
- Completed Tasks: [Count]
- In Progress: [Count]
- Pending: [Count]

### Recent Changes
- [Change 1]: [What changed and when]
- [Change 2]: [What changed and when]
- [Decision]: [New decisions made]

### Active Agents
- [Agent Type]: Working on [Task]
- [Agent Type]: Status [Status]
```

### 3. Update Internal State

Refresh your understanding:
- Current project phase
- Your assigned tasks
- Dependencies and blockers
- Recent decisions
- Team activity

### 4. Identify Gaps

Check for missing information:
- [ ] Uncommitted Memory Bank entries
- [ ] Outdated task statuses
- [ ] Missing review feedback
- [ ] Untracked decisions

### 5. Sync Actions by Role

#### Manager Agent Sync:
1. Review all phase progress
2. Check pending reviews
3. Identify idle agents
4. Note blocked tasks
5. Plan next assignments

#### Implementation Agent Sync:
1. Check task updates
2. Review dependencies
3. Note related work
4. Identify blockers
5. Update task status

#### Specialized Agent Sync:
1. Review relevant tasks
2. Check for issues
3. Note areas needing attention
4. Plan interventions

### 6. Memory Bank Reconciliation

Ensure Memory Bank is current:
```markdown
## Memory Bank Status
- Last Entry: [Timestamp]
- Entries Since Last Sync: [Count]
- New Phases: [Any new phases]
- New Reviews: [Recent reviews]
```

### 7. Dependency Check

Validate task dependencies:
```markdown
## Dependency Analysis
- Completed Dependencies: [List]
- Pending Dependencies: [List]
- Newly Unblocked: [Tasks now ready]
- Still Blocked: [Tasks waiting]
```

### 8. Generate Sync Report

Create a comprehensive sync summary:

```markdown
# APM Synchronization Report

## Sync Metadata
- **Date**: [Current timestamp]
- **Agent**: [Your type and ID]
- **Last Sync**: [Previous sync time]

## Project State
- **Phase**: [Current] of [Total]
- **Progress**: [Overall percentage]
- **Health**: [Status indicator]

## Changes Since Last Sync
### Completed Tasks
- [Task ID]: [Name] by [Agent]

### New Activities
- [Activity type]: [Description]

### Updated Entries
- [Entry]: [What changed]

## Current Understanding
### My Role
- [Your current responsibilities]

### My Tasks
- [Current task status]
- [Upcoming tasks]

### Dependencies
- [What you're waiting for]
- [What's waiting on you]

## Action Items
Based on sync findings:
1. [Immediate action needed]
2. [Follow-up required]
3. [Planning needed]

## Sync Complete
✅ Implementation Plan: Loaded
✅ Memory Bank: Current
✅ Dependencies: Verified
✅ Role Context: Updated
```

### 9. Post-Sync Actions

After synchronization:
1. Update any stale information
2. Adjust plans based on findings
3. Communicate sync results
4. Address any issues found
5. Resume work with fresh context

### 10. Sync Best Practices

- Sync at session start
- Sync before major decisions
- Sync after extended breaks
- Sync when confused
- Sync before handovers

Perform full project synchronization and update your understanding of the current state.