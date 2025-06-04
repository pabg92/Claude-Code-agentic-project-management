# APM Project Status

Display comprehensive project status from your current agent's perspective. This provides a real-time view of project progress, active work, and pending items.

## Status Report Components

### 1. Agent Context
First, identify your current role:
- **Current Agent**: [Manager|Implementation|Debug|Review|Test]
- **Agent ID**: [Your identifier]
- **Session Start**: [When initialized]

### 2. Project Overview
Display high-level project information:

```markdown
## Project Status Overview
- **Project**: [Name from Implementation Plan]
- **Current Phase**: Phase [X] of [Y]
- **Overall Progress**: [X]% complete
- **Health Status**: 🟢 On Track | 🟡 At Risk | 🔴 Blocked
```

### 3. Phase Status
For each phase:

```markdown
### Phase 1: [Name] - [Status]
Progress: ████████░░ 80% (4/5 tasks)
- ✅ Task 1.1: [Name] - Complete
- ✅ Task 1.2: [Name] - Complete  
- ✅ Task 1.3: [Name] - Complete
- 🔄 Task 1.4: [Name] - In Progress (Agent B)
- ⏳ Task 1.5: [Name] - Pending

### Phase 2: [Name] - [Status]
Progress: ██░░░░░░░░ 20% (1/5 tasks)
- ✅ Task 2.1: [Name] - Complete
- 🔄 Task 2.2: [Name] - In Progress (Agent C)
- ⏳ Task 2.3: [Name] - Pending
- ⏳ Task 2.4: [Name] - Blocked by Task 2.2
- ⏳ Task 2.5: [Name] - Pending
```

### 4. Active Work (Agent-Specific Views)

#### For Manager Agent:
```markdown
## Active Assignments
- Agent A: Task 1.4 - Database Schema (75% complete)
- Agent B: Task 2.2 - API Endpoints (Started today)
- Agent C: Idle - Awaiting task assignment

## Pending Reviews  
- Task 1.3: Submitted by Agent A (2 hours ago)
- Task 2.1: Submitted by Agent B (Yesterday)

## Recent Decisions
- Chose PostgreSQL over MySQL for database
- Approved REST API over GraphQL
```

#### For Implementation Agent:
```markdown
## My Current Task
- Task ID: 2.2
- Name: Implement User API Endpoints
- Status: In Progress (40% complete)
- Started: 2 days ago
- Blockers: None

## Dependencies
- Waiting for: None
- Blocking: Task 2.4, Task 2.5
```

### 5. Memory Bank Activity

Recent Memory Bank updates:
```markdown
## Recent Memory Bank Activity
- [2 hours ago] Task_1.4_Log.md updated by Agent A
- [4 hours ago] Phase_1_Review.md created by Manager
- [Yesterday] Task_2.1_Log.md completed by Agent B
- [2 days ago] Project_Decisions.md updated
```

### 6. Blockers & Issues

Current impediments:
```markdown
## Current Blockers
1. **Task 2.4**: Waiting on Task 2.2 completion
   - Impact: Delays Phase 2 by ~2 days
   - Owner: Agent B
   
2. **Technical Issue**: Database connection timeout
   - Severity: Medium
   - Status: Under investigation
   - Owner: Debug Agent
```

### 7. Upcoming Work

Next priorities:
```markdown
## Upcoming Priorities
1. Complete Task 1.4 (Today)
2. Review Task 1.3 (Today)
3. Start Task 1.5 (Tomorrow)
4. Plan Phase 3 (This week)
```

### 8. Resource Utilization

Agent workload:
```markdown
## Agent Utilization
- Manager: Active (Planning Phase 3)
- Agent A: 80% - Heavy workload
- Agent B: 60% - Normal workload  
- Agent C: 0% - Available
- Debug Agent: 40% - Investigating issues
```

### 9. Timeline Status

Schedule adherence:
```markdown
## Timeline Status
- Project Start: [Date] ✅
- Phase 1 Complete: [Target] vs [Actual] 🟡 2 days late
- Phase 2 Complete: [Target] 🟢 On track
- Project End: [Target] 🟢 On track
```

### 10. Quick Actions

Suggested next steps based on role:
```markdown
## Recommended Actions
1. [Role-specific action 1]
2. [Role-specific action 2]
3. [Role-specific action 3]
```

### 11. Status Summary

Concise summary for quick reference:
```markdown
## Summary
**Overall**: Project 45% complete, generally on track
**Active**: 2 tasks in progress, 3 agents working
**Blocked**: 1 task blocked, medium priority
**Next**: Complete Phase 1, accelerate Phase 2
**Attention**: Database timeout issue needs resolution
```

Generate the comprehensive project status report based on your current agent role and project state.