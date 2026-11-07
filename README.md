<div align="center">

# 2026 부트캠프 쿡북

**AUTONOMOUS PCC 부트캠프에서 쓰는 강의자료(슬라이드) 원본 저장소입니다.**<br>
실습 코드는 회차별 `aypi-*-tutorial` 저장소에, 강의자료는 여기에 모읍니다.

![Format](https://img.shields.io/badge/형식-PPTX-D24726?style=for-the-badge)
![Slides](https://img.shields.io/badge/슬라이드-254장-0B1B33?style=for-the-badge)
![Topic](https://img.shields.io/badge/주제-자율주행·로보틱스·웹3D-1E6FD9?style=for-the-badge)
![License](https://img.shields.io/badge/이용-교육%20목적-16A34A?style=for-the-badge)

[**받는 법**](#받는-법) · [**자료 목록**](#자료-목록) · [**Day 1**](#day-1-구성--카메라로-배우는-자율주행) · [**Day 2**](#day-2-구성--라이다로-계산하는-자율주행) · [**Day 3**](#day-3-구성--말로-만드는-3d와-내가-만드는-공간) · [**함께 보는 저장소**](#함께-보는-저장소)

</div>

---

## 받는 법

슬라이드만 필요하면 웹에서 개별 파일을 눌러 **Download** 하면 됩니다.
전체를 받으려면 (파일이 커서 **130MB 정도** 내려옵니다):

```bat
git clone https://github.com/AUTONOMOUS-PCC-Inc/aypi-2026-bootcamp-cookbook.git
cd aypi-2026-bootcamp-cookbook
```

> [!NOTE]
> 이 저장소에는 **슬라이드만** 있습니다. 실습을 따라가려면
> 아래 [함께 보는 저장소](#함께-보는-저장소)의 실습 코드를 같이 받으세요.

> [!WARNING]
> `day2/1.ROS2_입문_선행이론_초안.pptx` 한 파일이 **101MB**입니다 (96MB짜리 영상이 슬라이드에
> 박혀 있습니다). 저장소 전체 용량의 80%가 이 파일 하나입니다. 느린 회선에서는 이 파일만
> 웹에서 따로 받는 편이 빠릅니다.

---

## 자료 목록

| 폴더 | 파일 | 슬라이드 | 크기 |
|---|---|---|---|
| `day1/` | 1. 자율주행 AI 기초 — 오전 이론 (초안) | 43장 | 20.4 MB |
| `day1/` | 2. donkeycar 자율주행 실습 Part 1 — 세팅부터 학습까지 | 30장 | 0.5 MB |
| `day1/` | 3-2. donkeycar 자율주행 실습 Part 2 — 시뮬링크로 Donkeycar 모델 주행기록 비교하기 | 37장 | 4.9 MB |
| `day2/` | 1. ROS 2 입문 — 선행 이론 (초안) | 17장 | 101.4 MB |
| `day2/` | 2-1. TurtleBot3 자율주행 실습 Part 1 — 세팅부터 SLAM+Nav2까지 **(Windows WSL)** | 27장 | 0.1 MB |
| `day2/` | 2-3. TurtleBot3 자율주행 실습 Part 1 — 세팅부터 SLAM+Nav2까지 **(macOS)** | 27장 | 0.1 MB |
| `day2/` | 3. TurtleBot3 자율주행 실습 Part 2 — MATLAB + Simulink 실습 | 25장 | 0.1 MB |
| `day3/` | 1. 텍스트 투 캐드 3D 모델링 — 오전 (초안) | 17장 | 0.1 MB |
| `day3/` | 2. 메타버스 웹 3D 실습 (확장, 초안) | 31장 | 0.2 MB |

> [!IMPORTANT]
> `day2/`의 **2-1(Windows WSL)**과 **2-3(macOS)**는 **같은 실습의 OS별 판본**입니다.
> 내용은 같고 설치 방법만 다릅니다 — 자기 노트북에 맞는 쪽 **하나만** 보면 됩니다.

---

## Day 1 구성 — 카메라로 배우는 자율주행

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

## Day 2 구성 — 라이다로 계산하는 자율주행

Day 1의 donkeycar가 **카메라로 사람 운전을 따라 배웠다면**, Day 2의 TurtleBot3는
**라이다로 지도를 만들고 길을 계산**합니다. 같은 문제를 푸는 정반대의 두 방법입니다.

```
선행 이론 (20분)            실습 Part 1 (100분)             심화  실습 Part 2 (90분)
   ROS 2 · DDS                  설치 → SLAM → Nav2              MATLAB/Simulink로 직접
   토픽·서비스·액션              → Codex 순찰 코드                SLAM · A* · Pure Pursuit
```

### 1. ROS 2 입문 — 선행 이론 (20분)

실습에서 그대로 명령어로 나올 낱말들을 먼저 깔아 둡니다.

| 장 | 내용 |
|---|---|
| 1 | **ROS란 무엇인가** — OS가 아니라 로봇 소프트웨어의 공통 바탕. 통신 · 도구 · 생태계 |
| 2 | **ROS 1 → ROS 2** — `roscore`가 사라진 P2P 분산 구조, 국제 표준 DDS, micro-ROS, 라이프사이클 노드 |
| 3 | **노드끼리 말을 거는 세 가지** — 토픽(계속 흐른다) · 서비스(묻고 답한다) · 액션(시켜 놓고 지켜본다) |
| 4 | **작업 공간** — `ros2_ws`의 `build` / `install` / `log` / `src`, 직접 건드리는 건 `src` 하나뿐 |

> RViz에서 목표점을 찍는 순간 `NavigateToPose` **액션**이 하나 생깁니다 — 이론과 실습이
> 여기서 만납니다. (원본: 윤성웅 · 세미나 1주차 발표 「ROS2와 DDS」, KNU ACE Lab.)

### 2. TurtleBot3 SLAM + Nav2 실습 Part 1 (100분)

설치 35분이 가장 큰 고비입니다. ROS를 내려받는 동안 Codex CLI를 같이 설치해 시간을 아낍니다.

| 단계 | 하는 일 |
|---|---|
| **설치** | ROS 2 Humble · TurtleBot3 · Codex CLI (터미널 4개로 역할 분담) |
| **1** | Gazebo 시뮬레이터에 로봇 띄우기 — 육각형 경기장 |
| **2~3** | SLAM으로 지도 그리기 + 키보드 운전(`w`/`a`/`d`/`x`) — 벽 따라 한 바퀴 → 제자리 회전 → 기둥 사이 → **출발점 복귀(루프 폐쇄)** |
| **4** | `map_saver_cli`로 `map.pgm` + `map.yaml` 저장 |
| **5~7** | Nav2 실행 → `2D Pose Estimate`로 초기 위치 → `Nav2 Goal`로 자율주행 |
| **8~10** | `/clicked_point`로 순찰 좌표 4개 채집 → **Codex에게 말로 시켜** `patrol.py` 생성 → 실행 |

**OS별 판본 차이**

| | `2-1` Windows WSL | `2-3` macOS |
|---|---|---|
| 설치 도구 | WSL2 + Ubuntu 22.04 + `apt` | micromamba + RoboStack (brew·Docker 없이) |
| 다운로드 | 약 3GB · 15~25분 | 약 7GB · 15~30분 |
| SLAM | Cartographer | `slam_toolbox` (Mac에서 Cartographer가 바로 꺼짐) |
| 토픽 격리 | `ROS_LOCALHOST_ONLY=1` | `ROS_DOMAIN_ID`를 자리 번호로 |
| 환경 진입 | 새 탭이면 자동 (`~/.bashrc`) | 탭마다 `ros` 한 단어 |

> "Codex는 언제나 그럴듯한 코드를 씁니다. **맞는지는 로봇이 실제로 4곳을 도는지로 판정합니다.**"

### 3. TurtleBot3 실습 Part 2 — MATLAB + Simulink (90분, 심화)

Part 1에서 **Nav2가 대신해 주던 지도·경로·제어를 이번엔 직접 만듭니다.**
Gazebo는 WSL에서, MATLAB은 Windows에서 — 두 쪽이 `/scan` · `/odom` · `/cmd_vel` 세 토픽으로 대화합니다.

| 단계 | 내용 |
|---|---|
| **연결** | WSL `networkingMode=mirrored` + 방화벽 + `ROS_DOMAIN_ID` 맞추기 — 15분 안에 `/scan`이 보여야 합니다 |
| **기초** | `ros2node` / `ros2subscriber` / `ros2publisher` — 라이다 그리기, 위치 읽기, 속도 보내기 |
| **회피** | `avoidController.m` — 정면 ±30°가 0.5m 안이면 멈추고 더 비어 있는 쪽으로 회전 |
| **Simulink** | 같은 제어기를 블록 6개로 (Subscribe → Bus Selector → MATLAB Function → Bus Assignment → Publish) |
| **SLAM·경로** | `lidarSLAM` → `buildMap` → `inflate` → `plannerAStarGrid` → `controllerPurePursuit` |
| **코드 생성** | Simulink 모델을 ROS 2 노드로 빌드해 WSL에서 실행 (강사 시연 · Coder 라이선스 필요) |

**같은 로봇, 세 가지 개발 방식**

| | Nav2 + Python (Part 1) | MATLAB | Simulink |
|---|---|---|---|
| 방식 | 완성된 도구를 조합 | 알고리즘을 직접 | 블록으로 설계 |
| 강점 | 빠르게 동작 | 그래프로 바로 확인 | 검증 후 코드 생성, 실기 배포까지 |
| 한계 | 속은 블랙박스 | 배포는 별개 | 라이선스가 필요 |

---

## Day 3 구성 — 말로 만드는 3D와, 내가 만드는 공간

**오전의 산출물이 오후의 입력입니다.** 오전에 만든 `mymodel.glb` 파일 하나가
점심을 건너 오후 실습의 재료가 됩니다 — 중간에 끊기지 않습니다.

```
오전 10:00-12:00                              오후 13:00-16:00
  말로 설명 → OpenSCAD 코드 → Render            스타터 → 내 GLB 올리기 → 조명·배경
  → 고쳐 요청 3~4바퀴 → GLB 내보내기              → 캐릭터 + WASD  ┊ (심화) socket.io 멀티플레이
```

### 1. 텍스트 투 캐드 — 오전 이론 + 실습

| 장 | 내용 |
|---|---|
| 1 | **CAD와 메시** — 치수로 정의하느냐(OpenSCAD·Fusion), 삼각형 껍데기냐(Blender·스캔) |
| 2 | **GLB** — 3D의 공통 통화. STL은 형상만, OBJ는 색이 따로, GLB는 한 파일에 전부 |
| 3 | **Text-to-CAD의 실체** — AI는 형상을 그리지 않고 **형상을 만드는 코드**를 씁니다 |
| 4 | **OpenSCAD 30초 문법** — `cube` · `cylinder` · `sphere` · `translate` · `difference` · `color`, 그리고 `$fn` / `center` / 단위 |
| 5 | **왜 마우스가 아니라 코드인가** — AI와 같이 일하려면 모델이 글자여야 합니다 |
| 6 | **보고 → 고쳐 요청하기** — 이 원을 3~4바퀴 도는 것이 오늘의 실습 |

도구는 **Codex**(코드를 쓰는 쪽)와 **OpenSCAD Playground**(형상을 보여 주는 쪽) 둘뿐 —
설치도 가입도 없습니다.

**AI가 자주 틀리는 것 — 대응표**

| 증상 | 원인 | 이렇게 말하세요 |
|---|---|---|
| 아무것도 안 보인다 | 도형이 화면 밖에 있다 | "모든 부품을 원점 근처로 옮겨 줘" |
| 원이 각져 보인다 | `$fn`을 안 줬다 | "`$fn = 48`을 맨 위에 넣어 줘" |
| 부품이 절반 어긋난다 | `center`를 섞어 썼다 | "`center` 옵션을 전부 통일해 줘" |
| 뺀 자리에 얇은 막 | 빼는 도형이 딱 맞는다 | "빼는 도형을 위아래로 1씩 길게" |

> **실습 조건**: 부품 3개 이상 · 모든 치수를 mm 숫자로 · `difference()`로 구멍 한 군데 ·
> 색 2가지 이상 · **고쳐 요청하기 최소 3번**. 11:45까지 `mymodel.glb`가 손에 있어야 합니다.

### 2. 메타버스 웹 3D 실습 — 오후

남의 플랫폼에 업로드하지 않습니다. **공간 자체를 만듭니다** (React Three Fiber + socket.io).

**기본 트랙 — 오늘의 목표 (4번까지)**

| # | 하는 일 |
|---|---|
| 1 | 스타터 저장소를 `npm run dev`로 띄운다 → `localhost:5173` |
| 2 | 오전에 만든 GLB를 `web3d/public/`에 넣고 장면 가운데 올린다 (`scale={0.01}`) |
| 3 | HDRI(`adamsbridge.hdr`)로 배경·환경광을 깔고 그림자를 떨어뜨린다 |
| 4 | `Robot.glb`를 세우고 **WASD로 걸어 다닌다** (Idle / Walk / Run / Fast Run / Jump) |

**심화 트랙 — 먼저 끝낸 사람**

| # | 하는 일 |
|---|---|
| 5 | `Colleague.jsx` — `SkeletonUtils`로 로봇을 복제하고 머리 위에 이름표 |
| 6 | `server/` 폴더에 socket.io 서버(3001) + `ServerConnector.jsx` |
| 7 | 창 두 개에서 함께 걷기 — 0.2초마다 바뀔 때만 전송, 받는 쪽은 **보간** |
| 8 | 로그인·채팅 오버레이, 같은 Wi-Fi의 다른 기기에서 입장 |

**이 자료의 핵심 장치**

- **`AGENTS.md`** — Codex가 읽는 규칙 파일. 버전(`three 0.153` / `fiber 8.13.4` / `drei 9.77.4`),
  에셋 목록, 이벤트 약속표를 **코드보다 먼저** 적습니다. 버전을 못 박지 않으면 AI가 최신 문법을 섞어 씁니다.
- **이벤트 표가 먼저** — `join` / `update` / `talk` / `characters`.
  client는 `message`로 보내는데 server는 `chat`을 기다리면 **에러도 없이 아무 일도 안 일어납니다.**
- **"AI가 완료라고 해도 다섯 군데를 본다"** — 화면(창 두 개) · 콘솔(F12) · 서버 터미널 · FPS · 커밋.
- **숫자로 판단한다** — CAD 트로피 1,308 삼각형, 로봇 한 대 55,320, 네 대 221,280(FPS 145 유지).
  느려지는 1순위는 삼각형이 아니라 **그림자와 텍스처**입니다.

> "**고치기 전에 원인부터 설명해 줘**"가 가장 많이 아낀 말입니다 —
> AI가 추측으로 코드를 갈아엎기 전에 멈춰 세웁니다.

---

## 함께 보는 저장소

| 저장소 | 쓰임 |
|---|---|
| [aypi-car-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-car-tutorial) | **Day 1** 실습 코드 — donkeycar + Unity 시뮬레이터 행동 복제 |
| [aypi-car-teleop-keyboard](https://github.com/AUTONOMOUS-PCC-Inc/aypi-car-teleop-keyboard) | **Day 1** 웹 컨트롤러 WASD 키보드 원격조종 패치 |
| [aypi-turtlebot-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-turtlebot-tutorial) | **Day 2** ROS 2 TurtleBot3 · SLAM / Nav2 · MATLAB + Simulink |
| [aypi-metaverse-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-metaverse-tutorial) | **Day 3** text-to-CAD · 웹 3D 가상공간 (`AGENTS.md` · 스타터 · 에셋) |
| [aypi-agent-tutorial](https://github.com/AUTONOMOUS-PCC-Inc/aypi-agent-tutorial) | 자동화 에이전트 — Codex(코드) · N8N(노코드) |

---

<div align="center">

**AUTONOMOUS PCC, Inc.**<br>
교육 목적으로 제공되는 자료입니다. 재배포·상업적 이용 전에는 문의해 주세요.

</div>
