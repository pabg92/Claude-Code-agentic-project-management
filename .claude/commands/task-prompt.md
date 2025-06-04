# Generate Task Assignment Prompt

As a Manager Agent, you will now generate a detailed task assignment prompt for an Implementation Agent. This prompt will include all necessary context and specifications for the task.

## Task ID: $ARGUMENTS

### Generating Task Assignment

Based on the task ID provided, create a comprehensive assignment prompt that includes:

### 1. Task Context
- Extract task details from Implementation Plan
- Include relevant project context
- Reference any dependencies

### 2. Assignment Prompt Structure

Generate a prompt in this format:

```markdown
# Task Assignment for Implementation Agent

## Task Identification
- **Task ID**: [From Implementation Plan]
- **Task Name**: [Descriptive name]
- **Phase**: [Which project phase]
- **Assigned Agent**: [Target agent identifier]

## Project Context
[Brief overview of the project and how this task fits]

## Task Requirements
### Objective
[Clear statement of what needs to be accomplished]

### Specific Deliverables
1. [Concrete deliverable 1]
2. [Concrete deliverable 2]
3. [Concrete deliverable 3]

### Technical Specifications
- **Technologies**: [Required languages/frameworks]
- **Architecture**: [How it fits in the system]
- **Integration Points**: [What it connects to]

### Guiding Notes
[Extract and expand from Implementation Plan]
- Key approaches to consider
- Recommended libraries or methods
- Important parameters or configurations
- Design patterns to follow

### Dependencies
- **Requires**: [What must be complete first]
- **Enables**: [What this unblocks]

### Constraints
- [Any limitations or requirements]
- [Performance considerations]
- [Security requirements]

### Acceptance Criteria
- [ ] [Specific criterion 1]
- [ ] [Specific criterion 2]
- [ ] [Specific criterion 3]

## Resources
- Implementation Plan: `Implementation_Plan.md`
- Memory Bank: `Memory/Phase_X/`
- Related Tasks: [Reference other task logs]

## Working Instructions
1. Initialize as Implementation Agent: `/apm-init implement`
2. Load this task: `/load-task clipboard`
3. Begin work: `/implement start`
4. Log progress regularly to Memory Bank
5. Complete task: `/implement complete`

## Memory Bank Logging
Create entries in: `Memory/Phase_X/Task_X.X_Log.md`
Include:
- Implementation decisions
- Code snippets
- Test results
- Any blockers or issues

## Questions or Clarifications
If you need clarification:
1. Document the question in Memory Bank
2. Mark task as blocked with reason
3. Await Manager response
```

### 3. Customization Based on Task Type

Adjust the prompt based on task characteristics:
- **Development Tasks**: Include code structure, patterns
- **Testing Tasks**: Include test scenarios, coverage requirements
- **Documentation Tasks**: Include format, audience, scope
- **Integration Tasks**: Include API specs, data formats
- **Debugging Tasks**: Include error details, logs

### 4. Include Relevant Context
Pull from:
- Implementation Plan guiding notes
- Previous related task logs
- Project conventions and standards
- User preferences or requirements

### 5. Make It Self-Contained
Ensure the Implementation Agent has:
- All necessary information to start
- Clear success criteria
- Proper Memory Bank instructions
- Links to relevant resources

## After Generating the Prompt
1. Review for completeness
2. Ensure all task details are included
3. Verify technical specifications are clear
4. Check that acceptance criteria are measurable
5. Copy prompt for Implementation Agent use

Generate the task assignment prompt for the specified task ID.