---
allowed-tools: [Read, Grep, Write, Edit]
description: "인터랙티브 요소 번호 매기기를 통한 ASCII 와이어프레임 생성"
---

# /sc:wireframe - ASCII Wireframe Generation

## Purpose
Generate ASCII wireframes with interactive element numbering for UI layouts, components, and screen designs.

## Usage
```
/sc:wireframe @<file-path> [--type layout|component|screen] [--interactive] [--detailed]
```

## Arguments
- `@<file-path>` - Path to component or design specification file
- `--type` - Wireframe type (layout, component, screen)
- `--interactive` - Add numbered interactive elements
- `--detailed` - Include detailed element specifications
- `--ascii-style` - ASCII art style (simple, detailed, boxed)

## Execution
1. Analyze existing component or design specifications
2. Extract layout structure and element hierarchy
3. Generate ASCII wireframe with proper spacing and alignment
4. Add interactive element numbering if requested
5. Include element specifications and interaction notes

## Claude Code Integration
- Uses Read for component analysis and structure understanding
- Leverages Grep for pattern matching in existing designs
- Applies Write for wireframe output generation
- Maintains consistency with design system patterns
- Auto-activates Frontend and Architect personas
- Answer to Korean always

## Auto-Activation Patterns
- **Frontend Persona**: UI component analysis, responsive design considerations
- **Architect Persona**: Layout structure, system design patterns
- **MCP Integration**: Magic (UI analysis), Sequential (structure analysis)

## Examples
```
/sc:wireframe @src/components/Dashboard.jsx --type component --interactive
/sc:wireframe @designs/login-page.md --type screen --detailed
/sc:wireframe @layouts/main-layout.vue --type layout --ascii-style boxed
```

## Output Format
- ASCII art representation of UI structure
- Numbered interactive elements (buttons, inputs, links)
- Element specifications and interaction notes
- Responsive breakpoint considerations
- Design system component references

## Gemini CLI Integration
Leverage Gemini CLI for complex wireframe analysis:

### Usage Scenarios
1. **Design System Analysis**
   ```bash
   # Complete component library analysis
   gemini -p "Analyze all components and extract common layout patterns" src/components/
   
   # Design consistency review
   gemini -p "Analyze wireframes and identify design pattern inconsistencies"
   ```

2. **User Flow Wireframing**
   ```bash
   # Multi-screen flow analysis
   gemini -p "Analyze user flow and suggest optimal screen layout sequences"
   
   # Interaction pattern mapping
   gemini -p "Map user interactions across screens and suggest wireframe improvements"
   ```

3. **Accessibility Wireframing**
   ```bash
   # Accessibility structure analysis
   gemini -p "Analyze wireframe for accessibility compliance and suggest improvements"
   ```

### Collaboration Strategy
- **Design Analysis**: Use Gemini to understand complex design requirements
- **Wireframe Generation**: Use Claude Code to create precise ASCII wireframes
- **Pattern Validation**: Review wireframes against design system consistency