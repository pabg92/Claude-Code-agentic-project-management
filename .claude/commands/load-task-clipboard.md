# Load Task Assignment from Clipboard

As an Implementation Agent, you will now load and parse a task assignment that has been copied to your clipboard. This command processes the Manager Agent's task assignment prompt.

## Loading Process

### 1. Parse Task Assignment
Extract the following information from the clipboard content:

- **Task ID**: The unique identifier
- **Task Name**: Descriptive title
- **Phase**: Which project phase
- **Objectives**: What needs to be accomplished
- **Deliverables**: Concrete outputs expected
- **Technical Specifications**: Required technologies and approaches
- **Guiding Notes**: Implementation guidance
- **Dependencies**: What must be complete first
- **Acceptance Criteria**: How to measure completion

### 2. Validate Assignment
Ensure the assignment includes:
- [ ] Clear task identification
- [ ] Specific deliverables
- [ ] Technical requirements
- [ ] Acceptance criteria
- [ ] Memory Bank location

### 3. Set Up Task Context
After loading:
1. Confirm task details are understood
2. Note the Memory Bank location for logs
3. Identify any immediate questions
4. Review related Implementation Plan section
5. Check for dependent task outputs

### 4. Initialize Task Workspace
Prepare your working environment:
- Understand project structure
- Identify where to create files
- Review existing codebase if applicable
- Set up Memory Bank log file

### 5. Confirm Task Load
Provide confirmation:
```
✅ Task Loaded Successfully

Task ID: [Extracted ID]
Task Name: [Extracted Name]
Phase: [Extracted Phase]
Memory Bank Location: Memory/Phase_X/Task_X.X_Log.md

Ready to begin implementation.
Next step: Use `/implement start` to begin work.
```

### 6. Handle Loading Issues
If the clipboard doesn't contain a valid task:
- Request proper task assignment format
- Ask for task details from Manager
- Suggest using `/task-prompt` command

## After Loading
1. Review all task details carefully
2. Ask for clarification if needed
3. Use `/implement start` to begin work
4. Set up Memory Bank logging

Parse the task assignment from clipboard and confirm successful loading.