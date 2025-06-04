# Validate Memory Bank Structure

Perform a comprehensive validation of the Memory Bank to ensure it maintains proper structure, consistency, and alignment with the Implementation Plan.

## Validation Process

### 1. Structure Validation

Check the Memory Bank organization:

#### For Multi-File Memory Bank
Verify directory structure matches Implementation Plan:
```
Memory/
├── README.md                    ✓ Exists and current
├── Phase_1/                     ✓ Matches plan phases
│   ├── Task_1.1_Log.md         ✓ Follows naming convention
│   ├── Task_1.2_Log.md         ✓ Has required sections
│   └── Summary.md              ✓ Phase summary present
├── Phase_2/                     ✓ All phases represented
│   └── ...
├── Reviews/                     ✓ Review logs organized
└── Handovers/                   ✓ Handover docs if needed
```

#### For Single-File Memory Bank
Verify `Memory_Bank.md` contains:
- [ ] Clear section headers
- [ ] Chronological ordering
- [ ] All phases represented
- [ ] Consistent formatting

### 2. Content Validation

For each Memory Bank entry, check:

#### Required Sections
- [ ] Entry metadata (date, agent, type)
- [ ] Clear section headers
- [ ] Actual content (not just placeholders)
- [ ] Next steps or status

#### Content Quality
- [ ] Entries are informative
- [ ] Code snippets are complete
- [ ] Decisions are justified
- [ ] Progress is trackable

### 3. Consistency Checks

#### Task Alignment
Verify against Implementation Plan:
- [ ] All started tasks have logs
- [ ] Task IDs match the plan
- [ ] No orphaned task logs
- [ ] Dependencies are noted

#### Naming Conventions
Check file naming:
- Pattern: `Task_X.X_Log.md`
- Reviews: `[TaskID]_Review.md`
- Summaries: `Summary.md` or `README.md`

#### Cross-References
Validate references:
- [ ] Links between related logs work
- [ ] Dependencies are bidirectional
- [ ] No broken references

### 4. Completeness Audit

#### Coverage Check
For each phase in Implementation Plan:
```
Phase X: [Name]
├── Expected Tasks: [Count from plan]
├── Actual Logs: [Count in Memory Bank]
├── Missing: [List any gaps]
└── Status: ✅ Complete | ⚠️ Partial | ❌ Missing
```

#### Review Coverage
- [ ] Completed tasks have reviews
- [ ] Review feedback is addressed
- [ ] Follow-up actions are tracked

### 5. Format Compliance

Verify entries follow format:
```markdown
# [Clear Title]

## Entry Metadata
- **Date**: [ISO format preferred]
- **Agent**: [Type and identifier]
- **Type**: [Standard types only]

## [Content sections with headers]

## Next Steps
[Clear actions or status]
```

### 6. Validation Report

Generate a validation report:

```markdown
# Memory Bank Validation Report
Date: [Current date]

## Structure Validation
- Directory Structure: ✅ Valid | ❌ Issues found
- Naming Conventions: ✅ Compliant | ❌ Non-compliant
- Required Directories: ✅ All present | ❌ Missing: [list]

## Content Validation  
- Entry Completeness: [X]% complete
- Format Compliance: [X]% compliant
- Cross-references: [X] valid, [Y] broken

## Alignment with Implementation Plan
- Phase Coverage: [X]/[Y] phases documented
- Task Coverage: [X]/[Y] tasks logged
- Review Coverage: [X]/[Y] reviews completed

## Issues Found
1. [Issue description and location]
2. [Issue description and location]

## Recommendations
1. [Specific action to fix issues]
2. [Improvement suggestion]

## Overall Health
🟢 Healthy | 🟡 Needs Attention | 🔴 Critical Issues
```

### 7. Common Issues

Watch for these problems:
- Empty or placeholder logs
- Inconsistent naming
- Missing task logs
- Orphaned files
- Broken cross-references
- Outdated summaries
- Format violations

### 8. Corrective Actions

If issues are found:
1. Document in validation report
2. Create fix recommendations
3. Update problematic entries
4. Align with Implementation Plan
5. Notify relevant agents

Perform the Memory Bank validation and generate a comprehensive report.