---
allowed-tools: [Read, Grep, Glob, Bash, Write]
description: "종합적인 프로젝트 문서화 및 지식 베이스 생성"
---

# /sc:index - Project Documentation

## Purpose
Create and maintain comprehensive project documentation, indexes, and knowledge bases.

## Usage
```
/sc:index [target] [--type docs|api|structure|readme] [--format md|json|yaml]
```

## Arguments
- `target` - Project directory or specific component to document
- `--type` - Documentation type (docs, api, structure, readme)
- `--format` - Output format (md, json, yaml)
- `--update` - Update existing documentation

## Execution
1. Analyze project structure and identify key components
2. Extract documentation from code comments and README files
3. Generate comprehensive documentation based on type
4. Create navigation structure and cross-references
5. Output formatted documentation with proper organization

## Claude Code Integration
- Uses Glob for systematic file discovery
- Leverages Grep for extracting documentation patterns
- Applies Write for creating structured documentation
- Maintains consistency with project conventions
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale project documentation:

### Usage Scenarios
1. **Complete Project Structure Analysis**
   ```bash
   # Complete project structure documentation
   gemini -p "Analyze complete project structure and write developer guide" . --exclude "node_modules,dist,build"
   
   # Auto-generate API documentation
   gemini -p "Analyze all API endpoints and generate API reference" routes/
   ```

2. **Knowledge Base Construction**
   ```bash
   # Code pattern documentation
   gemini -p "Find frequently used code patterns and write development guidelines" src/
   
   # Architecture documentation creation
   gemini -p "Analyze system architecture and write technical documentation"
   ```

3. **Documentation Updates**
   ```bash
   # Change-based documentation updates
   gemini -p "Analyze recent changes and update documentation" docs/
   
   # FAQ generation
   gemini -p "Generate frequently asked questions and answers through code analysis"
   ```

### Collaboration Strategy
- **Information Collection**: Use Gemini to collect complete project information
- **Document Creation**: Use Claude Code to create structured documentation
- **Quality Management**: Verify documentation consistency and accuracy