---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite]
description: "코드 품질, 보안, 성능 및 아키텍처 분석"
---

# /sc:analyze - Code Analysis

## Purpose
Execute comprehensive code analysis with Swift-specific focus, emphasizing TDD compliance, Tidy First principles, and Swift best practices including Protocol-Oriented Programming and value types.

## Usage
```
/sc:analyze [target] [--focus quality|security|performance|architecture] [--depth quick|deep]
```

## Arguments
- `target` - Files, directories, or project to analyze
- `--focus` - Analysis focus area (quality, security, performance, architecture)
- `--depth` - Analysis depth (quick, deep)
- `--format` - Output format (text, json, report)
- `--tdd` - Analyze TDD compliance and test coverage
- `--tidy-first` - Analyze structural vs behavioral change separation
- `--swift` - Apply Swift-specific analysis patterns and best practices

## Execution
1. **TDD Compliance Analysis**: Check test coverage and Red → Green → Refactor cycles
2. **Tidy First Assessment**: Analyze structural vs behavioral change separation
3. **Swift Best Practices**: Evaluate Protocol-Oriented Programming, value types usage
4. **Code Quality Metrics**: Assess duplication, complexity, and maintainability
5. **Comprehensive Reporting**: Present findings with Swift-specific recommendations

## Swift-Specific Analysis Guidelines
- **Value Types**: Prefer structs/enums over classes when possible
- **Functional Programming**: Use map, flatMap, compactMap, ?? for optionals
- **Protocol-Oriented**: Leverage protocols for dependency injection
- **Error Handling**: Use Result combinators (map, flatMap, get())
- **Async Code**: Test with XCTestExpectation or async tests

## Claude Code Integration
- Uses Glob for systematic file discovery
- Leverages Grep for pattern-based analysis
- Applies Read for deep code inspection
- Maintains structured analysis reporting
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for token efficiency in large-scale analysis tasks:

### Usage Scenarios
1. **Full Project Analysis**
   ```bash
   # Large-scale project structure analysis
   gemini -p "Analyze code quality and architecture across the entire project" src/
   
   # Complete security vulnerability scan
   gemini -p "Find security vulnerabilities across all files and organize them" --include "*.js,*.py"
   ```

2. **Dependency Analysis**
   ```bash
   # Complex dependency relationship analysis
   gemini -p "Analyze dependencies between packages and find circular references" package.json
   ```

3. **Performance Bottleneck Analysis**
   ```bash
   # Large log file analysis
   gemini -p "Analyze performance logs to identify bottleneck points" logs/performance.log
   ```

### Collaboration Strategy
- **Phase 1**: Use Gemini for full project scan and issue list generation
- **Phase 2**: Use Claude Code for deep analysis of specific issues
- **Phase 3**: Establish improvement plan based on analysis results