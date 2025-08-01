# /monkeyproof-plan

Creates a comprehensive, atomic-commit execution plan with NO FUZZY BITS. The planning phase resolves everything upfront so execution is purely mechanical.

## Usage
```
/monkeyproof-plan $FEATURE_DESCRIPTION
```

## Core Principle
**Planning phase resolves EVERYTHING, execution is purely mechanical**
- Every step = exactly one atomic commit
- Zero decisions required during execution
- Complete specifications with exact code and commands
- Exhaustive upfront research and resolution

## Process

### Phase 1: Exhaustive Upfront Resolution (NO FUZZY BITS)

#### 1. Initial Decisions
Ask user immediately:
- **Branch Strategy:** "Should I create a new branch for this feature? (recommended: yes)"
- **Scope Clarification:** Ask any clarifying questions about the feature requirements
- **Constraints:** Any specific requirements, patterns to follow, or limitations

#### 2. Comprehensive Information Gathering
Use continuous thinking (at least 2 passes) to analyze the feature requirements, then:

**Code Discovery:**
- Use Glob to find all relevant files and patterns
- Use Grep extensively to find existing similar implementations
- Use Read to understand current architecture and conventions
- Identify exact patterns and code examples to follow

**Research Phase:**
- Use WebSearch to research best practices for this type of feature
- Find solutions to any technical challenges identified
- Research testing approaches and validation strategies
- Resolve any architectural questions

**Context Building:**
- Understand all affected components and their relationships
- Identify all dependencies and prerequisites
- Map out integration points and potential conflicts
- Analyze edge cases and error scenarios

#### 3. Complete Architecture Resolution
Before proceeding, resolve ALL:
- Implementation approaches and technical decisions
- Code patterns and conventions to follow
- Error handling strategies
- Testing approaches and frameworks
- Integration requirements
- Performance considerations

### Phase 2: Atomic Execution Design

#### 4. Atomic Commit Boundary Analysis
Break down the work into atomic units where each unit:
- Represents one logical, complete change
- Can be committed independently without breaking functionality
- Has clear, measurable success criteria
- Can be rolled back safely without affecting other changes

#### 5. Precise Step Specification
For each atomic unit, provide:
- **Exact files to modify** (full paths)
- **Exact code to write** (complete code snippets, not descriptions)
- **Exact commands to run** (with expected outputs)
- **Exact validation steps** (specific tests, checks, build commands)
- **Exact commit message** (pre-written, following project conventions)

#### 6. Dependency Ordering
Sequence steps so that:
- Prerequisites come before dependents
- Each step builds incrementally on previous steps
- Tests are written before implementations (TDD red-green cycle)
- Integration tests come after unit tests
- Documentation and validation come last

### Phase 3: Zero-Decision Execution Plan

#### 7. Create Complete Execution Specification
Generate a plan where someone can:
- Copy/paste exact code snippets
- Run exact commands with expected outputs
- Validate each step with precise criteria
- Commit with pre-written messages
- Never need to make decisions or do research

#### 8. Quality Assurance Planning
Include explicit steps for:
- Running tests after each relevant change
- Type checking and linting validation
- Build verification
- Integration testing
- Final comprehensive validation

#### 9. Error Recovery Planning
For each step, specify:
- What could go wrong
- How to detect failures
- Exact recovery steps
- When to abort vs. continue

### Phase 4: Plan Generation and Execution Setup

#### 10. Branch Creation (if chosen)
Create and switch to feature branch with descriptive name

#### 11. Generate TodoWrite List
Convert the complete plan into TodoWrite format with:
- Each atomic step as a separate todo
- High priority for core functionality
- Medium priority for supporting features  
- Low priority for documentation and final validation
- Clear, actionable descriptions with exact specifications

#### 12. Final Plan Validation
Ensure the plan has:
- No ambiguous steps or fuzzy bits
- Complete code specifications for all changes
- Exact validation criteria for each step
- Pre-written commit messages
- Clear success/failure criteria
- Comprehensive error handling

## Success Criteria

The generated plan should be so complete that:
- Someone unfamiliar with the codebase could execute it successfully
- No research or decision-making is required during execution
- Each step results in exactly one atomic commit
- The git history tells a clear story of feature development
- All edge cases and error scenarios are handled
- The implementation follows existing project patterns exactly

## Key Techniques

- **Continuous Thinking**: Use multiple passes to ensure comprehensive analysis
- **Exhaustive Code Discovery**: Use all available tools to understand existing patterns
- **Research-Driven**: Use WebSearch to resolve technical questions upfront
- **Test-Driven Design**: Plan tests before implementations
- **Atomic Boundaries**: Each step is one complete, logical change
- **Zero Ambiguity**: Every instruction is precise and actionable
- **Error Prevention**: Plan for failures and recovery scenarios
- **Context Preservation**: Capture all reasoning and decisions in the plan

## Example Usage

```
/monkeyproof-plan Add user authentication with JWT tokens and refresh mechanism
```

This would generate a complete plan with exact code, tests, validation steps, and atomic commits for implementing the entire authentication system.