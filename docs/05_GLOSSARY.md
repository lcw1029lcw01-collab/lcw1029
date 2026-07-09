# 05. GLOSSARY — 용어집

프로젝트 전체에서 같은 의미로 쓰는 용어 정의. AI와 사람이 같은 언어로 말하기 위한 문서.

| 용어 | 정의 |
|------|------|
| **ADOS** | AI Documentary Operating System. 이 프로젝트. 주제 입력 → 영화급 다큐 자동 생성 운영체제 |
| **Scene** | 영상의 최소 단위. 5~8초. 25분 영상 = 약 120~200 Scene. 이미지·영상·나레이션 생성의 기준 |
| **Shot** | Scene 안에서의 카메라 단위 (Wide, Close Up, Drone, POV 등). 영화는 Shot이 계속 바뀐다 |
| **Scene Script** | 글이 아니라 장면(Scene) 단위로 쓰는 대본. "영화를 쓰는" 방식. 문장 하나가 아니라 장면 하나가 단위 |
| **Engine** | 파이프라인의 한 단계를 담당하는 독립 모듈 (Story Engine, Director Engine 등). 서로 JSON으로 통신 |
| **Bible** | 제작 규칙 문서. 모든 엔진·직원이 따르는 기준 (`docs/bibles/`) |
| **World Bible** | 세계관 설정. 연도별 기술·정치·경제·도시·인간의 모습. 모든 영상이 같은 세계관을 공유하게 만든다 |
| **Character Bible** | 캐릭터 외형·행동 정의. 100편 동안 같은 인물을 유지하기 위한 기준 |
| **Camera Bible** | 카메라 타입·렌즈·움직임 문법 정의 |
| **Color Bible** | 장소·감정별 색감 규칙 (Earth=Blue, Mars=Orange 등) |
| **Director Engine** | ⭐ 핵심 엔진. 감정을 입력받아 카메라·렌즈·조명·색감·음악·속도를 결정한다 |
| **Emotion Engine** | Scene별 감정을 수치로 표현 (외로움 80, 공포 60 ...). Director 결정의 입력값 |
| **Decision Engineering** | 프롬프트 엔지니어링의 반대 개념. Prompt를 쓰는 게 아니라 **결정을 내리면 Prompt가 결과로 나온다** |
| **Prompt DSL** | 프롬프트 조립용 도메인 언어. Subject + Environment + Camera + Lens + Lighting + Mood + Film 블록 조합 |
| **Hook** | 영상 첫 15~30초의 강렬한 질문/충격. 시청 지속의 핵심 |
| **Visual Motif** | 매 영상 반복되는 시각 요소 (지구 홀로그램, HUD, 오프닝 애니메이션, 색감). 채널 정체성을 만든다 |
| **AI 직원 (Employee/Agent)** | 회사 구조의 AI 역할 단위 (리서처, 작가, 감독, 촬영감독, 편집자 등). `agents/` 폴더에 정의 |
| **Sprint** | 1주 단위 개발 주기. 문서 → 설계 → 검토 → 구현 → 테스트 → Commit |
| **ADOS Brain** | GitHub 저장소의 별칭. 코드 저장소가 아니라 **프로젝트의 기억(Memory)** |
| **AI First** | 사람보다 AI가 읽기 쉬운 구조를 우선하는 문서 설계 원칙 (번호 순서, 명시적 규칙) |
