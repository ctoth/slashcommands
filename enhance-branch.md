---
description: "Branch management utilities for feature development"
tools: ["Bash", "Read"]
---

# Branch Management Utilities

Branch operation: **$ARGUMENTS**

## Available Operations

### Create Feature Branch
```bash
# Sanitize feature name and create branch
FEATURE_NAME=$(echo "$ARGUMENTS" | tr ' ' '-' | tr '[:upper:]' '[:lower:]' | sed 's/[^a-z0-9-]//g')
git checkout -b "feature/$FEATURE_NAME"
echo "✅ Created feature branch: feature/$FEATURE_NAME"
```

### Create Quick Branch
```bash
FEATURE_NAME=$(echo "$ARGUMENTS" | tr ' ' '-' | tr '[:upper:]' '[:lower:]' | sed 's/[^a-z0-9-]//g')
git checkout -b "quick/$FEATURE_NAME"
echo "✅ Created quick branch: quick/$FEATURE_NAME"
```

### Branch Status
```bash
echo "📍 Current branch: $(git branch --show-current)"
echo "📊 Branch status:"
git status --porcelain
echo "📝 Recent commits:"
git log --oneline -5
```

### List Enhancement Branches
```bash
echo "🌿 Enhancement branches:"
git branch | grep -E "(feature/|quick/|enhance/)" | sort
```

### Clean Merged Branches
```bash
echo "🧹 Cleaning merged enhancement branches..."
git branch --merged | grep -E "(feature/|quick/)" | xargs -r git branch -d
echo "✅ Cleanup complete"
```

## Usage Examples:
- `/enhance-branch status` - Show current branch info
- `/enhance-branch list` - List all enhancement branches  
- `/enhance-branch clean` - Remove merged branches
- `/enhance-branch create my-feature` - Create feature/my-feature branch