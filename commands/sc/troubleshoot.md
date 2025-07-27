---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite]
description: "코드, 빌드 또는 시스템 동작의 문제 진단 및 해결"
---

# /sc:troubleshoot - Issue Diagnosis and Resolution

## Purpose
Systematically diagnose and resolve issues in code, builds, deployments, or system behavior.

## Usage
```
/sc:troubleshoot [issue] [--type bug|build|performance|deployment] [--trace]
```

## Arguments
- `issue` - Description of the problem or error message
- `--type` - Issue category (bug, build, performance, deployment)
- `--trace` - Enable detailed tracing and logging
- `--fix` - Automatically apply fixes when safe

## Execution
1. Analyze issue description and gather initial context
2. Identify potential root causes and investigation paths
3. Execute systematic debugging and diagnosis
4. Propose and validate solution approaches
5. Apply fixes and verify resolution

## Claude Code Integration
- Uses Read for error log analysis
- Leverages Bash for runtime diagnostics
- Applies Grep for pattern-based issue detection
- Maintains structured troubleshooting documentation
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for complex issue diagnosis:

### Usage Scenarios
1. **Large-Scale Log Analysis**
   ```bash
   # Error log pattern analysis
   gemini -p "Find common patterns in error logs and analyze root causes" logs/error.log
   
   # System performance log analysis
   gemini -p "Analyze performance logs to find bottleneck points" logs/performance.log
   ```

2. **Complete System Diagnosis**
   ```bash
   # Complete system status analysis
   gemini -p "Diagnose overall system status and find potential issues" . --include "*.log,*.json,config/*"
   
   # Dependency conflict analysis
   gemini -p "Analyze dependency conflict issues and suggest solutions" package*.json
   ```

3. **Problem Resolution Strategy**
   ```bash
   # Similar problem pattern search
   gemini -p "Find similar issues in past history and suggest resolution strategies" issues/
   
   # Debugging strategy planning
   gemini -p "Establish systematic debugging strategies for complex bugs"
   ```

### Collaboration Strategy
- **Problem Analysis**: Use Gemini to discover patterns in large-scale data
- **Diagnosis Execution**: Use Claude Code to perform accurate debugging and diagnosis
- **Resolution Verification**: Establish prevention measures after problem resolution