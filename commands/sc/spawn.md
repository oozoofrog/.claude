---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite, Edit, MultiEdit, Write]
description: "복잡한 작업을 효율적으로 실행하는 조정된 하위 작업으로 분해"
---

# /sc:spawn - Task Orchestration

## Purpose
Decompose complex requests into manageable subtasks and coordinate their execution.

## Usage
```
/sc:spawn [task] [--sequential|--parallel] [--validate]
```

## Arguments
- `task` - Complex task or project to orchestrate
- `--sequential` - Execute tasks in dependency order (default)
- `--parallel` - Execute independent tasks concurrently
- `--validate` - Enable quality checkpoints between tasks

## Execution
1. Parse request and create hierarchical task breakdown
2. Map dependencies between subtasks
3. Choose optimal execution strategy (sequential/parallel)
4. Execute subtasks with progress monitoring
5. Integrate results and validate completion

## Claude Code Integration
- Uses TodoWrite for task breakdown and tracking
- Leverages file operations for coordinated changes
- Applies efficient batching for related operations
- Maintains clear dependency management
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for complex task orchestration:

### Usage Scenarios
1. **Task Decomposition Strategy**
   ```bash
   # Break down complex tasks into subtasks
   gemini -p "Break down this complex feature into step-by-step tasks and set work order" requirements.md
   
   # Dependency analysis
   gemini -p "Analyze dependencies between tasks and find parallelizable parts"
   ```

2. **Resource Optimization**
   ```bash
   # Task priority determination
   gemini -p "Set task priorities considering resource constraints"
   
   # Bottleneck prediction
   gemini -p "Find expected bottlenecks during task execution and suggest countermeasures"
   ```

3. **Progress Monitoring**
   ```bash
   # Overall progress analysis
   gemini -p "Analyze current task progress and organize remaining work"
   
   # Quality checkpoint design
   gemini -p "Set quality verification criteria for each phase"
   ```

### Collaboration Strategy
- **Strategy Planning**: Use Gemini to establish complex task decomposition strategies
- **Execution Management**: Use Claude Code to perform accurate task execution and coordination
- **Progress Tracking**: Real-time progress monitoring and adjustment