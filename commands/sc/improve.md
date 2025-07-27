---
allowed-tools: [Read, Grep, Glob, Edit, MultiEdit, TodoWrite]
description: "코드 품질, 성능 및 유지보수성에 대한 체계적인 개선 적용"
---

# /sc:improve - Code Improvement

## Purpose
Apply systematic improvements to code quality, performance, maintainability, and best practices.

## Usage
```
/sc:improve [target] [--type quality|performance|maintainability|style] [--safe]
```

## Arguments
- `target` - Files, directories, or project to improve
- `--type` - Improvement type (quality, performance, maintainability, style)
- `--safe` - Apply only safe, low-risk improvements
- `--preview` - Show improvements without applying them

## Execution
1. Analyze code for improvement opportunities
2. Identify specific improvement patterns and techniques
3. Create improvement plan with risk assessment
4. Apply improvements with appropriate validation
5. Verify improvements and report changes

## Claude Code Integration
- Uses Read for comprehensive code analysis
- Leverages MultiEdit for batch improvements
- Applies TodoWrite for improvement tracking
- Maintains safety and validation mechanisms
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale code improvement tasks:

### Usage Scenarios
1. **Complete Code Quality Analysis**
   ```bash
   # Complete project quality assessment
   gemini -p "Analyze overall code quality of the project and suggest improvement priorities" src/
   
   # Technical debt assessment
   gemini -p "Analyze technical debt and suggest resolution roadmap"
   ```

2. **Performance Optimization Analysis**
   ```bash
   # Performance bottleneck detection
   gemini -p "Find code patterns that may become performance bottlenecks and suggest optimization strategies"
   
   # Memory usage analysis
   gemini -p "Find code with potential memory leaks and suggest improvement strategies"
   ```

3. **Maintainability Improvement**
   ```bash
   # Complexity analysis
   gemini -p "Find functions with high complexity and suggest refactoring strategies"
   
   # Dependency improvement
   gemini -p "Find modules with strong coupling and suggest dependency improvement strategies"
   ```

### Collaboration Strategy
- **Problem Identification**: Use Gemini to discover complete improvement points
- **Improvement Application**: Use Claude Code to safely perform improvement tasks
- **Result Validation**: Measure and verify improvement effects