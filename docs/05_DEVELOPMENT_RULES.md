# ADOS Development Rules

Version: 0.2.0

---

# 기본 원칙

1. **요구사항 → 설계 → 구현 → 테스트** 순서로 간다. (실제 소프트웨어 회사 방식)
2. **설계 우선** — 코드보다 설계 문서를 먼저 작성한다. 절대 코딩부터 시작하지 않는다.
3. **모듈화** — 모듈은 서로 독립적으로 교체 가능해야 한다. Provider 교체 시 Engine은 수정하지 않는다.
4. **데이터 중심** — JSON으로 모듈 간 통신. 규격은 `schemas/`에 정의.
5. **YAGNI** — You Aren't Gonna Need It. **지금 필요하지 않은 것은 만들지 않는다.**
6. **문서는 코드보다 중요하다** — 좋은 문서는 Claude Code, Codex, ChatGPT, 미래의 AI 모두 사용할 수 있다.

# 문서 레벨

코드는 제일 마지막이다.

```
Level 0  System Prompt (철학)
Level 1  Project Charter (헌법)
Level 2  Architecture (구조)
Level 3  Bibles (제작 규칙)
Level 4  Code (구현)
```

# 문서 작성 형식 (Spec 형식)

모든 핵심 문서는 설명서가 아니라 **Software Specification**으로 작성한다.
Claude Code가 가장 잘 읽는 형식이다.

```
Purpose          — 이 문서/모듈은 왜 존재하는가
Scope            — 무엇을 포함하고 무엇을 포함하지 않는가
Inputs           — 입력
Outputs          — 출력
Constraints      — 제약 조건
Examples         — 예제
Acceptance Criteria — 완료 기준
```

- 애매한 표현 금지
- 구현 가능한 수준의 정의
- 입력/출력 명시
- 완료 기준 포함

# 문서를 만들기 전 자문 4문

- 이 문서가 정말 필요한가?
- 기존 문서에 넣을 수는 없는가?
- AI가 읽기 쉬운가?
- 1년 후에도 이해할 수 있는가?

**좋은 문서 20개가 나쁜 문서 100개보다 훨씬 가치 있다.**

# ADR (Architecture Decision Record)

중요한 설계 결정은 `docs/adr/ADR-XXXX.md`로 기록한다.

- 아키텍처 확정 후 변경은 ADR에 기록할 정도로 신중하게만 한다.
- 형식: 결정 / 이유 / 날짜 / 상태

# 매일 작업 사이클

```
요구사항 → 설계 → 검토(설계 리뷰) → Claude Code 구현 → 테스트 → Git Commit
```

- 한 문서를 완벽하게 만들고 다음으로 넘어간다.
- 작업이 끝나면 `docs/01_AI_CONTEXT.md`(현재 상태)와 `TASK.md`를 갱신한다.
- 규칙이 바뀌면 `CHANGELOG.md`에 **무엇을, 왜** 바꿨는지 기록한다.
- **매주 금요일은 개발을 멈추고 "설계 리뷰"만 하는 날**이다. 잘못된 설계를 빨리 고치는 것이 코드를 많이 쓰는 것보다 중요하다.

# 상태 동기화 (매일 작업 시작 시 5분)

새 대화/세션의 첫 메시지는 항상 이 형식으로 시작한다:

```
ADOS Sprint 1 Day 3

현재 상태:
- System Prompt 완료
- Architecture 완료

오늘 목표:
- Data Flow 설계

주의사항:
- 영화 연출 우선 / Scene 중심 / Prompt 직접 작성 금지
```

새로운 대화를 시작할 때는:

> "ADOS 프로젝트를 계속하자. docs/00_SYSTEM_PROMPT.md부터 번호 순서로 읽고 이어가자."

# Git 규칙

- 커밋 메시지는 conventional commit 형식: `chore:`, `docs:`, `feat:`, `fix:`, `refactor:`
- 매 작업 단위마다 커밋한다. GitHub는 ADOS Brain(기억)이다.
- 커밋 단위를 작게 유지해 언제든 복구 가능하게 한다.

# 언어 규칙

- 문서는 **한국어 기본**, 기술 용어만 영어. 예: Story Engine (스토리 엔진)
- 파일·폴더명은 영어 (GPT 설계 원안 유지)

# 설계 검증 4문 (통과 못 하면 만들지 않는다)

1. 확장성 — 채널 100개에도 그대로 쓸 수 있는가?
2. 유지보수성 — 1년 후에도 이해할 수 있는가?
3. 품질 — Netflix/BBC 수준을 목표로 하는가?
4. 자동화 — 사람의 직접 작업을 줄이는가?
