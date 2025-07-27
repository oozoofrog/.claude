---
allowed-tools: [Read, Bash, Glob, TodoWrite, Edit, Write]
description: "테스트 실행, 테스트 보고서 생성 및 테스트 커버리지 유지"
---

# /sc:test - Testing and Quality Assurance

## Purpose
Execute tests, generate comprehensive test reports, and maintain test coverage standards.

## Usage
```
/sc:test [target] [--type unit|integration|e2e|all] [--coverage] [--watch]
```

## Arguments
- `target` - Specific tests, files, or entire test suite
- `--type` - Test type (unit, integration, e2e, all)
- `--coverage` - Generate coverage reports
- `--watch` - Run tests in watch mode
- `--fix` - Automatically fix failing tests when possible

## Execution
1. Discover and categorize available tests
2. Execute tests with appropriate configuration
3. Monitor test results and collect metrics
4. Generate comprehensive test reports
5. Provide recommendations for test improvements

## Claude Code Integration
- Uses Bash for test execution and monitoring
- Leverages Glob for test discovery
- Applies TodoWrite for test result tracking
- Maintains structured test reporting and coverage analysis
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale test analysis and strategy planning:

### Usage Scenarios
1. **Test Coverage Analysis**
   ```bash
   # Complete test coverage analysis
   gemini -p "Analyze all test files and find areas with insufficient coverage" tests/
   
   # Test quality evaluation
   gemini -p "Analyze test code quality and suggest improvement strategies"
   ```

2. **Test Strategy Planning**
   ```bash
   # Test pyramid analysis
   gemini -p "Analyze current test structure and suggest optimal test pyramid"
   
   # E2E test scenario design
   gemini -p "Analyze user journeys and design E2E test scenarios" user-stories/
   ```

3. **Test Performance Optimization**
   ```bash
   # Test execution time analysis
   gemini -p "Analyze test execution time and suggest optimization strategies" test-results/
   
   # Flaky test detection
   gemini -p "Find unstable tests and suggest stabilization strategies"
   ```

### Collaboration Strategy
- **Strategy Analysis**: Use Gemini to analyze complete test strategies and coverage
- **Test Execution**: Use Claude Code to perform accurate test execution and monitoring
- **Result Analysis**: Interpret test results and derive improvement strategies