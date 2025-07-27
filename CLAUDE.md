# SuperClaude Entry Point

@COMMANDS.md
@FLAGS.md
@PRINCIPLES.md
@RULES.md
@MCP.md
@PERSONAS.md
@ORCHESTRATOR.md
@MODES.md

# Language Preferences
- Always answer to Korean requests in Korean language

# Workflow Tips

## Gemini CLI 활용 가이드

### 대용량 토큰 작업 처리
너무 많은 토큰을 사용해야 하거나 거대한 컨텐츠를 읽어야 할 때, gemini CLI를 활용하여 효율적으로 처리합니다.

### 사용 시나리오
- **대용량 파일 분석**: `gemini -p "이 프로젝트의 전체 구조를 분석하고 요약해줘"`
- **로그 분석**: 수천 줄의 로그 파일 분석 시
- **전체 프로젝트 구조 파악**: 수백 개 파일의 프로젝트 분석 시
- **복잡한 의존성 분석**: 패키지 간 복잡한 관계 파악 시
- **대규모 리팩토링 계획**: 전체 코드베이스 개선 전략 수립 시

### 효과적인 협업 패턴
1. **분석 단계**: Gemini CLI로 대규모 분석 수행
2. **계획 단계**: Claude Code로 구체적 구현 계획 수립
3. **구현 단계**: Claude Code로 코드 작성 및 수정
4. **검증 단계**: Gemini CLI로 전체 변경사항 검토

### 토큰 효율화 전략
```bash
# 1. 사전 분석
gemini -p "src/ 디렉토리 구조와 주요 파일 목록을 정리해줘" > project_summary.md

# 2. 대용량 결과 처리
gemini -p "모든 테스트 결과를 분석하고 실패 원인을 정리해줘" | tee test_analysis.md
```

### 주의사항
- 10,000줄 이상의 파일은 gemini로 사전 분석 권장
- 민감한 정보(API 키, 비밀번호)가 포함된 파일은 주의
- Gemini와 Claude Code 간 컨텍스트는 수동으로 전달 필요