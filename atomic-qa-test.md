---
description: Implement next QA test item atomically, building on existing test infrastructure
allowed-tools: Read, Edit, MultiEdit, Bash, Glob, Grep, TodoWrite
---

# Implement QA Test Atomically

## Context Gathering
!`git status && ls tests/ && find . -name "*qa*" -o -name "*QA*" | head -10`

## Your Task
Implement the next QA test item: "$ARGUMENTS"

Build on existing test infrastructure using the atomic methodology. Analyze the QA requirement, extend mocking/infrastructure as needed, implement incrementally, and commit atomically.

### Phase 1: Understanding the QA Requirement
- Analyze the QA test description to understand what needs to be tested
- Break down multi-step requirements into discrete test phases
- Identify the interaction pattern (navigation, audio, speech, UI elements)
- Review existing test patterns to understand current infrastructure
- Determine what new mocking or setup might be needed

### Phase 2: Planning the Implementation
- Read existing test files to understand current patterns and infrastructure
- Plan the test structure (setup, steps, verification, cleanup)
- Identify any extensions needed for mocking system (audio, speech, UI interactions)
- Design test steps with clear separation (Step 1, Step 2, etc. for multi-step tests)
- Plan investigative approach for handling unexpected results

### Phase 3: Implementation
- Extend mocking infrastructure if needed (following existing patterns)
- Implement the test building on established patterns from existing tests
- Use the same setup/activation sequence as existing tests (demo mode, audio map activation)
- Structure test with clear logging for each step
- Implement resilient verification that treats unexpected results as system insights
- Follow existing naming conventions and test structure

### Phase 4: Verification and Atomic Commit
- Run the test to verify it works as expected
- Analyze results and treat "failures" as potential system boundary discoveries
- If test reveals unexpected behavior, document findings in test output
- Ensure test provides valuable insights even if results differ from expectations
- Stage only the test changes: `git add tests/qa-playground.spec.ts`
- Create focused atomic commit with detailed message following established pattern
- Verify commit completed successfully

## Success Criteria
- Test is implemented and runs without breaking existing tests
- Test builds incrementally on existing infrastructure and patterns
- Test provides clear output and insights about system behavior
- Any unexpected results are treated investigatively rather than as failures
- Atomic commit is completed with descriptive message
- Test follows established patterns and conventions
- New infrastructure (if added) integrates cleanly with existing mocking system

## Edge Cases and Variations
- **Complex multi-step tests**: Break into clear phases with separate verification
- **New interaction types**: Extend mocking system following existing WebAudio/Speech patterns
- **Unexpected system behavior**: Document findings and treat as valuable system insights
- **Boundary conditions**: Recognize when tests reveal map edges or system limits
- **Infrastructure conflicts**: Ensure new mocking doesn't break existing functionality

## Quality Checks
- Does the test build on existing patterns without duplicating setup code?
- Are test steps clearly separated and logged for debugging?
- Does the test handle unexpected results gracefully?
- Is the commit message descriptive and follows established format?
- Would the test provide value even if results differ from initial expectations?