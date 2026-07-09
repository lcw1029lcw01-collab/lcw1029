# ADOS Data Flow

Version: 0.1.0

Status: Draft (초안 — GPT 아키텍트의 정식 설계 대기 중)

---

# Purpose

이 문서는 ADOS 파이프라인 단계 간에 오가는 데이터의 형태와 흐름을 정의한다.

`03_ARCHITECTURE.md`의 5장(Data Flow)을 데이터 규격 수준으로 상세화한다.

---

# 전체 흐름

```
Topic (사용자 입력: 주제·언어·길이·채널)
   │
   ▼
Research Document        ← Research Module 출력
   │
   ▼
Story Structure          ← Story Module 출력 (Hook/Conflict/Discovery/Twist/Ending/Question)
   │
   ▼
Scene List               ← Scene Module 출력 (scene.json 배열)
   │
   ▼
Visual Plan              ← Visual Planning Module 출력 (Camera/Lighting/Color/Mood/Composition)
   │
   ▼
Assets                   ← Asset Generation Module 출력 (이미지·영상·음성·자막 파일)
   │
   ▼
Video (MP4)              ← Editing Module 출력
   │
   ▼
Publish                  ← Publishing Module (Title/Description/Tags/Thumbnail/SEO)
```

---

# 데이터 규격

모든 단계 간 데이터는 JSON으로 주고받으며, 규격은 `schemas/`에 정의한다.

| 데이터 | 규격 파일 | 상태 |
|--------|----------|------|
| Project Configuration | `schemas/project.json` | v0.1 |
| Scene | `schemas/scene.json` | v0.1 |
| Shot | `schemas/shot.json` | v0.1 |
| Research Document | (미정) | 예정 |
| Story Structure | `schemas/project.json`의 `story` 블록 | v0.1 |
| Visual Plan | `schemas/scene.json`의 연출 필드 | v0.1 |

---

# Scene 데이터 예시

```json
{
  "scene": 1,
  "emotion": { "dominant": "외로움", "scores": { "외로움": 80, "희망": 10 } },
  "camera": "Wide",
  "lens": "24mm",
  "lighting": "새벽",
  "weather": "안개",
  "subject": "미래 인간",
  "motion": "천천히 걷기",
  "duration": 5
}
```

---

# TODO (GPT 정식 설계 시 확정)

- Research Document 스키마
- Visual Plan 독립 스키마 여부
- Asset 메타데이터 (파일 경로, 생성 Provider, 버전)
- 단계 간 실패/재시도 데이터 처리
