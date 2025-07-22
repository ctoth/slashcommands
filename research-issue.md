---
description: Research and investigate topics comprehensively to create well-informed GitHub issues
allowed-tools: mcp__continuous-thinking__sequentialthinking, Read, Grep, Glob, WebSearch, mcp__zen__chat, TodoWrite, Bash
---

# Research-Driven Issue Investigation and Creation

## Context Gathering
!`pwd && git status --porcelain && echo "=== Current Branch ===" && git branch --show-current && echo "=== Recent Issues ===" && gh issue list --limit 5`

## Your Task
Conduct comprehensive research and investigation to create a well-informed GitHub issue for: $ARGUMENTS

This command guides you through systematic investigation of current systems, research of industry patterns, analysis of integration constraints, and synthesis into a compelling GitHub issue that balances user needs with technical feasibility.

### Phase 1: Understanding the Current System
Use continuous thinking to plan your investigation approach, then systematically analyze:

**1.1 Map the Current Implementation**
- Use Read and Grep to understand how the current system works
- Identify key files, functions, and architectural patterns
- Document the current user experience and workflow
- Note limitations, pain points, or areas for improvement

**1.2 Analyze Constraints and Integration Points**
- Examine existing patterns (APIs, UI conventions, data models)
- Check for conflicting functionality or naming
- Understand performance, security, or compatibility requirements
- Identify stakeholders and affected user workflows

**1.3 Progress Tracking**
Use TodoWrite to track your investigation progress with specific, actionable items.

### Phase 2: External Research and Validation
Research industry patterns and validate your understanding:

**2.1 Industry Pattern Research**
- Use WebSearch or the chat tool with web search to research:
  - How similar applications handle this problem
  - Industry standards and best practices
  - Accessibility guidelines and user experience patterns
  - Common implementation approaches

**2.2 Competitive Analysis**
- Identify what works well in existing solutions
- Note gaps or opportunities for innovation
- Understand user expectations from similar tools
- Gather evidence for design decisions

**2.3 Technical Feasibility**
- Research technical constraints and possibilities
- Identify potential libraries, frameworks, or patterns
- Understand implementation complexity and tradeoffs

### Phase 3: Synthesis and Issue Creation
Transform your research into a compelling, actionable GitHub issue:

**3.1 Problem Definition**
- Lead with the user problem in natural, conversational language
- Use specific examples and user stories
- Quantify the impact where possible (time saved, users affected, etc.)
- Explain why this matters now

**3.2 Solution Design**
- Present research-backed recommendations
- Show how your solution integrates with existing systems
- Address potential concerns or objections
- Include keyboard shortcuts, API changes, or UI modifications as specific as possible

**3.3 Issue Structure**
Follow this proven format:
```
# [Natural Title - focus on user benefit]

# The Problem
[Conversational explanation with concrete examples]

# What We Should Do Instead  
[Research-backed solution with specific details]

# How It Works Now
[Current system analysis with file references]

# What Users Want
[Real user quotes or scenarios]

# Success Criteria
[Specific, measurable checkboxes]
```

**3.4 Iterative Refinement**
- Present draft to user for feedback
- Iterate on language, scope, and technical details
- Remove jargon and make it accessible
- Ensure it's actionable for implementers

### Phase 4: Issue Creation and Validation
**4.1 Create the GitHub Issue**
- Use `gh issue create` with your refined content
- Ensure proper formatting and readability
- Include relevant labels or project assignments if appropriate

**4.2 Validation**
- Verify the issue was created successfully
- Check that all links and references work
- Confirm the issue appears in the project's issue list
- Review for any formatting or content issues

## Success Criteria
- [ ] Comprehensive understanding of current system documented with specific file references
- [ ] External research conducted with evidence from industry patterns
- [ ] Integration constraints and opportunities identified
- [ ] User problem clearly articulated with concrete examples
- [ ] Solution recommendations backed by research
- [ ] Issue created with natural, conversational language
- [ ] Success criteria are specific and measurable
- [ ] Todo list maintained throughout process
- [ ] Final issue is actionable for implementers

## Quality Markers
- **Research-driven**: Recommendations supported by evidence from current system analysis and industry research
- **Integration-aware**: Solution considers existing patterns, constraints, and user workflows  
- **User-centered**: Problem definition focuses on user experience and concrete benefits
- **Actionable**: Issue includes specific technical details and clear success criteria
- **Conversational**: Language is natural and accessible, avoiding unnecessary jargon
- **Systematic**: Logical progression through investigation → research → synthesis → creation