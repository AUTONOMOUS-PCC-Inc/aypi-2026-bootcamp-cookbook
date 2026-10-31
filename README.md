<div align="center">

# 2026 부트캠프 쿡북

**AUTONOMOUS PCC 부트캠프에서 쓰는 강의자료(슬라이드) 원본 저장소입니다.**<br>
실습 코드는 회차별 `aypi-*-tutorial` 저장소에, 강의자료는 여기에 모읍니다.

![Format](https://img.shields.io/badge/형식-PPTX-D24726?style=for-the-badge)
![Day1](https://img.shields.io/badge/Day%201-슬라이드%20100장-0B1B33?style=for-the-badge)
![Topic](https://img.shields.io/badge/주제-자율주행%20AI-1E6FD9?style=for-the-badge)
![License](https://img.shields.io/badge/이용-교육%20목적-16A34A?style=for-the-badge)

[**받는 법**](#받는-법) · [**자료 목록**](#자료-목록) · [**Day 1 구성**](#day-1-구성) · [**함께 보는 저장소**](#함께-보는-저장소)

</div>

---

## 받는 법

슬라이드만 필요하면 웹에서 개별 파일을 눌러 **Download** 하면 됩니다.
전체를 받으려면 (파일이 커서 25MB 정도 내려옵니다):

```bat
git clone https://github.com/AUTONOMOUS-PCC-Inc/aypi-2026-bootcamp-cookbook.git
cd aypi-2026-bootcamp-cookbook
```

> [!NOTE]
> 이 저장소에는 **슬라이드만** 있습니다. 실습을 따라가려면
> 아래 [함께 보는 저장소](#함께-보는-저장소)의 실습 코드를 같이 받으세요.

---

## 자료 목록

| 폴더 | 파일 | 슬라이드 | 크기 |
|---|---|---|---|
| `day1/` | 1. 자율주행 AI 기초 — 오전 이론 (초안) | 43장 | 20.4 MB |
| `day1/` | 2. donkeycar 자율주행 실습 Part 1 — 세팅부터 학습까지 | 30장 | 0.5 MB |
| `day1/` | 3-2. donkeycar 자율주행 실습 Part 2 — 시뮬링크로 Donkeycar 모델 주행기록 비교하기 | 27장 | 4.4 MB |

---

## Day 1 구성

하루가 **이론 → 실습 → 검증** 세 덩어리로 흘러갑니다.

```
오전  이론 (2h)                오후  실습 Part 1              심화  실습 Part 2
      인지·판단·제어                 세팅 → 수집 → 학습 → 주행        Python ↔ MATLAB 동치성 검증
      모듈형 vs 행동복제              (donkeycar + 시뮬레이터)         (Simulink · Codex)
```

### 1. 자율주행 AI 기초 — 오전 이론

여섯 장(章)으로 자율주행 전체 그림을 한 번 훑습니다.

| 장 | 내용 |
|---|---|
| 1 | **자율주행이란** — SAE Level 0~5, 3대 요소와 3대 인지 센서, 두 가지 설계 철학 |
| 2 | **센서와 인식** — 카메라(이미지는 숫자 덩어리 · CNN · 분류/탐지/분할), 라이다, 센서 퓨전 |
| 3 | **SLAM** — 측정·추정·갱신·보정 루프, 점유 격자 지도, 누적 오차와 루프 폐쇄 |
| 4 | **경로 계획과 제어** — 전역/지역 경로, 코스트맵, 최단경로 탐색, Nav2가 대신해 주는 일 |
| 5 | **행동 복제** — 모듈형과 정반대의 접근, 학습 데이터의 형태, 데이터가 성능을 정한다 |
| 6 | **AI에게 코드를 시키는 법** — 프롬프트에 맥락을 싣는 네 가지 요령 |

### 2. donkeycar 실습 Part 1 — 세팅부터 학습까지

설치 0~7단계 → 시뮬레이터 띄우기 → 브라우저로 운전해 `tub` 수집 → 학습 → 자율주행 테스트.
설치 트러블슈팅과 "여기까지 왔나요?" 체크리스트, 바이브코딩 과제 프롬프트가 함께 들어 있습니다.

### 3-2. donkeycar 실습 Part 2 — 주행기록 비교

학습한 모델을 MATLAB으로 변환한 뒤, **Python과 MATLAB의 추론 결과가 같은지** 따져 봅니다.

| 과제 | 내용 |
|---|---|
| **A** | 단일 영상에 대한 수치 동치성 검증 — 불일치 시 오차 원인 분리 |
| **B** | 주행 기록 전체 비교 — 시계열 비교, 오차의 시간 분포, 조향 오차 상위 프레임 |
| **C** (심화) | 공개 Simulink 예제를 재구성해 보기 |

"**실행 가능성과 정확성은 다르다**" — 돌아간다고 맞는 게 아니라는 점이 이 파트의 핵심입니다.

---

## 함께 보는 저장소

| 저장소 | 쓰임 |
|---|---|
| [aypi-car-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-car-tutorial) | Day 1 실습 코드 — donkeycar + Unity 시뮬레이터 행동 복제 |
| [aypi-car-teleop-keyboard](https://github.com/AUTONOMOUS-PCC-Inc/aypi-car-teleop-keyboard) | 웹 컨트롤러 WASD 키보드 원격조종 패치 |
| [aypi-turtlebot-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-turtlebot-tutorial) | ROS 2 TurtleBot3 · SLAM / 경로계획 · Simulink |
| [aypi-metaverse-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-metaverse-tutorial) | text-to-CAD · 웹 3D 가상공간 |
| [aypi-agent-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-agent-tutorial) | 자동화 에이전트 — Codex(코드) · N8N(노코드) |

---

<div align="center">

**AUTONOMOUS PCC, Inc.**<br>
교육 목적으로 제공되는 자료입니다. 재배포·상업적 이용 전에는 문의해 주세요.

</div>
