# ADOS Glossary (용어집)

프로젝트 전체에서 같은 의미로 쓰는 용어 정의. AI와 사람이 같은 언어로 말하기 위한 문서.

| 용어 | 정의 |
|------|------|
| **ADOS** | AI Documentary Operating System. 이 프로젝트. 대외 정체성은 AI Documentary Studio |
| **Decision Engineering** | ADOS의 핵심 개념. Prompt를 쓰는 게 아니라 **결정을 내리면 Prompt가 결과로 나온다**. Prompt Engineering의 반대 |
| **Pipeline** | Research→Story→Scene→Visual→Asset→Editing→Publishing으로 이어지는 제작 흐름. ADOS의 본체 |
| **Module** | 파이프라인의 한 단계를 담당하는 독립 단위 (Project, Research, Story, Scene, Visual Planning, Asset Generation, Editing, Publishing) |
| **Provider** | 외부 AI 서비스 (Midjourney, Kling, Typecast 등). ADOS는 Provider에 종속되지 않는다 |
| **Adapter** | Provider를 감싸는 교체 가능한 연결층. Engine은 서비스를 모르고 Adapter만 안다 |
| **Scene** | 영상의 최소 단위. 5~8초. 25분 영상 = 약 120~200 Scene |
| **Shot** | Scene 안의 카메라 단위 (Wide, Close Up, Drone, POV 등). 영화는 Shot이 계속 바뀐다 |
| **Scene Script** | 글이 아니라 장면(Scene) 단위로 쓰는 대본. "영화를 쓰는" 방식 |
| **Narrative Design** | "Story(글쓰기)"보다 정확한 개념 — 우리가 만드는 것은 글이 아니라 **영상의 경험** |
| **Bible** | 제작 규칙 문서 (`docs/bibles/`). Story·Director·Camera·Emotion·World |
| **World Bible** | 세계관 설정. 모든 영상이 같은 세계관을 공유하게 만드는 연대기 |
| **Style Memory** | 채널별 톤앤매너 저장소 (나레이션 속도, 색감, 카메라, 음악). 100편을 만들어도 같은 감독이 만든 것처럼 보이게 한다 |
| **Quality System** | "좋은 영상이란 무엇인가"를 시스템으로 정의한 규칙 (예: 첫 30초 안에 Hook, 같은 화면 8초 이상 금지) |
| **System Prompt** | `00_SYSTEM_PROMPT.md`. 모든 AI가 가장 먼저 읽는 ADOS의 헌법. 자주 수정하지 않는다 |
| **AI Context** | `01_AI_CONTEXT.md`. 현재 프로젝트 상태 문서. 수시로 갱신된다 |
| **Spec (Specification)** | 개발 명세서. Purpose/Scope/Inputs/Outputs/Constraints/Acceptance Criteria 형식 |
| **ADR** | Architecture Decision Record. 중요한 설계 결정과 이유의 기록 (`docs/adr/`) |
| **YAGNI** | You Aren't Gonna Need It — 지금 필요하지 않은 것은 만들지 않는다 |
| **Hook** | 영상 첫 15~30초의 강렬한 질문/충격. 시청 지속의 핵심 |
| **Visual Motif** | 매 영상 반복되는 시각 요소 (지구 홀로그램, HUD, 오프닝). 채널 정체성을 만든다 |
| **Sprint** | 1주 단위 개발 주기. 요구사항 → 설계 → 구현 → 테스트 |
| **ADOS Brain** | GitHub 저장소의 별칭. 코드 저장소가 아니라 프로젝트의 기억(Memory) |
