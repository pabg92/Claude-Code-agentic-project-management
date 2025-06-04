# Log to Memory Bank

Create or update Memory Bank entries to document project progress, decisions, and important information. The Memory Bank serves as the single source of truth for all agents.

## Memory Bank Logging Process

### 1. Determine Log Type
Identify what type of entry you're creating:

#### Task Implementation Log
For ongoing task work:
- Location: `Memory/Phase_X/Task_X.X_Log.md`
- Content: Progress, code, decisions, issues

#### Review Log
For Manager reviews:
- Location: `Memory/Reviews/[TaskID]_Review.md`
- Content: Feedback, approval status, actions

#### Phase Summary
For phase completion:
- Location: `Memory/Phase_X/Summary.md`
- Content: Completed tasks, outcomes, metrics

#### General Project Log
For cross-cutting concerns:
- Location: `Memory/Project_Log.md`
- Content: Decisions, changes, clarifications

### 2. Memory Bank Entry Format

Use this structure for consistency:

```markdown
# [Entry Title]

## Entry Metadata
- **Date**: [Current timestamp]
- **Agent**: [Your agent type and ID]
- **Type**: [Implementation|Review|Decision|Update]
- **Related Task**: [Task ID if applicable]

## Entry Content

### [Section 1 - e.g., Progress Update]
[Detailed content]

### [Section 2 - e.g., Code Implementation]
```[language]
[Code snippet]
```
**Purpose**: [What this code does]
**Rationale**: [Why implemented this way]

### [Section 3 - e.g., Decisions Made]
- **Decision**: [What was decided]
- **Context**: [Why it was necessary]
- **Impact**: [How it affects the project]

### [Section 4 - e.g., Issues/Blockers]
- **Issue**: [Description]
- **Status**: [Resolved|Pending|Escalated]
- **Action**: [What was done or needed]

## Next Steps
[What happens next based on this entry]
```

### 3. Log Categories

#### Implementation Progress
```markdown
### Implementation Progress - [Timestamp]
- Completed: [What was finished]
- In Progress: [Current work]
- Code Changes: [Files affected]
- Tests: [Test results]
```

#### Technical Decisions
```markdown
### Technical Decision - [Timestamp]
**Decision**: [What was decided]
**Options Considered**:
1. [Option 1]: [Pros/Cons]
2. [Option 2]: [Pros/Cons]
**Chosen**: [Which option and why]
**Implementation**: [How it will be done]
```

#### Problem Resolution
```markdown
### Problem Resolution - [Timestamp]
**Problem**: [Description]
**Root Cause**: [Analysis]
**Solution**: [What fixed it]
**Prevention**: [How to avoid in future]
```

#### Integration Notes
```markdown
### Integration - [Timestamp]
**Component**: [What was integrated]
**With**: [What it connects to]
**Method**: [How integration works]
**Testing**: [Verification approach]
```

### 4. Code Documentation
When logging code:
```markdown
### Implementation: [Feature Name]
```[language]
// Clear, well-commented code
function exampleFunction() {
    // Implementation details
}
```
**Usage**: `exampleFunction(param1, param2)`
**Returns**: [What it returns]
**Side Effects**: [Any side effects]
```

### 5. Best Practices

#### DO:
- Log regularly (at least daily)
- Be concise but complete
- Include context for decisions
- Document both successes and failures
- Use consistent formatting
- Include code snippets
- Add timestamps

#### DON'T:
- Leave long gaps without updates
- Log sensitive information
- Duplicate information unnecessarily
- Use vague descriptions
- Forget to document blockers
- Skip important decisions

### 6. Memory Bank Validation
After logging, ensure:
- Entry follows project format
- Location matches Implementation Plan
- Links to related entries work
- No duplicate information
- Clear and readable

### 7. Collaborative Logging
When multiple agents work together:
- Reference other agents' logs
- Avoid conflicting information
- Build on previous entries
- Maintain consistent terminology

## Create Your Log Entry

Based on your current context, create an appropriate Memory Bank entry following the format above. Ensure it provides value for future reference and maintains project continuity.