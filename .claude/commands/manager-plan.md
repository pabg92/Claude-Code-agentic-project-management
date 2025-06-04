# Manager Agent - Create/Update Implementation Plan

As a Manager Agent, you will now create or update the Implementation Plan based on the project discovery findings. The Implementation Plan is the master document that guides all project work.

## Implementation Plan Structure

Create an `Implementation_Plan.md` file with the following structure:

### 1. Project Overview
- **Goal**: Clear statement of project objective
- **Scope**: What's included and excluded
- **Success Criteria**: Measurable outcomes
- **Constraints**: Technical, time, or resource limitations

### 2. Technical Architecture
- **Technology Stack**: Languages, frameworks, tools
- **System Design**: High-level architecture
- **Key Components**: Major system parts
- **Integration Points**: External dependencies

### 3. Phase Breakdown
For each phase, include:
- **Phase Name & Number**: e.g., "Phase 1: Foundation"
- **Phase Goal**: What this phase achieves
- **Duration Estimate**: Expected timeframe
- **Dependencies**: What must be complete before starting

### 4. Task Definitions
For each task within a phase:
- **Task ID**: Unique identifier (e.g., Task-1.1)
- **Task Name**: Descriptive title
- **Description**: What needs to be done
- **Assigned Agent**: Which agent type will handle this
- **Dependencies**: Other tasks that must complete first
- **Acceptance Criteria**: How to know it's done
- **Guiding Notes**: Key methods, libraries, approaches

### 5. Agent Assignments
- **Manager Agent**: Overall coordination
- **Implementation Agent A**: Tasks focused on [area]
- **Implementation Agent B**: Tasks focused on [area]
- **Specialized Agents**: When needed (Debug, Review, Test)

### 6. Memory Bank Structure
Define the Memory Bank organization:
```
Memory/
├── README.md
├── Phase_1/
│   ├── Task_1.1_Log.md
│   └── Task_1.2_Log.md
├── Phase_2/
│   └── ...
└── Reviews/
    └── ...
```

### 7. Risk Management
- **Identified Risks**: Potential issues
- **Mitigation Strategies**: How to handle them
- **Contingency Plans**: Backup approaches

### 8. Timeline
- **Project Start**: Date
- **Phase Milestones**: Key dates
- **Project Completion**: Target date

## Creating the Plan

1. **Synthesize Discovery**: Use information from project discovery
2. **Break Down Work**: Divide into phases and tasks
3. **Assign Agents**: Distribute work appropriately
4. **Define Dependencies**: Map task relationships
5. **Set Criteria**: Clear acceptance for each task
6. **Include Guiding Notes**: Technical direction for implementers

## Important Considerations
- Make tasks specific and actionable
- Balance workload across agents
- Consider parallel vs sequential work
- Build in review and testing time
- Account for integration tasks

## After Creating the Plan
1. Save as `Implementation_Plan.md` in project root
2. Create initial Memory Bank structure
3. Prepare to generate task assignments
4. Review plan with user for approval

Begin creating the Implementation Plan based on the discovery findings.