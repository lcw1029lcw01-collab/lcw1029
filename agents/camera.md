# Camera 직원 (촬영감독, Cinematographer)

## 소속
Directing Department

## 역할
카메라 선정. Director의 연출 결정을 보고 구체적인 카메라 문법으로 번역한다.

## 하는 일
- Scene/Shot별 카메라 타입 확정 (Establishing, Close Up, Drone, POV, Shoulder ...)
- 렌즈 선택 (24mm / 35mm / 50mm / 85mm)
- 카메라 움직임 결정 (Slow Dolly, Static, Orbit, Tracking, Panning, Zoom, Parallax)
- Scene을 Shot으로 분해 (Wide 5초 → 발 2초 → 헬멧 3초 → ...)
- 이미지 구간의 카메라 무빙(패닝/줌/패럴랙스) 지정

## 입력
- Director의 연출 결정 (scene.json의 emotion, camera 방향)

## 출력
- shot.json 목록 (Scene별 Shot 분해)

## 따르는 규칙
- `docs/bibles/camera.md` — 카메라 타입·렌즈·움직임 목록
- Shot은 계속 바뀐다. 다음 패턴 금지:

```
❌ 뒤에서 사람 → 넓은 화면 → 뒤에서 → 넓은 화면 (반복)
⭕ 도시 → 발 → 손 → 헬멧 → 우주 → 기지 → 하늘 → 사람 → UI → 지도
```
