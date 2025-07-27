---
allowed-tools: [Read, Bash, Glob, TodoWrite, Edit]
description: "오류 처리 및 최적화를 통한 프로젝트 빌드, 컴파일 및 패키징"
---

# /sc:build - Project Building

## Purpose
Build, compile, and package projects with comprehensive error handling and optimization.

## Usage
```
/sc:build [target] [--type dev|prod|test] [--clean] [--optimize]
```

## Arguments
- `target` - Project or specific component to build
- `--type` - Build type (dev, prod, test)
- `--clean` - Clean build artifacts before building
- `--optimize` - Enable build optimizations
- `--verbose` - Enable detailed build output

## Execution
1. Analyze project structure and build configuration
2. Validate dependencies and environment setup
3. Execute build process with error monitoring
4. Handle build errors and provide diagnostic information
5. Optimize build output and report results

## Claude Code Integration
- Uses Bash for build command execution
- Leverages Read for build configuration analysis
- Applies TodoWrite for build progress tracking
- Maintains comprehensive error handling and reporting
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for complex build processes and large-scale projects:

### Usage Scenarios
1. **Build Configuration Analysis**
   ```bash
   # Complex build configuration understanding
   gemini -p "Analyze all settings in webpack.config.js and suggest optimization strategies"
   
   # Multi-module project build strategy
   gemini -p "Analyze build dependencies between all packages in monorepo" lerna.json
   ```

2. **Build Error Analysis**
   ```bash
   # Large build log analysis
   gemini -p "Find root cause from build failure logs" build.log
   
   # Dependency conflict resolution
   gemini -p "Analyze npm dependency conflicts and suggest solutions" package-lock.json
   ```

3. **Build Optimization**
   ```bash
   # Bundle size optimization
   gemini -p "Find optimization points from webpack bundle analysis results" stats.json
   ```

### Collaboration Strategy
- **Pre-analysis**: Use Gemini to understand complete build configuration
- **Problem Solving**: Use Claude Code to resolve specific build issues
- **Optimization**: Perform build performance improvement tasks