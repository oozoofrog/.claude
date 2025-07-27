---
allowed-tools: [Read, Grep, Glob, Bash]
description: "작업, 기능 또는 프로젝트에 대한 개발 추정 제공"
---

# /sc:estimate - Development Estimation

## Purpose
Generate accurate development estimates for tasks, features, or projects based on complexity analysis.

## Usage
```
/sc:estimate [target] [--type time|effort|complexity|cost] [--unit hours|days|weeks]
```

## Arguments
- `target` - Task, feature, or project to estimate
- `--type` - Estimation type (time, effort, complexity, cost)
- `--unit` - Time unit for estimates (hours, days, weeks)
- `--breakdown` - Provide detailed breakdown of estimates

## Execution
1. Analyze scope and requirements of target
2. Identify complexity factors and dependencies
3. Apply estimation methodologies and historical data
4. Generate estimates with confidence intervals
5. Present detailed breakdown with risk factors

## Claude Code Integration
- Uses Read for requirement analysis
- Leverages Glob for codebase complexity assessment
- Applies Grep for pattern-based estimation
- Maintains structured estimation documentation
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for complex project estimation tasks:

### Usage Scenarios
1. **Project Scale Analysis**
   ```bash
   # Complete codebase complexity analysis
   gemini -p "Analyze overall complexity of the project and estimate development effort" src/
   
   # Feature complexity evaluation
   gemini -p "Evaluate complexity of each module and set development priorities"
   ```

2. **Refactoring Cost Estimation**
   ```bash
   # Legacy code improvement cost
   gemini -p "Analyze technical debt in legacy code and estimate improvement costs" legacy/
   
   # Migration work estimation
   gemini -p "Estimate effort required for migration to new framework"
   ```

3. **Performance Improvement Estimation**
   ```bash
   # Performance optimization workload
   gemini -p "Analyze performance bottlenecks and estimate optimization time"
   ```

### Collaboration Strategy
- **Scope Understanding**: Use Gemini to analyze complete work scope
- **Detailed Estimation**: Use Claude Code to calculate accurate effort
- **Risk Assessment**: Identify uncertainty factors and mitigation strategies