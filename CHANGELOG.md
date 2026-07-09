# CHANGELOG

> 무엇을, 왜 바꿨는지 기록한다. 3개월 뒤에도 이유를 알 수 있게.

## 2026-07-09 — v0.2.0

### 변경 (GPT 아키텍트 3차 설계 반영)
- 00_AI_CONTEXT.md를 둘로 분리:
  - `00_SYSTEM_PROMPT.md` — ADOS 헌법. 철학·Hard Rules. 자주 수정하지 않음
  - `01_AI_CONTEXT.md` — 현재 프로젝트 상태. 수시 갱신 (루트 PROJECT_STATE.md를 이 문서로 통합)
- 문서 번호 재배치: 02_CHARTER, 03_ARCHITECTURE, 04_DATA_FLOW, 05_RULES, 06_ROADMAP, 07_GLOSSARY
- 03_ARCHITECTURE.md — GPT 제공 전문으로 교체 (v1.0 확정): Pipeline First / Decision First / Provider Independent / Modular, 8개 Core Module, Provider-Adapter 구조
- 02_VISION.md → 02_PROJECT_CHARTER.md에 통합 (Mission/Vision 섹션)
- decisions/ → adr/ (ADR-0001~0004, Architecture Decision Record 형식)
- 문서 작성 방식을 Spec 형식으로 전환 (Purpose/Scope/Inputs/Outputs/Acceptance Criteria)

### 폴더 구조 (v1.0 최종 확정 — ADR-0003)
- 제거: engines/, examples/, meetings/, agents/ (agents는 ADR-0004로 v1.0 이후 보류, git 히스토리에 보존)
- 추가: templates/, assets/, src/ 하위 모듈 9개 (project, research, story, scene, visual, providers, editing, publish, shared)

### 설계 결정
- ADR-0002: Prompt Engine → Decision Engine (Prompt라는 단어를 점점 없앰)
- ADR-0003: specs/ 폴더 만들지 않음 (YAGNI 원칙 채택)
- ADR-0004: AI 직원(Agent) 협업 구조는 단계적 도입 (v0.1 단일 파이프라인 → v0.5 모듈 분리 → v1.0+ Agent 협업)
- Architecture는 AI 서비스(Midjourney 등)에 종속되지 않는다 — Provider/Adapter 패턴

## 2026-07-09 — v0.1.2

### 변경
- 한글 파일명·폴더명(v0.1.1)을 다시 영문으로 복원
  - 이유: GPT(설계자)와 대화할 때 파일명이 서로 달라 헷갈리는 문제. GPT 설계 원안(영문) 유지가 협업에 유리 (CTO 결정)

## 2026-07-09 — v0.1.0

### 추가
- docs 번호 체계 도입 (00~06) — AI가 항상 같은 순서로 읽게 하기 위함 (AI First 구조)
- 00_AI_CONTEXT.md를 "프로젝트 소개"가 아니라 **AI 직원 교육 자료**로 작성
- ADOS 헌법 (01_PROJECT_CHARTER.md) — 10개 장 구조
- bibles/ 6개 초안 (story, director, camera, emotion, world, prompt)
- schemas/ 3개 (scene.json, shot.json, project.json) — 데이터 중심 설계
- agents/ AI 직원 정의 5개 (researcher, writer, director, camera, editor)
- 루트 운영 문서: PROJECT_STATE.md, TASK.md, CHANGELOG.md

### 변경
- docs/README.md → 루트 README.md로 이동 (GitHub 표시 관례)
- docs/PROJECT_CHARTER.md → docs/01_PROJECT_CHARTER.md
- docs/AI_CONTEXT.md → docs/00_AI_CONTEXT.md
- docs/ROADMAP.md → docs/04_ROADMAP.md

### 설계 결정
- 핵심 개념을 "Prompt Engineering"에서 **"Decision Engineering"** 으로 전환
  - 이유: ADOS는 Prompt를 생성하는 프로그램이 아니라 감독이다. 결정을 내리면 Prompt는 결과로 나온다.
- Engine 나열 구조에서 **회사(AI 직원) 구조**로 전환
  - 이유: 직원이 앞 직원의 결과물을 보고 일하는 구조가 더 자연스럽고 Claude Code 구현이 쉬워진다.

## 2026-07-09 — v0.0.1

### 추가
- 초기 프로젝트 구조 (폴더 10개 + docs 스텁 4개)
- GitHub Repository 연결 및 첫 push
