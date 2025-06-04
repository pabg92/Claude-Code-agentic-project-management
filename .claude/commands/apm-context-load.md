# Load Saved Context

Restore a previously saved context to continue work or recover from an interruption. This loads a context snapshot and helps you resume where you or another agent left off.

## Context Load Process

### 1. Locate Context File

Find available context files:
```
.apm/context/
├── manager/
│   ├── 20250106_143000_context.md
│   └── 20250106_090000_context.md
├── implementations/
│   ├── agent_a/
│   │   └── 20250106_110000_context.md
│   └── agent_b/
│       └── 20250105_160000_context.md
└── specialized/
    └── debug/
        └── 20250106_120000_context.md
```

### 2. Read Context Document

Load and parse the context file containing:
- Agent role and state
- Active work status
- Recent decisions
- Pending items
- Environment state

### 3. Restore Understanding

From the context file, restore:

#### Role Understanding
- What type of agent you are
- Your responsibilities
- Current focus area

#### Work State
- Active task details
- Progress made
- Work remaining
- Any work in progress code

#### Project Context
- Recent decisions
- User communications
- Technical understanding
- Patterns identified

#### Pending Items
- Next steps planned
- Waiting dependencies
- Questions to address

### 4. Verify Related Resources

Check referenced documents:
```markdown
## Resource Verification
- [ ] Implementation Plan accessible
- [ ] Memory Bank entries readable
- [ ] Referenced files exist
- [ ] Dependencies available
```

### 5. Synchronize Current State

After loading context:
1. Check for updates since context was saved
2. Read recent Memory Bank entries
3. Verify task status hasn't changed
4. Look for new communications

### 6. Context Integration

Merge loaded context with current state:

```markdown
## Context Integration Report

### Loaded Context
- **From**: [Timestamp]
- **Agent**: [Type saved by]
- **Age**: [How old]

### Updates Since Save
- [New Memory Bank entries]
- [Task status changes]
- [New decisions]

### Current Understanding
Combining loaded context with updates:
- **Role**: [Confirmed role]
- **Task**: [Current status]
- **Next Steps**: [Updated plan]

### Conflicts/Changes
- [Any conflicts found]
- [Resolution approach]
```

### 7. Resume Work

Based on loaded context:

#### Continue Current Task
If task was in progress:
1. Review work completed
2. Check partial implementations
3. Verify approach still valid
4. Resume from stopping point

#### Address Pending Items
If items were waiting:
1. Check if still blocked
2. See if dependencies met
3. Address questions
4. Proceed with next steps

#### Apply Understanding
Use restored knowledge:
- Project patterns
- Technical decisions
- User preferences
- Architecture understanding

### 8. Load Confirmation

Confirm successful context restoration:

```markdown
# Context Load Complete

## Load Summary
✅ Context file loaded: [Path]
✅ Role restored: [Agent type]
✅ Task context: [Task ID] - [Status]
✅ Memory synchronized: [Last entry checked]

## Restored State
### Current Work
- Working on: [Task description]
- Progress: [Percentage]
- Next action: [Immediate step]

### Key Context
- [Important decision 1]
- [Important pattern 2]
- [Critical understanding 3]

## Ready to Continue
Based on loaded context:
1. [First action to take]
2. [Second action planned]
3. [Third step prepared]

Type '/implement status' to see current task details
Or continue with restored work...
```

### 9. Error Handling

If context load fails:

#### File Not Found
- List available contexts
- Suggest recent files
- Offer to start fresh

#### Corrupted Context
- Load partial information
- Highlight missing sections
- Suggest manual recovery

#### Outdated Context
- Show age warning
- Recommend full sync
- List major changes

### 10. Best Practices

#### Loading Context:
- Load most recent relevant context
- Verify age before loading
- Check for multiple contexts
- Sync after loading
- Validate understanding

#### After Loading:
- Confirm role matches
- Verify task still valid
- Check for conflicts
- Update stale information
- Continue smoothly

Load the specified context file or the most recent context for your role.