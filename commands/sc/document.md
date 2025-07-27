---
allowed-tools: [Read, Grep, Glob, Write, Edit]
description: "특정 컴포넌트 또는 기능에 대한 집중적인 문서화 생성"
---

# /sc:document - Focused Documentation

## Purpose
Generate precise, focused documentation for specific components, functions, or features.

## Usage
```
/sc:document [target] [--type inline|external|api|guide] [--style brief|detailed]
```

## Arguments
- `target` - Specific file, function, or component to document
- `--type` - Documentation type (inline, external, api, guide)
- `--style` - Documentation style (brief, detailed)
- `--template` - Use specific documentation template

## Execution
1. Analyze target component and extract key information
2. Identify documentation requirements and audience
3. Generate appropriate documentation based on type and style
4. Apply consistent formatting and structure
5. Integrate with existing documentation ecosystem

## Claude Code Integration
- Uses Read for deep component analysis
- Leverages Edit for inline documentation updates
- Applies Write for external documentation creation
- Maintains documentation standards and conventions
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale documentation tasks:

### Usage Scenarios
1. **Complete Project Documentation**
   ```bash
   # Document entire project structure
   gemini -p "Document the complete project structure and role of each module" src/
   
   # Auto-generate API documentation
   gemini -p "Analyze all API endpoints and generate OpenAPI specification" controllers/
   ```

2. **Technical Documentation Creation**
   ```bash
   # Generate Architecture Decision Records (ADR)
   gemini -p "Analyze code changes and write architecture decision documents"
   
   # Create developer guides
   gemini -p "Write onboarding guide for new developers"
   ```

3. **Code Comments and Documentation Updates**
   ```bash
   # Document complex functions
   gemini -p "Improve comments for functions containing complex algorithms" utils/
   ```

### Collaboration Strategy
- **Content Collection**: Use Gemini to collect and organize complete information
- **Document Creation**: Use Claude Code to create accurate documentation
- **Style Consistency**: Ensure documentation quality and consistency