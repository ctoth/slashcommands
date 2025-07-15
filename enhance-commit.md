---
description: "Atomic commit utilities for clean version control"
tools: ["Bash", "Read"]
---

# Atomic Commit Utilities

Commit operation: **$ARGUMENTS**

## Atomic Commit Patterns

### Smart Commit
Analyzes changes and suggests appropriate commit message:
```bash
echo "🔍 Analyzing changes..."
git status --porcelain

echo "📝 Suggested commit patterns:"
echo "feat: add new functionality"
echo "fix: resolve bug or issue"  
echo "refactor: improve code structure"
echo "test: add or update tests"
echo "docs: update documentation"
echo "chore: maintenance tasks"
```

### Commit with Validation
```bash
# Check for common issues before committing
echo "✅ Pre-commit validation:"

# Check for large files
if git diff --cached --name-only | xargs ls -la | awk '{if($5 > 100000) print $9 " (" $5 " bytes)"}' | grep -q .; then
    echo "⚠️  Large files detected - consider if appropriate"
fi

# Check for mixed concerns
CHANGED_FILES=$(git diff --cached --name-only | wc -l)
if [ "$CHANGED_FILES" -gt 5 ]; then
    echo "⚠️  Many files changed - ensure single concern"
fi

# Check for secrets (basic)
if git diff --cached | grep -i -E "(password|secret|key|token)" | grep -v -E "(test|mock|example)"; then
    echo "🚨 Potential secrets detected - review carefully"
fi

echo "Ready to commit with: $ARGUMENTS"
```

### Commit Types Guide
```
✨ feat: new feature or enhancement
🐛 fix: bug fix or issue resolution
♻️  refactor: code restructuring without behavior change
✅ test: add, update, or fix tests
📚 docs: documentation changes
🔧 chore: maintenance, build, or tooling
🎨 style: formatting, whitespace, code style
⚡ perf: performance improvements
🔒 security: security-related changes
```

### Enhanced Commit Message
Create detailed commit message with context:
```bash
echo "Creating enhanced commit message for: $ARGUMENTS"
echo ""
echo "# Commit template:"
echo "type: brief description"
echo ""
echo "Detailed explanation of what changed and why."
echo "Reference any issues, discussions, or decision records."
echo ""
echo "🤖 Generated with [Claude Code](https://claude.ai/code)"
echo ""
echo "Co-Authored-By: Claude <noreply@anthropic.com>"
```

## Usage Examples:
- `/enhance-commit "feat: add user authentication"` - Commit with message
- `/enhance-commit validate` - Run pre-commit checks
- `/enhance-commit guide` - Show commit type guide
- `/enhance-commit template` - Generate commit message template

**🎯 Remember: One logical change per commit, commit immediately after completion.**