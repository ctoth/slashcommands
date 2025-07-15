---
description: "Streamlined feature development for small enhancements"
tools: ["TodoWrite", "Bash", "Read", "Edit", "Write", "Grep", "Glob"]
---

# Quick Feature Enhancement

Streamlined workflow for: **$ARGUMENTS**

This is a simplified version of the full `/enhance` workflow for smaller features that don't require extensive architectural design.

## Quick Workflow

### 1. Confirm & Branch
- **Confirm**: Ready to implement small enhancement
- **Branch**: `git checkout -b "quick/$(echo '$ARGUMENTS' | tr ' ' '-' | tr '[:upper:]' '[:lower:]')"`

### 2. Research (5-10 min max)
- Quick codebase examination with get_symbols/Grep
- Identify integration points
- **Commit**: `"docs: research notes for $ARGUMENTS"`

### 3. Implementation
- Direct implementation with TodoWrite tracking
- **Atomic commits** after each logical change
- Pattern: `feat: [specific change]`

### 4. Basic Testing
- Quick functional test
- Update existing tests if needed
- **Commit**: `"test: add basic tests for [feature]"`

### 5. Quick Documentation
- Update relevant docs/comments
- **Commit**: `"docs: update for [feature]"`

## Use When:
- Small utility functions
- Configuration changes
- Documentation improvements
- Bug fixes
- Minor UI tweaks

## Skip This For:
- New major features
- Architectural changes
- Performance optimizations
- Security enhancements
- API design changes

**🚀 Execute quickly while maintaining atomic commit discipline.**