---
allowed-tools: [Read, Grep, Glob, Write, Edit, TodoWrite]
description: "시스템 아키텍처, API 및 컴포넌트 인터페이스 설계"
---

# /sc:design - System and Component Design

## Purpose
Design system architecture, APIs, component interfaces, and technical specifications.

## Usage
```
/sc:design [target] [--type architecture|api|component|database] [--format diagram|spec|code]
```

## Arguments
- `target` - System, component, or feature to design
- `--type` - Design type (architecture, api, component, database)
- `--format` - Output format (diagram, spec, code)
- `--iterative` - Enable iterative design refinement

## Execution
1. Analyze requirements and design constraints
2. Create initial design concepts and alternatives
3. Develop detailed design specifications
4. Validate design against requirements and best practices
5. Generate design documentation and implementation guides

## Claude Code Integration
- Uses Read for requirement analysis
- Leverages Write for design documentation
- Applies TodoWrite for design task tracking
- Maintains consistency with architectural patterns
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for complex system design tasks:

### Usage Scenarios
1. **System Architecture Analysis**
   ```bash
   # Complete analysis of existing architecture
   gemini -p "Analyze current system architecture and suggest improvements" src/
   
   # Microservice design analysis
   gemini -p "Analyze dependencies between services and suggest microservice separation strategies"
   ```

2. **API Design Review**
   ```bash
   # Complete API specification review
   gemini -p "Analyze OpenAPI specification and verify RESTful design principles compliance" api-spec.yaml
   
   # API version compatibility analysis
   gemini -p "Analyze API changes and find backward compatibility issues"
   ```

3. **Database Design**
   ```bash
   # Schema design review
   gemini -p "Analyze database schema and suggest normalization and performance optimization strategies" schema.sql
   ```

### Collaboration Strategy
- **Requirements Analysis**: Use Gemini to understand complete requirements
- **Design Creation**: Use Claude Code to create specific designs
- **Validation**: Review designs and iterative improvements