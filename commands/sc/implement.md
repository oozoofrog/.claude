---
allowed-tools: [Read, Write, Edit, MultiEdit, Bash, Glob, TodoWrite, Task]
description: "지능적인 페르소나 활성화 및 MCP 통합을 통한 기능 및 코드 구현"
---

# /sc:implement - Feature Implementation

## Purpose
Implement features, components, and code functionality with intelligent expert activation and comprehensive development support.

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
1. Analyze implementation requirements and detect technology context
2. Auto-activate relevant personas (frontend, backend, security, etc.)
3. Coordinate with MCP servers (Magic for UI, Context7 for patterns, Sequential for complex logic)
4. Generate implementation code with best practices
5. Apply security and quality validation
6. Provide testing recommendations and next steps

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
/sc:implement user authentication system --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for user management --type api --safe
/sc:implement payment processing service --type service --iterative
```

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