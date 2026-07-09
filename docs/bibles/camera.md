# Camera Bible (v0.1 초안)

> 카메라 문법 정의. Director Engine이 이 목록에서 자동 선택한다.

## 카메라 타입 목록

| 타입 | Midjourney 문구 | 용도 |
|------|----------------|------|
| Establishing (Wide) | `Ultra wide establishing shot` | 장소·규모 소개, 외로움·경외감 |
| Close Up | `Extreme close up` | 감정, 공포, 디테일 |
| Drone | `Drone aerial shot` | 스케일, 이동, 부감 |
| Shoulder | `Over the shoulder` | 인물 시점 유도, 몰입 |
| Side | `Side profile` | 인물의 고독·사색 |
| POV | `POV shot` | 1인칭 몰입 |
| Low Angle | `Low angle shot` | 위압감, 웅장함 |
| High Angle | `High angle shot` | 무력감, 조망 |
| Tracking | — | 이동 추적 |
| Orbit | — | 대상 중심 회전 (드론 Orbit 등) |
| Macro | — | 초근접 디테일 |
| Handheld | — | 긴박감, 현장감 |

## 렌즈

| 렌즈 | 용도 |
|------|------|
| 24mm | Wide, Establishing — 공간·고립감 |
| 35mm | 자연스러운 시네마틱 표준 |
| 50mm | 인물 중심 |
| 85mm | Close Up — 감정·압축 |

## Scene별 카메라 지정 형식

Director Engine이 Scene마다 자동 결정한다:

```
Scene 001
Camera: Establishing / Lens: 24mm / Movement: Slow Dolly / Lighting: Sunrise

Scene 002
Camera: Close Up / Lens: 85mm / Movement: Static

Scene 003
Camera: Drone / Height: 50m / Movement: Orbit

Scene 004
Camera: POV / Movement: Walking
```

## 카메라 무빙 (이미지에 생명 넣기)

Midjourney 이미지 + 후반 카메라 무빙으로 영상의 50~60%를 채운다:

- 패닝 (Panning)
- 줌 (Zoom In/Out)
- 패럴랙스 (Parallax)

## Kling 모션 문구 (예시)

```
Slow cinematic dolly in.
Wind blowing.
Dust particles.
Camera shake.
Natural eye blinking.
Soft breathing.
```
