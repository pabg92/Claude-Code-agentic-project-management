# Save Current Context

Save your current working context to enable recovery or handover. This creates a snapshot of your current state, understanding, and work in progress.

## Context Save Process

### 1. Identify Context Components

Determine what needs to be saved:
- Current role and responsibilities
- Active tasks and their status
- Recent decisions and rationale
- Work in progress
- Important conversations
- Unlogged updates

### 2. Create Context Directory

Set up context storage:
```bash
.apm/context/
├── manager/
│   └── [timestamp]_context.md
├── implementations/
│   ├── agent_a/
│   │   └── [timestamp]_context.md
│   └── agent_b/
│       └── [timestamp]_context.md
└── specialized/
    └── [role]/
        └── [timestamp]_context.md
```

### 3. Context Document Structure

Create a comprehensive context file:

```markdown
# Agent Context Snapshot
Generated: [Current timestamp]
Agent: [Type] - [Identifier]

## Current State

### Role & Responsibilities
- **Primary Role**: [Your main function]
- **Current Focus**: [What you're working on]
- **Key Responsibilities**: [List main duties]

### Active Work
#### Current Task
- **Task ID**: [Identifier]
- **Status**: [Progress percentage]
- **Started**: [When begun]
- **Work Completed**: [What's done]
- **Work Remaining**: [What's left]

#### Work in Progress
```[language]
// Any code being developed
// Include partial implementations
```

### Recent Context

#### Decisions Made
1. **Decision**: [What was decided]
   - **Rationale**: [Why]
   - **Impact**: [Effects]
   - **Time**: [When]

2. **Decision**: [What was decided]
   - **Rationale**: [Why]
   - **Impact**: [Effects]

#### Problems Encountered
- **Issue**: [Description]
  - **Status**: [Resolved/Pending]
  - **Approach**: [How addressing it]

#### User Communications
Recent important exchanges:
- [Time]: User requested [what]
- [Time]: Clarified [what]
- [Time]: Approved [what]

### Understanding & Insights

#### Project Patterns
- [Pattern noticed]: [Description]
- [Convention used]: [Details]
- [Preference identified]: [What]

#### Technical Context
- **Architecture**: [Key understanding]
- **Constraints**: [Important limits]
- **Dependencies**: [Critical relationships]

### Pending Items

#### Immediate Next Steps
1. [Next action to take]
2. [Following action]
3. [Subsequent task]

#### Waiting For
- [Dependency]: From [source]
- [Clarification]: About [topic]

#### Questions/Concerns
- [Question needing answer]
- [Concern to address]

### Memory Bank Status
- **Last Update**: [When]
- **Uncommitted Changes**: [Any pending logs]
- **Next Log Plans**: [What to document]

### Environment State
- **Current Directory**: [Path]
- **Open Files**: [List if relevant]
- **Modified Files**: [Uncommitted changes]
- **Tool States**: [Any tool-specific context]

### Handover Notes
If context is for handover:
- **Critical Information**: [Must know]
- **Watch Out For**: [Potential issues]
- **Recommended Approach**: [Suggestions]

## Recovery Instructions
To restore this context:
1. Load this context file
2. Read referenced Memory Bank entries
3. Check Implementation Plan section [X]
4. Review recent changes in [locations]
5. Continue with [specific next action]
```

### 4. Include Conversation Context

Add recent conversation highlights:
```markdown
### Recent Conversation Context
Key points from current session:
- User emphasized [important point]
- Agreed to [decision]
- Changed approach for [what]
- Prioritized [task/feature]
```

### 5. Save Context File

Save to appropriate location:
- **Filename**: `[timestamp]_context.md`
- **Location**: `.apm/context/[role]/`
- **Format**: ISO timestamp (YYYYMMDD_HHMMSS)

### 6. Create Context Index

Update or create index file:
```markdown
# Context Index

## Recent Contexts
- [Timestamp]: [Brief description] - [Status]
- [Timestamp]: [Brief description] - [Status]

## Active Context
Current: [Timestamp] - [Description]
```

### 7. Verify Save

Confirm context saved properly:
```markdown
## Context Save Confirmation
✅ Context saved successfully
- Location: .apm/context/[role]/[timestamp]_context.md
- Size: [File size]
- Components: [What was included]
- Purpose: [Why saved]

Next steps:
- Continue working with saved checkpoint
- Or prepare for handover
- Or close session safely
```

### 8. Best Practices

#### When to Save Context:
- Before long operations
- At natural break points
- Before switching tasks
- When approaching context limit
- At end of work session

#### What to Include:
- Unfinished work
- Recent decisions
- Current understanding
- Next steps
- Any blockers

#### What to Exclude:
- Redundant information
- Already logged items
- Sensitive data
- Verbose code listings

Save your current context following the structure above.