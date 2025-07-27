---
allowed-tools: [Read, Grep, Glob, Bash]
description: "코드, 개념 또는 시스템 동작에 대한 명확한 설명 제공"
---

# /sc:explain - Code and Concept Explanation

## Purpose
Deliver clear, comprehensive explanations of code functionality, concepts, or system behavior.

## Usage
```
/sc:explain [target] [--level basic|intermediate|advanced] [--format text|diagram|examples]
```

## Arguments
- `target` - Code file, function, concept, or system to explain
- `--level` - Explanation complexity (basic, intermediate, advanced)
- `--format` - Output format (text, diagram, examples)
- `--context` - Additional context for explanation

## Execution
1. Analyze target code or concept thoroughly
2. Identify key components and relationships
3. Structure explanation based on complexity level
4. Provide relevant examples and use cases
5. Present clear, accessible explanation with proper formatting

## Claude Code Integration
- Uses Read for comprehensive code analysis
- Leverages Grep for pattern identification
- Applies Bash for runtime behavior analysis
- Maintains clear, educational communication style
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for complex concept explanation tasks:

### Usage Scenarios
1. **Complete System Understanding**
   ```bash
   # Complete system structure explanation
   gemini -p "Explain the complete system structure and operation principles in a way beginners can understand" src/
   
   # Complex business logic explanation
   gemini -p "Explain core business logic flow step by step" business/
   ```

2. **Technology Stack Analysis**
   ```bash
   # Explain roles of used technologies
   gemini -p "Explain the role and selection rationale of all technology stacks used in the project"
   
   # Architecture pattern explanation
   gemini -p "Explain applied architecture patterns with examples"
   ```

3. **Problem Solving Process Explanation**
   ```bash
   # Debugging process explanation
   gemini -p "Explain the cause of this bug and detailed resolution process" logs/
   ```

### Collaboration Strategy
- **Context Understanding**: Use Gemini to collect complete context and background information
- **Detailed Explanation**: Use Claude Code to provide accurate and clear explanations
- **Educational Materials**: Generate learning examples and practice materials