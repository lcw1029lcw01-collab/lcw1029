# ADOS

**AI Documentary Operating System** — AI Documentary Studio

> **"AI가 감독처럼 생각하고, 영화처럼 제작한다."**

Netflix 수준의 AI 다큐멘터리를 자동 생성하는 콘텐츠 운영체제.
사람은 4가지만 결정한다 — **주제, 언어, 영상 길이, 채널**. 그 외 모든 과정(리서치→스토리→연출→생성→편집→업로드)은 ADOS가 수행한다.

## 핵심 개념: Decision Engineering

ADOS의 핵심은 Prompt 생성이 아니라 **의사결정(Decision)** 이다.

```
Research → Story → Emotion → Direction → Generation
```

Prompt는 결과물이다. AI는 생성기가 아니라 **감독**이다. (ADR-0002)

## 시작하기 (AI와 사람 공통)

**`docs/00_SYSTEM_PROMPT.md`부터 번호 순서로 읽는다.**

```
docs/
├── 00_SYSTEM_PROMPT.md      ⭐ ADOS 헌법 (자주 수정하지 않음)
├── 01_AI_CONTEXT.md         현재 프로젝트 상태 (수시 갱신)
├── 02_PROJECT_CHARTER.md    프로젝트 헌장
├── 03_ARCHITECTURE.md       시스템 구조 (v1.0 확정)
├── 04_DATA_FLOW.md          데이터 흐름
├── 05_DEVELOPMENT_RULES.md  개발 규칙
├── 06_ROADMAP.md            로드맵
├── 07_GLOSSARY.md           용어집
├── bibles/                  제작 규칙 (story·director·camera·emotion·world·prompt)
└── adr/                     Architecture Decision Records
```

변경 이력은 [CHANGELOG.md](CHANGELOG.md), 할 일은 [TASK.md](TASK.md) 참조.

## 폴더 구조 (v1.0 확정 — ADR-0003)

```
ados/
├── docs/          설계 문서
├── src/           코드 (project/research/story/scene/visual/providers/editing/publish/shared)
├── schemas/       JSON 구조 (scene, shot, project)
├── prompts/       AI 프롬프트 템플릿
├── templates/     템플릿
├── scripts/       유틸리티 스크립트
├── tests/         테스트
├── output/        생성 결과물
└── assets/        에셋
```

## 현재 버전

**v0.2.0** — Sprint 1 (설계) / Architecture v1.0 확정

## 운영 채널 (포트폴리오)

| 채널 | 주제 |
|------|------|
| Beyond Humanity | 미래 문명·인류·과학·철학 (1순위) |
| Humanity Explained | 인간 심리·행동·진화 |
| Civilization Stories | 국가·문화·문명의 성공과 실패 |

각 채널은 영어 + 한국어 2개로 운영.
