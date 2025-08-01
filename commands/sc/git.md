---
allowed-tools: [Bash, Read, Glob, TodoWrite, Edit]
description: "지능적인 커밋 메시지 및 브랜치 관리를 통한 Git 작업"
---

# /sc:git - Git Operations

## Purpose
Execute Git operations with TDD and Tidy First commit discipline, ensuring proper separation of structural vs behavioral changes and maintaining small, frequent commits with clear commit messages.

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
- `--tdd` - Apply TDD commit discipline (tests must pass)
- `--tidy-first` - Separate structural vs behavioral commits
- `--structural` - Mark commit as structural change only
- `--behavioral` - Mark commit as behavioral change only

## Execution
1. **Commit Discipline Check**: Verify all tests pass and build succeeds
2. **Change Categorization**: Identify structural vs behavioral changes
3. **Commit Message Generation**: Create clear, descriptive commit messages
4. **Small Commit Strategy**: Maintain small, frequent commits
5. **Validation**: Ensure Xcode build succeeds with no linter warnings

## TDD Commit Guidelines
- **All Tests Passing**: Only commit when all tests are green
- **Build Success**: Ensure Xcode build succeeds with no SwiftLint warnings
- **Single Logical Unit**: Each commit represents one logical change
- **Clear Messages**: Commit messages clearly state Structural vs Behavioral
- **Small Commits**: Favor small, frequent commits over large batches

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