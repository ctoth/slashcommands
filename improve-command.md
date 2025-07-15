---
description: Analyze slash command usage and iteratively improve commands based on user feedback
allowed-tools: [mcp__continuous-thinking__sequentialthinking, Read, Edit, Bash]
---

# Improve Slash Command Based on Usage Experience

## Context Gathering
!`ls -la .claude/commands/ && echo "Recent commands:" && ls -t .claude/commands/ | head -5`

## Your Task
Analyze the recent usage of a slash command and improve it based on actual user experience, modifications needed, and additional interactions that occurred.

**Target command to improve:** $ARGUMENTS (specify the command name/file to analyze and improve)

### Phase 1: Usage Analysis
Use continuous thinking to analyze the conversation history and identify:
- How the specified slash command was actually used
- What parts worked well vs. what didn't
- What changes or clarifications the user had to make
- What additional interactions were needed after running the command
- What gaps or missing steps were discovered
- What assumptions in the original command were incorrect

### Phase 2: Gap Identification
Systematically identify improvement opportunities:
- Steps that were unclear or missing
- Parameters that need better guidance
- Tools that should be added or removed
- Success criteria that need refinement
- Edge cases that weren't considered
- User experience friction points

### Phase 3: Improvement Proposal
Generate specific, actionable improvements:
- Exact text changes needed
- Additional phases or steps to add
- Better parameter handling or examples
- Clearer instructions or context
- Enhanced validation or verification steps
- Improved error handling or edge case coverage

### Phase 4: User Verification
Present the proposed improvements to the user:
```
## Proposed Improvements for [Command Name]

### Issues Identified:
- [Specific problem 1]
- [Specific problem 2]
- [etc.]

### Proposed Changes:
1. **[Section/Area]**: [Specific change with before/after]
2. **[Section/Area]**: [Specific change with before/after]
3. [etc.]

### Rationale:
- Why these changes address the identified issues
- How they improve user experience
- What edge cases they handle better

**Do you want me to make these changes to the slash command?**
```

Wait for explicit user approval before proceeding.

### Phase 5: Implementation
Only after user approval:
- First locate the command file: `find ~ -name "[command-name].md" -path "*/.claude/commands/*" -type f 2>/dev/null`
- Read the current command file from the located path
- Apply the approved changes using Edit tool
- Verify the changes were applied correctly
- Confirm the improved command structure
- **Stage and commit the improved command**:
  - If command is in `~/.claude/commands/`: `cd ~/.claude/commands && git add [command-name].md`
  - If command is in project `.claude/commands/`: `git add .claude/commands/[command-name].md`
  - `git commit -m "improve: enhance [command-name] based on usage experience - [brief description of changes]"`
- Verify git operations completed successfully
- **REMINDER: Restart Claude Code for changes to take effect**

## Success Criteria
- Identified specific usage gaps from conversation history
- Proposed concrete, actionable improvements
- Got explicit user verification before making changes
- Successfully applied improvements to the command file
- **Automatically staged and committed the improved command to git**
- Verified the updated command follows Claude Code conventions

## Quality Checks
Before proposing changes:
- Are the identified issues specific and evidence-based?
- Do the proposed changes directly address the issues?
- Are the improvements backward-compatible where possible?
- Will the changes make the command more robust and user-friendly?
- Are the instructions still clear and self-contained?

## User Verification Protocol
**CRITICAL**: Always get explicit user approval before editing any command files. Present:
1. Clear summary of identified issues
2. Specific proposed changes with rationale
3. Request for approval: "Should I make these changes?"
4. Only proceed with Edit tool after user says yes