---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite]
description: "코드 품질, 보안, 성능 및 아키텍처 분석"
---

# /sc:analyze - Code Analysis

## Purpose
Execute comprehensive code analysis across quality, security, performance, and architecture domains.

## Usage
```
/sc:analyze [target] [--focus quality|security|performance|architecture] [--depth quick|deep]
```

## Arguments
- `target` - Files, directories, or project to analyze
- `--focus` - Analysis focus area (quality, security, performance, architecture)
- `--depth` - Analysis depth (quick, deep)
- `--format` - Output format (text, json, report)

## Execution
1. Discover and categorize files for analysis
2. Apply appropriate analysis tools and techniques
3. Generate findings with severity ratings
4. Create actionable recommendations with priorities
5. Present comprehensive analysis report

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