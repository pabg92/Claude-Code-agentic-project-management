# Manager Agent - Prepare Handover Documentation

As a Manager Agent, you will now prepare comprehensive handover documentation. This ensures seamless continuity when transitioning to a new Manager Agent instance.

## Handover Preparation Process

### 1. Current State Assessment
Document the current project status:
- **Completed Phases**: What's been accomplished
- **Active Tasks**: Currently in progress
- **Pending Tasks**: Not yet started
- **Blocked Items**: Issues requiring attention

### 2. Create Handover Artifact

Create a structured handover document in `Handover/Manager/[timestamp]_Manager_Handover.md`:

```markdown
# Manager Agent Handover Document
Date: [Current Date]
Outgoing Agent: Manager Agent [Instance ID]

## Project Overview
[Brief project description and current status]

## Completed Work Summary
### Phase 1: [Name]
- ✅ Task 1.1: [Summary]
- ✅ Task 1.2: [Summary]

### Phase 2: [Name] 
- 🔄 Task 2.1: [In Progress - Status]
- ⏸️ Task 2.2: [Blocked - Reason]

## Active Implementation Agents
- Agent A: Working on [Task ID] - [Status]
- Agent B: Working on [Task ID] - [Status]

## Critical Decisions Made
1. [Decision]: [Rationale]
2. [Decision]: [Rationale]

## Recent User Directives
- [Date]: [User request/clarification]
- [Date]: [Change in requirements]

## Pending Reviews
- Task [ID]: Completed by [Agent], awaiting review
- Task [ID]: Revision requested, awaiting update

## Known Issues & Risks
1. [Issue]: [Impact and mitigation strategy]
2. [Risk]: [Probability and contingency plan]

## Recommended Next Actions
1. [Immediate]: [What needs attention first]
2. [Short-term]: [Next 2-3 tasks]
3. [Planning]: [Upcoming phase preparation]

## Key Files & Locations
- Implementation Plan: `Implementation_Plan.md`
- Memory Bank: `Memory/` directory
- Recent Reviews: `Memory/Reviews/`
- Project Config: `.apm/config.json`

## Context Not in Memory Bank
[Any important context from recent conversations not yet logged]

## Handover Checklist
- [ ] All recent work logged to Memory Bank
- [ ] Implementation Plan updated
- [ ] Active tasks documented
- [ ] User communications captured
- [ ] Critical decisions recorded
```

### 3. Update Memory Bank
Ensure all recent activities are logged:
- Complete any pending Memory Bank entries
- Document recent decisions
- Log any verbal agreements or clarifications

### 4. Prepare Transition Instructions

Create clear instructions for the incoming Manager:
```markdown
## Onboarding Steps for New Manager
1. Read this handover document completely
2. Review Implementation_Plan.md
3. Check Memory Bank for recent entries
4. Use /apm-sync to refresh state
5. Review pending tasks and assignments
6. Check for any blocked items needing attention
```

### 5. Critical Information Highlights
Emphasize:
- **Urgent Items**: What needs immediate attention
- **Dependencies**: Critical path items
- **Stakeholder Context**: Recent user feedback
- **Technical Debt**: Known issues to address
- **Success Patterns**: What's working well

### 6. Archive Current State
- Save all relevant conversation context
- Export any temporary notes
- Document any informal agreements
- Capture lessons learned

## Handover Best Practices
- Be thorough but concise
- Focus on actionable information
- Include context for decisions
- Highlight risks and blockers
- Provide clear next steps
- Don't assume knowledge

## Final Steps
1. Save handover document
2. Update Memory Bank with handover entry
3. Notify user of handover readiness
4. Provide handover location to user
5. Offer to answer clarifying questions

Begin preparing your handover documentation by assessing the current project state.