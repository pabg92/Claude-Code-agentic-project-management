# Read Memory Bank Entry

Read specific entries from the Memory Bank to understand project context, review past work, or check implementation details.

## Path: $ARGUMENTS

### Reading Memory Bank

The Memory Bank can be organized as:
1. **Single File**: `Memory_Bank.md` (simple projects)
2. **Multi-File**: `Memory/` directory structure (complex projects)

### Common Read Patterns

#### Read Specific Task Log
Path examples:
- `Memory/Phase_1/Task_1.1_Log.md`
- `Memory/Phase_2/Task_2.3_Log.md`

#### Read Phase Summary  
Path examples:
- `Memory/Phase_1/README.md`
- `Memory/Phase_2/Summary.md`

#### Read Review Logs
Path examples:
- `Memory/Reviews/Phase_1_Review.md`
- `Memory/Reviews/Task_1.1_Review.md`

#### Read from Single-File Memory Bank
For simple projects using `Memory_Bank.md`:
- Read entire file if no specific section provided
- Or specify section like `Memory_Bank.md#Phase-1`

### What to Look For

When reading Memory Bank entries:

#### Task Implementation Logs
- Implementation approach
- Code snippets and decisions
- Test results
- Challenges and solutions
- Integration details

#### Review Feedback
- Manager comments
- Required changes
- Approval status
- Follow-up actions

#### Project Context
- Completed work
- Dependencies
- Technical decisions
- Lessons learned

### Reading Best Practices

1. **Start Broad**: Read phase summaries first
2. **Then Specific**: Dive into individual task logs
3. **Check Reviews**: Understand feedback patterns
4. **Note Dependencies**: See how tasks connect
5. **Learn Patterns**: Identify project conventions

### After Reading

Based on what you read:
1. Understand the context
2. Identify relevant patterns
3. Note any dependencies
4. Apply learnings to current work
5. Ask questions if unclear

### Common Memory Bank Structure
```
Memory/
├── README.md                 # Overview
├── Phase_1/
│   ├── Task_1.1_Log.md      # Implementation details
│   ├── Task_1.2_Log.md      
│   └── Summary.md           # Phase summary
├── Phase_2/
│   ├── Task_2.1_Log.md
│   └── Task_2.2_Log.md
├── Reviews/
│   ├── Phase_1_Review.md    # Manager feedback
│   └── Task_2.1_Review.md
└── Handovers/
    └── Agent_A_Handover.md   # Transition docs
```

Read the specified Memory Bank entry or section.