# ADOS Roadmap

Version: 0.2.0

> 원칙: 한 문서를 완벽하게 만들고 다음으로 넘어간다.
> 좋은 아이디어라도 구현 난이도가 너무 높으면 v2.0으로 미룬다.

---

# 3단계 전략 (전체 그림)

## Phase 1 (4~6주)

**목표: 첫 번째 채널이 실제로 성장할 수 있는 시스템**

- 주제 입력 → 리서치 → 대본 → 씬 분할 → 이미지 프롬프트 → 영상 프롬프트 → 음성 → 자막
- 👉 **사람이 최종 검토 후 업로드**

## Phase 2

- 자동 편집 / 자동 썸네일 / 자동 SEO / 자동 업로드

## Phase 3

- 채널 10개 / 언어 20개 / 완전 자동 운영

---

# 개발 순서 (모듈 단위)

| 단계 | 내용 | 상태 |
|------|------|------|
| Phase 0 | 제품 정의 (설계 문서 완성) | 🔄 진행 중 |
| Phase 1 | Story Engine | 예정 |
| Phase 2 | Director Engine | 예정 |
| Phase 3 | Scene Engine | 예정 |
| Phase 4 | Visual Engine | 예정 |
| Phase 5 | Automation | 예정 |

---

# Sprint 1 — 설계 (진행 중)

| 항목 | 상태 |
|------|------|
| 프로젝트 생성 (repo, 폴더, 첫 커밋) | ✅ |
| 00_SYSTEM_PROMPT.md | ✅ |
| 01_AI_CONTEXT.md | ✅ |
| 02_PROJECT_CHARTER.md | ✅ |
| 03_ARCHITECTURE.md (v1.0 확정) | ✅ |
| 04_DATA_FLOW.md | 🔄 초안 |
| 04_QUALITY_SYSTEM.md (좋은 영상의 시스템적 정의) | ⏳ GPT 설계 예정 |
| Story Bible / Director Bible 보강 (95점 수준) | ⏳ |
| Schema 확정 | 🔄 v0.1 |

## ADOS의 핵심 자산 (공들여 설계할 4가지)

1. Story Bible
2. Director Bible
3. Quality System
4. Style Memory

---

# 버전 마일스톤

| 버전 | 내용 |
|------|------|
| v0.1 | 프로젝트 기반 + 설계 문서 초안 |
| v0.2 | 아키텍처 v1.0 확정 (현재) |
| v0.3 | Story Engine |
| v0.5 | 첫 자동 생성 (Beyond Humanity 파이프라인 관통) |
| v1.0 | 첫 번째 영화급 다큐멘터리 완성 |

## Agent 구조 로드맵 (ADR-0004)

| 버전 | 구조 |
|------|------|
| v0.1 (지금) | 단일 파이프라인 — 하나의 AI가 모든 의사결정 |
| v0.5 | Research / Story / Director를 역할별 모듈로 분리 |
| v1.0 이후 | Research Agent, Director Agent, Editor Agent 협업 구조 |

---

# 첫 번째 에피소드 후보

**What Will Humans Look Like in 1 Million Years?**
(100만 년 후 인간은 어떤 모습일까?) — 채널: Beyond Humanity
