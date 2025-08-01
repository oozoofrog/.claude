---
allowed-tools: [Read, Write, Edit, MultiEdit, Bash, Glob, TodoWrite, Task]
description: "지능적인 페르소나 활성화 및 MCP 통합을 통한 기능 및 코드 구현"
---

# /sc:implement - Feature Implementation

## Purpose
Implement features, components, and code functionality with TDD (Test-Driven Development) and Tidy First principles, ensuring high-quality Swift code through systematic Red → Green → Refactor cycles.

## Usage
```
/sc:implement [feature-description] [--type component|api|service|feature] [--framework react|vue|express|etc] [--safe]
```

## Arguments
- `feature-description` - Description of what to implement
- `--type` - Implementation type (component, api, service, feature, module)
- `--framework` - Target framework or technology stack
- `--safe` - Use conservative implementation approach
- `--iterative` - Enable iterative development with validation steps
- `--with-tests` - Include test implementation
- `--documentation` - Generate documentation alongside implementation

## Execution
1. **TDD Cycle Initiation**: Write failing test for smallest behavior increment
2. **Red Phase**: Ensure test fails with clear, descriptive failure message
3. **Green Phase**: Implement minimum code to make test pass (no more)
4. **Refactor Phase**: Apply Tidy First principles (structural changes only)
5. **Commit Discipline**: Separate structural vs behavioral commits
6. **Repeat**: Continue TDD cycle for next behavior increment

## TDD Workflow Integration
- **Test-First Approach**: Always write test before implementation
- **Descriptive Test Names**: Use XCTest with clear naming (e.g., `testSumOfTwoPositiveNumbers_returnsCorrectResult`)
- **Minimal Implementation**: Write only code needed to pass current test
- **Swift Best Practices**: Use structs/enums over classes, functional chaining, Result combinators
- **Dependency Management**: Explicit dependency injection through protocols

## Claude Code Integration
- Uses Write/Edit/MultiEdit for code generation and modification
- Leverages Read and Glob for codebase analysis and context understanding
- Applies TodoWrite for implementation progress tracking
- Integrates Task tool for complex multi-step implementations
- Coordinates with MCP servers for specialized functionality
- Auto-activates appropriate personas based on implementation type
- Answer to Korean always

## Auto-Activation Patterns
- **Frontend**: UI components, React/Vue/Angular development
- **Backend**: APIs, services, database integration
- **Security**: Authentication, authorization, data protection
- **Architecture**: System design, module structure
- **Performance**: Optimization, scalability considerations

## Examples
```
/sc:implement user authentication system --type feature --tdd --swift
/sc:implement calculator service --type service --tdd --swift
/sc:implement data model --type model --tdd --swift
/sc:implement network layer --type service --tdd --swift
```

## TDD-Specific Arguments
- `--tdd` - Enable strict TDD workflow (Red → Green → Refactor)
- `--swift` - Apply Swift-specific best practices and patterns
- `--tidy-first` - Follow Tidy First principles (structural/behavioral separation)
- `--test-only` - Write tests only, no implementation
- `--refactor-only` - Apply refactoring to existing code

## Gemini CLI Integration
Leverage Gemini CLI for complex feature implementation:

### Usage Scenarios
1. **Feature Requirements Analysis**
   ```bash
   # Complete system structure understanding
   gemini -p "Analyze all components and dependencies needed to implement this feature" src/
   
   # Similar pattern exploration
   gemini -p "Find similar patterns in existing code and suggest reusable parts"
   ```

2. **Architecture Decisions**
   ```bash
   # Design pattern recommendations
   gemini -p "Suggest optimal architecture patterns for this feature based on existing codebase analysis"
   
   # Performance considerations
   gemini -p "Suggest optimization strategies for large-scale data processing"
   ```

3. **Implementation Strategy Planning**
   ```bash
   # Step-by-step implementation plan
   gemini -p "Break down complex features into step-by-step implementation plans"
   
   # Test strategy
   gemini -p "Design test cases for comprehensive test coverage of this feature"
   ```

### Collaboration Strategy
- **Pre-analysis**: Use Gemini to analyze requirements and architecture
- **Code Implementation**: Use Claude Code to implement accurate features
- **Quality Validation**: Verify quality and performance of implemented code