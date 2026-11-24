# 현은빈 · Eunbin Hyun

Physical AI · Autonomous Robot · Edge Computer Vision

[GitHub](https://github.com/eunbin-hyun) · [Repositories](https://github.com/eunbin-hyun?tab=repositories)

## 소개

카메라와 센서 데이터를 AI 모델로 해석하고, 그 결과를 실제 로봇의 움직임으로 연결하는 개발자입니다. YOLO 기반 비전 모델의 데이터 구축과 학습, 엣지 NPU 배포, ROS 2 자율주행, 디지털 트윈과 임베디드 하드웨어 통합을 경험했습니다.

## 핵심 역량

- ROS 2 기반 센서·상태머신·로봇 제어 통합
- YOLO 객체 탐지·인스턴스 분할 모델 학습과 검증
- PyTorch → ONNX → Hailo HAR/HEF 변환 및 PTQ 기반 엣지 최적화
- Jetson Orin Nano, Raspberry Pi 5, Hailo-8L, STM32 연동
- OpenCV 기반 AprilTag 기하 추정·CLAHE 영상 전처리
- RoboDK 디지털 트윈, Onshape 3D 설계, Simulation Dashboard 구현

## 프로젝트

### Tac-Touch — 촉각센서·그리퍼 PC 통합

2026.10–11 · SSAFY 15기 자율 프로젝트 · 6명 · [프로젝트 소개](projects/Tac-Touch.md)

**담당: Gateway · 공용 API · PC 통합 · 메인 런처 · 시나리오 실행 관리**

- 센서·감지·제어·GUI의 공통 데이터 계약과 통신 경계 설계
- 시리얼 수신·CSV 파싱과 WebSocket Gateway 구현
- 호출자 권한·요청 범위·중복·만료 처리와 접속 상태 복원
- 런처·시나리오의 준비·실행·종료와 장비 예약·단절 관리
- ROS 그리퍼 상태·명령 연결, 모의 시험과 제한된 실물 확인 범위 구분

`Python` · `WebSocket` · `USB Serial` · `ROS 2`

### BONDI — AI 유물 복원 VR 박물관

2026.08–09 · SSAFY 15기 특화 프로젝트 · 7명 · [프로젝트 소개](projects/BONDI.md)

**담당: AdaPoinTr 형상 복원 · 데이터·평가 · TTA · 메시화**

- 합성 결손 학습 데이터와 형상 단위 학습·평가 분할 구성
- AdaPoinTr 파인튜닝과 회전 TTA로 결손 형상 추정
- 평가 누출 수정과 결손부 중심 지표 비교
- 관측부와 AI 생성 면을 분리하는 메시화 구현
- 2026 SSAFY 특화 프로젝트 우수상 · 광주 2반 2등

`PyTorch` · `AdaPoinTr` · `Point Cloud` · `Blender`

### SSACURITY — AprilTag 기반 자율주행 보안 로봇

2026.07–2026.08 · SSAFY 15기 공통 프로젝트 · [프로젝트 소개](projects/SSACURITY.md)

**담당: Jetson · AprilTag 자율주행 · 관제 연동**

- OpenCV `tag36h11` 검출과 카메라 좌표 변환으로 종방향 거리·횡방향 오차 계산
- AprilTag 4장을 기준으로 출발, 90° 회전, 도착, U턴, 복귀하는 경로 상태머신 구현
- 일시 태그 손실, 최대 주행거리·시간 상한, FAULT latch와 HOLD 복귀 등 안전 상태 설계
- Jetson–STM32 UART V3 프레임, CRC, 스트림 파서와 가상 STM32 기반 검증 환경 구성
- 실제 카메라·차량 없이 동작하는 closed-loop course simulator 구축
- 기존 검증 기록: ROS 비의존 핵심 로직 테스트 243개 통과, 모의 폐루프 E2E 시나리오 5/5 통과

`ROS 2 Humble` · `Jetson Orin Nano` · `AprilTag` · `OpenCV` · `STM32` · `UART` · `WebSocket`

### AQIS for SmartFactory — AI 품질 검사 스마트팩토리

2026.06 · 4주 · SSAFY 15기 광주 4반 3조 · [프로젝트 소개](projects/AQIS.md)

**담당: Simulation · AI · 3D**

- RoboDK 기반 검사·분류·운반 공정 디지털 트윈과 로봇 공정 스크립트 구현
- 실제 장비보다 Simulation Dashboard를 먼저 개발하는 mock-first 전략 적용
- Onshape 기반 부품 설계와 3D 프린팅 자산 제작
- Roboflow 데이터 구성과 캔 뚜껑 정상·불량 YOLO 모델 학습
- 실제 장비 경로와 simulation 경로가 같은 백엔드·이벤트 모델을 사용하도록 통합

`RoboDK` · `YOLOv5` · `Onshape` · `React` · `FastAPI` · `ROS 2`

### Tangerine Pests AI Robot — 감귤 병해충 탐지·방제 로봇

[Repository](https://github.com/eunbin-hyun/tangerine_pests_AI)

**담당: 데이터 · AI 모델 · 엣지 배포 · 하드웨어 통합**

- AI-Hub와 자체 촬영 이미지를 병합하고 감귤 병해충 데이터셋 구축·라벨링
- YOLOv8 모델 학습과 실제 감귤 이미지 탐지 검증
- PyTorch 모델을 ONNX와 Hailo HAR로 변환
- Hailo Dataflow Compiler에서 PTQ·하드웨어 최적화 후 Hailo-8L용 HEF 생성
- Raspberry Pi 5와 Hailo-8L NPU 기반 임베디드 추론 구조 구성

`YOLOv8` · `PyTorch` · `ONNX` · `Hailo DFC` · `Raspberry Pi 5` · `Hailo-8L`

### Night & Rain Lane Segmentation — 야간·우천 차선 인식

[Repository](https://github.com/eunbin-hyun/Night_Rain_Lane_Segmentation)

**담당: 팀장 · 데이터 · 모델 학습 · 임베디드 추론**

- 편광필름으로 젖은 노면의 반사광을 줄이고, LAB L 채널 CLAHE로 저조도 대비 강화
- `yellow_line`, `white_line` YOLO11n segmentation 데이터 구축과 모델 학습
- Raspberry Pi 5·Picamera2 실시간 영상 파이프라인 구현
- 기존 모델 대비 Recall 28.7%p, mAP50 11.2%p 향상
- 한국전기전자학회 하계학술대회 논문 제1저자

`YOLO11n-seg` · `OpenCV` · `CLAHE` · `Raspberry Pi 5` · `Picamera2`

## 기술

| 분야 | 기술 |
|---|---|
| Language | Python, C, JavaScript |
| Robotics | ROS 2 Humble, AprilTag, Ackermann steering, RoboDK |
| AI / Vision | PyTorch, YOLOv5/8/11, OpenCV, ONNX, Hailo DFC |
| Edge / Embedded | Jetson Orin Nano, Raspberry Pi 5, Hailo-8L, STM32F429 |
| Integration | FastAPI, WebSocket, UART, Git, Linux |
| 3D | Onshape, 3D printing, Three.js |

## 수상

- 2025-1학기 캡스톤디자인 결과발표회 우수상
- 2024 제32회 설계 및 팀프로젝트 작품전시회 최우수상
- 2024 IP 창의발명 경진대회 동상
- 2024-2학기 캡스톤디자인 결과발표회 장려상

## 논문 · 특허

- 2025 한국전기전자학회 하계학술대회 제1저자
  - 「야간 및 악천후 환경에서의 딥러닝 기반 실시간 차선 인식 시스템」
- 특허 출원 `10-2025-0016861`
  - 「감귤 병충해 실시간 진단 및 예방 장치」

## 학습 기록

- [AlgorithmTest_practice](https://github.com/eunbin-hyun/AlgorithmTest_practice)
- [CodeUp_Algorithm](https://github.com/eunbin-hyun/CodeUp_Algorithm)
- [studyPy](https://github.com/eunbin-hyun/studyPy)
- [Pyton_Team_Notes](https://github.com/eunbin-hyun/Pyton_Team_Notes)
