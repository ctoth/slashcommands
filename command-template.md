# Slash Command Template

## Standard Structure
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

## Key Design Principles

### Essential Elements
- **Context Gathering**: Bash commands to understand current state
- **Task Definition**: Clear instructions with $ARGUMENTS integration
- **Phased Approach**: Logical progression through understanding → planning → implementation → verification
- **Success Criteria**: Specific, measurable checkpoints

### Best Practices
- Encode expertise and decision-making logic, not just steps
- Make instructions self-contained and context-independent
- Consider edge cases and variations
- Include proper validation steps
- Follow Claude Code slash command conventions

### Command Metadata
When creating commands, provide:
- Proposed command name and usage format
- Suggested filename and location
- Key design decisions and rationale
- Flexibility considerations for variations
- Usage examples and scenarios

### Git Integration
**Always stage and commit new commands**:
- Global commands: `cd ~/.claude/commands && git add [command-name].md`
- Project commands: `git add .claude/commands/[command-name].md`
- Commit: `git commit -m "feat: add [command-name] command - [brief description]"`
- **Remember**: Restart Claude Code after creating commands for availability

### Quality Checklist
- Does the command capture reasoning process, not just steps?
- Are instructions clear without requiring original conversation context?
- Is it flexible enough for task variations?
- Would a new user understand when and how to use it?
- Are edge cases considered?
- Is the structure efficient and maintainable?