# ADOS Architecture

Version: 1.0.0

Status: Draft

Last Updated: 2026-07-09

---

# 1. Purpose (목적)

이 문서는 ADOS(AI Documentary Operating System)의 전체 시스템 구조를 정의한다.

이 문서는 프로젝트에서 가장 중요한 기술 문서이며, 모든 개발은 이 문서를 기준으로 진행한다.

---

# 2. Architecture Principles (설계 원칙)

## 2.1 Pipeline First

ADOS는 하나의 거대한 AI가 모든 작업을 수행하지 않는다.

작업을 여러 단계(Pipeline)로 나누고, 각 단계는 하나의 명확한 책임만 가진다.

---

## 2.2 Decision First

ADOS의 핵심은 Prompt 생성이 아니다.

ADOS의 핵심은 의사결정(Decision)이다.

모든 생성은 의사결정 이후에 이루어진다.

Research → Story → Emotion → Direction → Generation

---

## 2.3 AI Provider Independent

ADOS는 특정 AI 서비스에 종속되지 않는다.

예시

Image Provider

- Midjourney
- Flux
- GPT Image
- Stable Diffusion

Motion Provider

- Kling
- Runway
- Veo

Voice Provider

- Typecast
- ElevenLabs
- OpenAI Voice

Provider는 언제든 교체 가능해야 한다.

---

## 2.4 Modular

각 모듈은 독립적으로 개발 가능해야 한다.

한 모듈이 변경되어도 다른 모듈에 영향을 최소화해야 한다.

---

# 3. System Overview

```
USER
↓
Project
↓
Research
↓
Story
↓
Scene Planning
↓
Visual Planning
↓
Asset Generation
↓
Editing
↓
Publishing
```

---

# 4. Core Modules

## 4.1 Project Module

책임

프로젝트 전체 설정 관리

입력

- 주제
- 언어
- 영상 길이
- 채널

출력

Project Configuration

---

## 4.2 Research Module

책임

주제 조사

입력

Topic

출력

Research Document

---

## 4.3 Story Module

책임

스토리 생성

입력

Research

출력

Story Structure

---

## 4.4 Scene Module

책임

스토리를 Scene으로 분리

입력

Story

출력

Scene List

---

## 4.5 Visual Planning Module

책임

각 Scene의 연출 결정

결정 항목

- Camera
- Lighting
- Color
- Mood
- Composition

출력

Visual Plan

---

## 4.6 Asset Generation Module

책임

Visual Plan을 실제 AI 서비스에서 생성

- Image
- Motion
- Voice
- Music
- Subtitle

---

## 4.7 Editing Module

책임

모든 Asset을 하나의 영상으로 합성

출력

MP4

---

## 4.8 Publishing Module

책임

유튜브 업로드

생성

- Title
- Description
- Tags
- Thumbnail
- SEO

---

# 5. Data Flow

```
Topic
↓
Research
↓
Story
↓
Scene
↓
Visual Plan
↓
Assets
↓
Video
↓
Publish
```

---

# 6. Directory Structure

```
src/
├── project/
├── research/
├── story/
├── scene/
├── visual/
├── providers/
├── editing/
├── publish/
└── shared/
```

---

# 7. Providers

- Image Provider
- Motion Provider
- Voice Provider
- Music Provider
- Subtitle Provider
- LLM Provider

모든 Provider는 Interface를 구현해야 한다.

Provider 변경 시 Engine은 수정하지 않는다.

---

# 8. Future Modules

- Knowledge Base
- Memory
- Director AI
- Style Memory
- Channel Memory
- Quality Checker
- Fact Checker
- Analytics

---

# 9. Non Goals

현재 버전(v1)은 아래 기능을 포함하지 않는다.

- 자동 업로드 스케줄링
- 멀티 사용자
- 웹 서비스
- 실시간 협업

---

# 10. Acceptance Criteria

이 문서를 읽은 개발자는

- 전체 구조를 이해할 수 있어야 한다.
- 각 모듈의 책임을 이해할 수 있어야 한다.
- 데이터 흐름을 이해할 수 있어야 한다.
- Provider를 교체 가능한 구조로 구현할 수 있어야 한다.
