---
description: "Collaborative feature development workflow with multi-model feedback and atomic commits"
tools: ["TodoWrite", "mcp__zen__chat", "mcp__continuous-thinking__sequentialthinking", "exit_plan_mode", "Bash", "Read", "Edit", "Write", "Grep", "Glob", "MultiEdit"]
---

# Enhanced Collaborative Feature Development Workflow

You are now entering a structured feature development workflow for: **$ARGUMENTS**

This workflow combines deep thinking, multi-model collaboration, atomic commits, and systematic validation to deliver high-quality features.

## Pre-Workflow Setup

### 1. User Confirmation & Branch Creation
```
🎯 CONFIRM: "Ready to enhance: $ARGUMENTS"
📁 CREATE: feature branch with sanitized name
⚡ SET: atomic commit strategy
```

### 2. Continuous Thinking Initialization
Use `mcp__continuous-thinking__sequentialthinking` throughout for:
- Problem decomposition and architectural analysis
- Design decision reasoning
- Implementation strategy thinking
- Quality validation insights

## Workflow Phases

### Phase 1: Deep Research & Understanding
**🧠 Thinking Focus**: Problem space analysis, existing architecture review

**Actions**:
1. **Start continuous thinking** to analyze the problem space
2. **Examine codebase** with get_symbols, Grep, Read tools
3. **Map integration points** and identify constraints
4. **Document insights** from thinking process

**💾 Atomic Commit**: `"docs: add research notes for [feature]"`

### Phase 2: Multi-Model Collaborative Design
**🧠 Thinking Focus**: Solution space exploration, design alternatives

**Model Consultation Strategy**:
- **o3/o3-pro**: Complex architectural decisions, system design
- **gemini-2.5-pro**: Performance optimization, scalability concerns  
- **flash models**: Quick validation, implementation details
- **Domain-specific**: API design, UI/UX, database, security

**Actions**:
1. **Use thinking** to frame design questions and alternatives
2. **Consult models** via `mcp__zen__chat` based on complexity and domain
3. **Synthesize feedback** from multiple expert perspectives
4. **Document decisions** with reasoning and trade-offs

**💾 Atomic Commit**: `"design: add architectural decision records for [feature]"`

### Phase 3: Structured Planning with User Gates
**🧠 Thinking Focus**: Implementation strategy, risk assessment, task breakdown

**Actions**:
1. **Think through** implementation approach systematically
2. **Present plan** via `exit_plan_mode` with detailed breakdown
3. **🚨 USER CONFIRMATION REQUIRED** - wait for explicit approval
4. **Refine plan** based on user feedback and concerns
5. **Set up TodoWrite** tracking for implementation tasks

**💾 Atomic Commit**: `"plan: add implementation roadmap for [feature]"`

### Phase 4: Incremental Implementation with Frequent Commits
**🧠 Thinking Focus**: Implementation execution, problem-solving, code quality

**Commit Strategy** (CRITICAL):
- **Atomic commits** after each logical unit of work
- **Immediate commits** - never accumulate multiple changes
- **Descriptive messages**: `feat|fix|refactor|test: [specific change]`
- **Single concern** per commit

**Implementation Flow**:
1. **Use thinking** before each major implementation step
2. **Update TodoWrite** status as you progress
3. **Commit immediately** after each:
   - New file/module creation
   - Complete function implementation
   - Test addition or fix
   - Configuration change
   - Documentation update

**Example Atomic Commits**:
```
feat: add VCS abstraction interface
feat: implement GitProvider class with pathlib
test: add GitProvider unit tests for all methods
feat: create unified file reader with VCS detection
feat: update get_symbols to support git_revision parameter
test: add integration tests for git revision support
docs: update function docstrings with git examples
```

### Phase 5: Comprehensive Testing with Model Review
**🧠 Thinking Focus**: Test strategy, edge case identification, quality assurance

**Actions**:
1. **Think through** comprehensive test scenarios
2. **Consult testing experts** via chat for strategy validation
3. **Implement test suite** with atomic commits for each test file
4. **Run all tests** and validate functionality
5. **Fix issues** with focused atomic commits

**💾 Atomic Commits**:
- `"test: add unit tests for [component]"`
- `"test: add integration tests for [feature]"`
- `"fix: resolve edge case in [specific function]"`

### Phase 6: Documentation & Knowledge Capture
**🧠 Thinking Focus**: Knowledge transfer, usage patterns, architectural insights

**Actions**:
1. **Use thinking** to identify key documentation needs
2. **Update project docs** with feature usage and examples
3. **Add architectural notes** from design thinking
4. **Document decisions** and trade-offs for future reference

**💾 Atomic Commits**:
- `"docs: update README with [feature] usage examples"`
- `"docs: add architecture notes for VCS abstraction"`
- `"docs: document git revision parameter in CLAUDE.md"`

### Phase 7: Pre-Merge Validation
**🧠 Thinking Focus**: Quality assurance, merge readiness, impact assessment

**Validation Checklist**:
- [ ] All tests passing
- [ ] Documentation updated
- [ ] Atomic commits throughout (review git log)
- [ ] User confirmations obtained
- [ ] Multi-model feedback incorporated
- [ ] Continuous thinking insights documented

**💾 Final Commit**: `"chore: prepare [feature] for merge review"`

## Advanced Model Selection

```
🤖 Model Selection Algorithm:
- Architectural complexity (high) → o3-pro + thinking
- Performance critical → gemini-2.5-pro + benchmarking focus
- API design → o3 + domain expert consultation
- UI/UX enhancement → design-focused models + user experience
- Database/persistence → data architecture specialists
- Security features → security-focused models + threat modeling
- Quick validation → flash models for rapid feedback
```

## Atomic Commit Philosophy

**🔑 Core Principles**:
- **One logical change** per commit (never mix concerns)
- **Immediate commits** after completion (don't accumulate)
- **Descriptive messages** with context and reasoning
- **Rollback safety** - each commit should be independently stable
- **Reviewable units** - each commit tells a story

**🚫 Anti-Patterns to Avoid**:
- Mixing feature implementation with refactoring
- Combining multiple file creations in one commit
- Batching test additions with feature implementation
- Holding changes until "everything is done"

## User Confirmation Gates

**🚨 Required Confirmations**:
1. **Feature Start** - confirm scope and approach
2. **Architecture Approval** - approve design after expert consultation
3. **Major Refactors** - confirm impact on existing code
4. **Pre-Merge** - final review and merge strategy

## Branch Management Strategy

**🌿 Branch Operations**:
```bash
# Create feature branch
git checkout -b "feature/$(echo '$ARGUMENTS' | tr ' ' '-' | tr '[:upper:]' '[:lower:]')"

# Atomic commit pattern
git add [specific-files]
git commit -m "[type]: [specific-change-description]"

# Regular status checks
git log --oneline -10  # Review commit history
```

## Quality Gates

**✅ Success Criteria**:
- [ ] Deep thinking applied to all major decisions
- [ ] Multiple expert models consulted for complex choices
- [ ] User maintains control with explicit confirmations
- [ ] Clean atomic commit history with logical progression
- [ ] Comprehensive testing and documentation
- [ ] Backward compatibility maintained
- [ ] Architecture supports future extensibility

---

**🚀 Execute this workflow methodically, ensuring each phase is complete before proceeding to the next. Use continuous thinking throughout to maintain context and quality.**