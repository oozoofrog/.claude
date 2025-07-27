---
allowed-tools: [Bash, Read, Glob, TodoWrite, Edit]
description: "지능적인 커밋 메시지 및 브랜치 관리를 통한 Git 작업"
---

# /sc:git - Git Operations

## Purpose
Execute Git operations with intelligent commit messages, branch management, and workflow optimization.

## Usage
```
/sc:git [operation] [args] [--smart-commit] [--branch-strategy]
```

## Arguments
- `operation` - Git operation (add, commit, push, pull, merge, branch, status)
- `args` - Operation-specific arguments
- `--smart-commit` - Generate intelligent commit messages
- `--branch-strategy` - Apply branch naming conventions
- `--interactive` - Interactive mode for complex operations

## Execution
1. Analyze current Git state and repository context
2. Execute requested Git operations with validation
3. Apply intelligent commit message generation
4. Handle merge conflicts and branch management
5. Provide clear feedback and next steps

## Claude Code Integration
- Uses Bash for Git command execution
- Leverages Read for repository analysis
- Applies TodoWrite for operation tracking
- Maintains Git best practices and conventions
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale Git history analysis and complex Git operations:

### Usage Scenarios
1. **Commit History Analysis**
   ```bash
   # Complete Git history analysis
   gemini -p "Analyze commit history from the past 6 months and find development patterns" --exec "git log --since='6 months ago' --pretty=format:'%h %an %s' --stat"
   
   # Branch strategy analysis
   gemini -p "Analyze branch structure and suggest Git workflow improvements" --exec "git branch -a"
   ```

2. **Conflict Resolution Support**
   ```bash
   # Complex merge conflict analysis
   gemini -p "Analyze files with merge conflicts and suggest resolution strategies" conflict-files/
   
   # Rebase strategy planning
   gemini -p "Predict conflicts that may occur during rebase and suggest countermeasures"
   ```

3. **Release Preparation**
   ```bash
   # Release note generation
   gemini -p "Analyze changes since last release and write release notes" CHANGELOG.md
   
   # Tag strategy analysis
   gemini -p "Analyze existing tag patterns and suggest version management strategies"
   ```

### Collaboration Strategy
- **History Analysis**: Use Gemini to analyze large-scale Git logs
- **Operation Execution**: Use Claude Code to perform accurate Git operations
- **Conflict Resolution**: Handle complex merge scenarios