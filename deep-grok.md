---
description: Collaboratively investigate and deeply understand a library's architecture, purpose, and design philosophy
allowed-tools: Read, LS, Glob, Grep, TodoWrite, Edit, Write, mcp__continuous-thinking__sequentialthinking, mcp__zen__chat, mcp__zen__thinkdeep, mcp__zen__analyze
---

# Deep Library Investigation and Understanding

## Context Gathering
!`pwd && echo "=== Directory Structure ===" && find . -maxdepth 2 -type d | head -20`
!`echo "=== Key Files ===" && find . -name "*.py" -o -name "*.md" -o -name "*.yml" -o -name "*.yaml" -o -name "*.json" | grep -E "(README|test|example|demo|main)" | head -10`

## Your Task
Conduct a collaborative, systematic investigation to deeply understand this library/codebase: $ARGUMENTS

This is **collaborative investigation** - you should actively engage with the user throughout, asking for guidance, verification, and direction. The goal is understanding the **vision**, **architecture**, **design philosophy**, and **zeitgeist** - not surface-level feature cataloging.

### Phase 1: Investigation Setup and Initial Orientation
**Set up investigation infrastructure:**
- Use TodoWrite to create systematic investigation plan
- Create investigation notes file: `[library-name]-investigation-notes.md`
- Use continuous thinking to establish initial investigation approach

**Engage with user for orientation:**
- Ask about their familiarity with the library
- Understand what specific aspects they want to focus on
- Get initial guidance on where to start exploring

**Key principle**: This is guided discovery - you're not working alone.

### Phase 2: Test-Driven Understanding
**Start with tests as your primary guide:**
- Explore test directories and key test files
- Use continuous thinking to analyze what tests reveal about intended functionality
- Look for integration tests that show full workflows
- Pay attention to test setup - this reveals system assumptions

**If no tests available**: Focus on examples, demos, or main entry points

**Consolidation Checkpoint**: Pause to synthesize what you've learned from tests. Ask user:
- Does this match their understanding of the system's purpose?
- Are there aspects you missed or misunderstood?
- Where should you investigate next?

### Phase 3: Architecture and Design Deep Dive
**Systematically explore codebase structure:**
- Map directories and their responsibilities
- Identify core modules and design patterns
- Use continuous thinking to understand architectural decisions
- Look for configuration, template, or plugin systems

**Use Zen tools for deeper analysis:**
- `mcp__zen__analyze` for comprehensive code analysis when needed
- `mcp__zen__thinkdeep` for complex architectural understanding
- `mcp__zen__chat` to discuss findings and get expert perspective

**Challenge assumptions**: Don't accept first impressions - dig deeper when something seems important.

### Phase 4: Domain-Specific Investigation  
**Based on discoveries, investigate the specific domain:**
- If AI system: understand algorithms and decision-making approaches
- If economic: understand market mechanisms and agent behaviors
- If simulation: understand physics and system dynamics
- If framework: understand abstractions and extension points

**Look for contrasting examples:**
- Working vs broken implementations
- Simple vs complex scenarios
- Different configuration approaches

**User guidance critical**: Ask for direction toward interesting or problematic areas.

### Phase 5: Consolidation - Building Understanding Basecamps
**Consolidation is NOT just summarizing - it's active thinking:**
- **Pattern Recognition**: Connect scattered observations into themes
- **Mental Model Building**: Create unified framework of how system works
- **Assumption Validation**: Test initial impressions against evidence
- **Vision Crystallization**: Move from "what does it do" to "what is it trying to achieve"
- **Gap Identification**: Recognize what you still don't understand

**Update investigation notes with:**
- Key architectural insights and design principles
- Understanding of the system's vision and purpose
- Questions that emerged and need investigation
- The "shape, tone, and zeitgeist" of the project

**User verification essential**: Present understanding for validation and course correction.

### Phase 6: Expert Consultation and Synthesis
**Use Zen tools for expert analysis:**
- Consult with expert models about your findings
- Validate architectural understanding
- Get perspective on design decisions and trade-offs
- Explore implications and broader context

**Final synthesis with user:**
- Present comprehensive understanding of the library's essence
- Discuss what makes it innovative or interesting
- Explore how pieces fit together into coherent vision
- Identify remaining questions or areas for future investigation

## Success Criteria
- Deep understanding emerges through collaborative investigation
- User actively guides and validates the investigation process
- Understanding focuses on vision and philosophy, not just features
- Architectural decisions and design principles are clearly grasped
- The library's "zeitgeist" and broader purpose is understood
- Investigation notes capture the journey and insights
- Expert consultation validates and deepens understanding

## Investigation Principles
- **Collaborative Discovery**: Engage user throughout - this is guided exploration
- **Think Continuously**: Use continuous thinking to process each discovery
- **Challenge Assumptions**: Question first impressions and dig deeper
- **Consolidate Actively**: Build understanding basecamps, don't just summarize
- **Seek Contrasts**: Compare working vs broken examples to understand constraints
- **Focus on Vision**: Understand what creators were trying to achieve
- **Use Expert Tools**: Leverage Zen tooling for deeper analysis and validation
- **Ask for Guidance**: When uncertain, ask user for direction or clarification

## Edge Case Handling
- **No tests available**: Focus on examples, demos, main files, or ask user for starting points
- **Very large codebase**: Ask user which areas to prioritize, use Zen tools for systematic analysis
- **Unfamiliar domain**: Use expert consultation to understand domain concepts
- **Conflicting evidence**: Present findings to user for interpretation and guidance
- **Investigation stalls**: Ask user for new directions or use Zen tools for fresh perspective

Remember: Deep understanding emerges through dialogue and collaboration. You're not investigating alone - you're working with the user to uncover the essence and vision of this library together.