# Load Task Assignment from File

As an Implementation Agent, you will now load and parse a task assignment from a specified file path. This command processes the Manager Agent's task assignment prompt stored in a file.

## File Path: $ARGUMENTS

### Loading Process

### 1. Read Task File
Read the task assignment from the specified file path:
- Validate file exists
- Read complete contents
- Parse task structure

### 2. Parse Task Assignment
Extract the following information from the file:

- **Task ID**: The unique identifier
- **Task Name**: Descriptive title  
- **Phase**: Which project phase
- **Objectives**: What needs to be accomplished
- **Deliverables**: Concrete outputs expected
- **Technical Specifications**: Required technologies and approaches
- **Guiding Notes**: Implementation guidance
- **Dependencies**: What must be complete first
- **Acceptance Criteria**: How to measure completion

### 3. Validate Assignment
Ensure the assignment includes:
- [ ] Clear task identification
- [ ] Specific deliverables
- [ ] Technical requirements
- [ ] Acceptance criteria
- [ ] Memory Bank location

### 4. Set Up Task Context
After loading:
1. Confirm task details are understood
2. Note the Memory Bank location for logs
3. Identify any immediate questions
4. Review related Implementation Plan section
5. Check for dependent task outputs

### 5. Initialize Task Workspace
Prepare your working environment:
- Understand project structure
- Identify where to create files
- Review existing codebase if applicable
- Set up Memory Bank log file

### 6. Confirm Task Load
Provide confirmation:
```
✅ Task Loaded Successfully

Source File: [File path]
Task ID: [Extracted ID]
Task Name: [Extracted Name]
Phase: [Extracted Phase]
Memory Bank Location: Memory/Phase_X/Task_X.X_Log.md

Ready to begin implementation.
Next step: Use `/implement start` to begin work.
```

### 7. Handle Loading Errors
If file loading fails:
- **File Not Found**: Verify the path is correct
- **Invalid Format**: Check file contains proper task assignment
- **Access Denied**: Ensure file permissions
- **Parse Error**: Request properly formatted assignment

## Common File Locations
Task assignments might be stored in:
- `Tasks/[TaskID]_Assignment.md`
- `Assignments/[Phase]/[TaskID].md`
- `.apm/tasks/[TaskID].md`
- Manager-specified custom location

## After Loading
1. Review all task details carefully
2. Ask for clarification if needed
3. Use `/implement start` to begin work
4. Set up Memory Bank logging

Read and parse the task assignment from the specified file path.