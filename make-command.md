---
description: Analyze successful workflow interactions and generate reusable slash commands
allowed-tools: [mcp__continuous-thinking__sequentialthinking, Read, Write, Bash]
---

# Generate Slash Command from Successful Workflow

## Context Gathering
!`pwd && ls -la .claude/commands/ 2>/dev/null || echo "No commands directory found"`

## Your Task
Analyze our recent successful workflow interaction and create a reusable slash command that captures the effective patterns, decision-making process, and implementation approach.

**Target workflow:** $ARGUMENTS (describe the successful task/workflow to convert)

### Phase 1: Understanding the Workflow Pattern
Use continuous thinking to analyze the conversation history and identify:
- Core workflow pattern and task type
- Key decision points that led to success
- Essential tools and techniques used
- Prerequisites and context requirements
- What made this interaction particularly effective

### Phase 2: Planning the Command Structure
Determine the command design:
- Identify required parameters (what needs `$ARGUMENTS`)
- Map out the logical flow of steps
- Identify which tools are essential
- Consider variations and edge cases
- Define success criteria and validation steps

### Phase 3: Command Generation
Create the slash command with this structure:
```markdown
---
description: [One-line description for command menu]
allowed-tools: [Optional: specific tools this command can use]
---

# [Task Title]

## Context Gathering
!`[bash commands to gather current state]`

## Your Task
[Clear instructions incorporating $ARGUMENTS where needed]

### Phase 1: Understanding
[Steps to analyze and understand the problem]

### Phase 2: Planning
[Steps to create an approach]

### Phase 3: Implementation
[Steps to execute the solution]

### Phase 4: Verification
[Steps to validate the work]

## Success Criteria
- [Specific checkpoints]
```

### Phase 4: Command Metadata and Documentation
Provide:
- Proposed command name and usage format
- Suggested filename and location
- Key design decisions and rationale
- Flexibility considerations for variations
- Usage examples and scenarios
- **REMINDER: Restart Claude Code after creating the command for it to be available**

## Success Criteria
- Command captures the reasoning process, not just the steps
- Instructions are clear without requiring context from original conversation
- Flexible enough for variations of the original task
- Includes proper validation and verification steps
- Follows Claude Code slash command conventions

## Quality Checks
Before finalizing:
- Does the command encode expertise and decision-making logic?
- Are the instructions self-contained and clear?
- Would a new user understand when and how to use this command?
- Are edge cases and variations considered?
- Is the command structure efficient and maintainable?