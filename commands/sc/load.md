---
allowed-tools: [Read, Grep, Glob, Bash, Write]
description: "프로젝트 컨텍스트, 구성 및 종속성 로드 및 분석"
---

# /sc:load - Project Context Loading

## Purpose
Load and analyze project context, configurations, dependencies, and environment setup.

## Usage
```
/sc:load [target] [--type project|config|deps|env] [--cache]
```

## Arguments
- `target` - Project directory or specific configuration to load
- `--type` - Loading type (project, config, deps, env)
- `--cache` - Cache loaded context for faster subsequent access
- `--refresh` - Force refresh of cached context

## Execution
1. Discover and analyze project structure and configuration files
2. Load dependencies, environment variables, and settings
3. Parse and validate configuration consistency
4. Create comprehensive project context map
5. Cache context for efficient future access

## Claude Code Integration
- Uses Glob for comprehensive project discovery
- Leverages Read for configuration analysis
- Applies Bash for environment validation
- Maintains efficient context caching mechanisms
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale project context loading:

### Usage Scenarios
1. **Complete Project Analysis**
   ```bash
   # Large-scale project structure understanding
   gemini -p "Analyze complete project structure and key configuration files" . --include "*.json,*.yaml,*.toml,*.config.*"
   
   # Complete dependency analysis
   gemini -p "Analyze all package dependencies and find potential conflicts" package*.json requirements.txt
   ```

2. **Environment Configuration Analysis**
   ```bash
   # Environment variables and configuration analysis
   gemini -p "Analyze all environment configuration files and find missing settings" .env* config/
   
   # Build configuration optimization
   gemini -p "Analyze build configurations and suggest performance improvements" webpack.config.* vite.config.*
   ```

3. **Project Status Diagnosis**
   ```bash
   # Complete project health check
   gemini -p "Diagnose overall project status and find improvement points"
   
   # Compatibility verification
   gemini -p "Find version compatibility issues and suggest solutions"
   ```

### Collaboration Strategy
- **Comprehensive Scanning**: Use Gemini to understand complete project context
- **Precise Loading**: Use Claude Code to load specific configurations
- **Status Validation**: Verify validity of loaded context