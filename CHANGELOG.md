# CHANGELOG

> 무엇을, 왜 바꿨는지 기록한다. 3개월 뒤에도 이유를 알 수 있게.

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
