---
description: Analyze successful workflow interactions and generate reusable slash commands
allowed-tools: [mcp__continuous-thinking__sequentialthinking, Read, Edit, Bash]
---

# Generate Slash Command from Successful Workflow

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
**First, read the command template**: Use the Read tool on `~/.claude/commands/command-template.md` to get the standard structure and design principles.

Create the slash command following the template structure and best practices outlined in the template file.

### Phase 4: Command Metadata and Documentation
Provide:
- Proposed command name and usage format
- Suggested filename and location
- Key design decisions and rationale
- Flexibility considerations for variations
- Usage examples and scenarios
- **Stage and commit the new command**:
  - If command is in `~/.claude/commands/`: `cd ~/.claude/commands && git add [command-name].md`
  - If command is in project `.claude/commands/`: `git add .claude/commands/[command-name].md`
  - `git commit -m "feat: add [command-name] command - [brief description of purpose]"`
- Verify git operations completed successfully
- **REMINDER: Restart Claude Code after creating the command for it to be available**

## Success Criteria
- Command captures the reasoning process, not just the steps
- Instructions are clear without requiring context from original conversation
- Flexible enough for variations of the original task
- Includes proper validation and verification steps
- **Automatically staged and committed the new command to git**
- Follows Claude Code slash command conventions

## Quality Checks
Before finalizing:
- Does the command encode expertise and decision-making logic?
- Are the instructions self-contained and clear?
- Would a new user understand when and how to use this command?
- Are edge cases and variations considered?
- Is the command structure efficient and maintainable?

