---
allowed-tools: [Read, Grep, Glob, Bash, Edit, MultiEdit]
description: "코드 정리, 데드 코드 제거 및 프로젝트 구조 최적화"
---

# /sc:cleanup - Code and Project Cleanup

## Purpose
Systematically clean up code, remove dead code, optimize imports, and improve project structure.

## Usage
```
/sc:cleanup [target] [--type code|imports|files|all] [--safe|--aggressive]
```

## Arguments
- `target` - Files, directories, or entire project to clean
- `--type` - Cleanup type (code, imports, files, all)
- `--safe` - Conservative cleanup (default)
- `--aggressive` - More thorough cleanup with higher risk
- `--dry-run` - Preview changes without applying them

## Execution
1. Analyze target for cleanup opportunities
2. Identify dead code, unused imports, and redundant files
3. Create cleanup plan with risk assessment
4. Execute cleanup operations with appropriate safety measures
5. Validate changes and report cleanup results

## Claude Code Integration
- Uses Glob for systematic file discovery
- Leverages Grep for dead code detection
- Applies MultiEdit for batch cleanup operations
- Maintains backup and rollback capabilities
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale codebase cleanup tasks:

### Usage Scenarios
1. **Dead Code Detection**
   ```bash
   # Find unused code across entire project
   gemini -p "Find all unused functions, variables, and classes and organize them" src/
   
   # Detect duplicate code patterns
   gemini -p "Find duplicate code blocks and suggest refactoring strategies"
   ```

2. **Import Optimization**
   ```bash
   # Clean up unused imports
   gemini -p "Find unused imports in all files and suggest removal strategies"
   
   # Detect circular references
   gemini -p "Find import circular references and suggest solutions"
   ```

3. **Project Structure Cleanup**
   ```bash
   # Find empty directories and unnecessary files
   gemini -p "Find files and directories that need cleanup in the project"
   ```

### Collaboration Strategy
- **Phase 1**: Use Gemini to generate complete cleanup target list
- **Phase 2**: Use Claude Code to safely perform cleanup tasks
- **Phase 3**: Validate cleanup results and test