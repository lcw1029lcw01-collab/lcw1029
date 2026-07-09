# 06. DEVELOPMENT RULES — 개발 규칙

## 기본 원칙

1. **설계 우선** — 코드보다 설계 문서를 먼저 작성한다. 절대 코딩부터 시작하지 않는다.
2. **모듈화** — 엔진은 서로 독립적으로 교체 가능해야 한다.
3. **재사용성** — 모든 채널에서 사용할 수 있어야 한다.
4. **데이터 중심** — JSON/YAML로 엔진 간 통신. 규격은 `schemas/`에 정의.
5. **AI 친화적** — AI가 이해하기 쉽게 문서화한다.

## 매일 작업 사이클

```
Sprint → 문서 → 설계 → 검토 → Claude Code 구현 → 테스트 → Git Commit
```

- 한 문서를 완벽하게 만들고 다음으로 넘어간다.
- 작업이 끝나면 `PROJECT_STATE.md`와 `TASK.md`를 갱신한다.
- 규칙이 바뀌면 `CHANGELOG.md`에 **무엇을, 왜** 바꿨는지 기록한다.

## 상태 동기화 (매일 작업 시작 시 5분)

새 대화/세션의 첫 메시지는 항상 이 형식으로 시작한다:

```
ADOS Sprint 1 Day 3

현재 상태:
- Vision 완료
- README 완료
- Director Rule 60%

오늘 목표:
- Director Rule 완성
- Scene Schema 설계

주의사항:
- 영화 연출 우선
- Scene 중심 설계
- Prompt 직접 작성 금지
```

새로운 대화를 시작할 때는:

> "ADOS 프로젝트를 계속하자. docs/00_AI_CONTEXT.md부터 번호 순서로 읽고 이어가자."

## Git 규칙

- 커밋 메시지는 conventional commit 형식: `chore:`, `docs:`, `feat:`, `fix:`, `refactor:`
  - 예: `chore: initialize ADOS project structure`
- 매 작업 단위마다 커밋한다. GitHub는 ADOS Brain(기억)이다.
- 잘 만든 버전은 언제든 복구할 수 있도록 커밋 단위를 작게 유지한다.

## 문서 규칙

- `docs/` 번호(00~06)는 AI가 읽는 순서다. 순서를 바꾸지 않는다.
- 사람용 설명과 AI용 규칙을 구분해서 쓴다. AI용 규칙은 명시적·기계적으로.
- 문서는 한국어 기본, 기술 용어는 영어 (예: Scene, Director Engine).

## 설계 검증 4문 (통과 못 하면 만들지 않는다)

1. 확장성 — 채널 100개에도 그대로 쓸 수 있는가?
2. 유지보수성 — 1년 후에도 이해할 수 있는가?
3. 품질 — Netflix/BBC 수준을 목표로 하는가?
4. 자동화 — 사람의 직접 작업을 줄이는가?

## 버전 관리

```
ADOS v0.1  Sprint 1 설계 완료
ADOS v0.2  Story Engine
ADOS v0.3  Director Engine
ADOS v0.5  첫 자동 생성
ADOS v1.0  첫 번째 영화 완성
```
