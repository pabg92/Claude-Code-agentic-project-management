# Synchronize Memory Bank

Ensure Memory Bank consistency and resolve any conflicts or synchronization issues. This command helps maintain a single source of truth across all agents.

## Synchronization Process

### 1. Check for Conflicts

Identify potential sync issues:
- **Concurrent Edits**: Multiple agents editing same file
- **Merge Conflicts**: Overlapping changes
- **Version Mismatches**: Outdated local copies
- **Missing Updates**: Uncommitted changes

### 2. Sync Strategy

#### For Git-Managed Projects
```bash
# Pull latest changes
git pull

# Check for conflicts
git status

# If conflicts exist, resolve them
# Then commit and push
git add Memory/
git commit -m "Memory Bank sync: [description]"
git push
```

#### For Non-Git Projects
- Compare timestamps
- Identify latest versions
- Merge changes manually
- Create backup before sync

### 3. Content Synchronization

#### Merge Parallel Work
When multiple agents work simultaneously:

```markdown
## Merged Entry - [Timestamp]
### From Agent A:
[Content from Agent A]

### From Agent B:
[Content from Agent B]

### Consolidated:
[Merged content preserving both contributions]
```

#### Resolve Conflicts
For conflicting information:
1. Identify conflict source
2. Determine authoritative version
3. Document resolution rationale
4. Update all references

### 4. Structure Alignment

Ensure Memory Bank matches Implementation Plan:

#### Add Missing Directories
```bash
# Create expected structure
mkdir -p Memory/Phase_3
mkdir -p Memory/Reviews
```

#### Move Misplaced Files
```bash
# Relocate to correct location
mv Memory/Task_3.1_Log.md Memory/Phase_3/
```

#### Fix Naming Issues
```bash
# Rename to follow convention
mv Memory/task31.md Memory/Phase_3/Task_3.1_Log.md
```

### 5. Cross-Reference Updates

Update references after sync:
- Fix broken links
- Update task IDs
- Align with Implementation Plan
- Ensure bidirectional references

### 6. Sync Checklist

Before synchronization:
- [ ] Backup current Memory Bank
- [ ] Check for uncommitted changes
- [ ] Note any local modifications

During synchronization:
- [ ] Pull/fetch latest changes
- [ ] Resolve any conflicts
- [ ] Validate structure
- [ ] Update cross-references

After synchronization:
- [ ] Verify all changes merged
- [ ] Test critical references
- [ ] Commit synchronized state
- [ ] Notify other agents

### 7. Sync Report

Generate a synchronization summary:

```markdown
# Memory Bank Synchronization Report

## Sync Details
- **Date**: [Current timestamp]
- **Agent**: [Your identification]
- **Sync Type**: [Full|Partial|Conflict Resolution]

## Changes Synchronized
### New Entries
- [List of new files/sections]

### Updated Entries  
- [List of modified files/sections]

### Structural Changes
- [Directories created/moved]
- [Files renamed]

### Conflicts Resolved
- [Conflict 1]: [Resolution]
- [Conflict 2]: [Resolution]

## Post-Sync Status
- Structure: ✅ Aligned with plan
- References: ✅ All valid
- Conflicts: ✅ None remaining
- Version: [Current version/commit]

## Notifications
- [Which agents need to know]
- [What they need to update]
```

### 8. Best Practices

#### Sync Frequency
- At start of each work session
- Before major updates
- After completing tasks
- When switching agents

#### Conflict Prevention
- Communicate active work areas
- Use specific file sections
- Update frequently
- Coordinate through Implementation Plan

#### Documentation
- Log all sync operations
- Document conflict resolutions
- Note any manual interventions
- Keep sync history

### 9. Recovery Procedures

If sync fails:
1. Check backup exists
2. Identify failure point
3. Resolve underlying issue
4. Retry sync operation
5. Validate successful sync

Perform Memory Bank synchronization and ensure consistency across the project.