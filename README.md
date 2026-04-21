<div align="center">

# 🪞 Intelligent Smart Mirror

**Embedded IoT System with Face Recognition & Voice Interaction on Raspberry Pi**

[![EN](https://img.shields.io/badge/Language-English-blue?style=flat-square)](#-english)
[![KR](https://img.shields.io/badge/언어-한국어-red?style=flat-square)](#-한국어)

</div>

---

## 🇺🇸 English

A personalized smart-mirror system built on Raspberry Pi that fuses **real-time face recognition** and **voice-driven interaction** to deliver per-user information on demand. Designed and built end-to-end — from hardware assembly and optics tuning to algorithm implementation and frontend visualization.

### 📋 Project Overview

Beyond a passive information display, this mirror integrates **OpenCV's LBPH algorithm** for user identification and **Google Cloud STT** for natural-language interaction, forming an intelligent personal-assistant solution. The project covered the full system-integration lifecycle, from embedded algorithm optimization to physical frame fabrication.

- **Role:** Lead developer — system design, algorithm implementation, hardware integration
- **Context:** University capstone / graduation project
- **Core Tech:** LBPH real-time face recognition, Google Cloud STT integration, embedded-system optimization

### 🛠 Tech Stack

| Layer | Technology |
|---|---|
| **Language** | Python, JavaScript |
| **Frontend** | HTML, CSS, Vanilla JS |
| **Vision** | OpenCV, Local Binary Patterns Histograms (LBPH) |
| **Voice** | Google Cloud Speech-to-Text |
| **Hardware** | Raspberry Pi 3B+, Logitech C920 Camera, USB Mic/Speaker, Magic Mirror Glass, Aluminum Profile Frame |

### 🚀 Core Engineering Contributions

#### 1. LBPH-Based Real-Time Face Recognition
Deployed a lightweight identification pipeline capable of running reliably on low-power embedded hardware.
- **Dataset Construction & Training** — Used OpenCV's `haarcascade_frontalface_default.xml` for face detection, then trained an **LBPH (Local Binary Patterns Histograms)** model on the collected samples to generate per-user feature vectors.
- **Profile-Matching Trigger** — Implemented trigger logic that activates a user-specific dashboard (weather, schedule, greeting) the moment the live camera feed returns a matching identity.

#### 2. Voice Interaction via Google STT
Built a natural-language control layer that lets users operate the mirror hands-free.
- **Speech Processing Pipeline** — Integrated the **Google Cloud Speech-to-Text API** to convert microphone input into text, with a Python backend that maps keywords (weather, news, etc.) to module-level actions.
- **Hands-Free UX** — Enabled voice-driven screen transitions and information requests, maximizing usability in a no-touch mirror context.

#### 3. Web-Based Dashboard & Module Customization
- **Framework-Free UI** — Built a lightweight dashboard in pure Vanilla JS that renders clock, weather, Google Calendar, and news headlines in real time — no framework overhead on constrained hardware.
- **Optics-Aware Layout** — Designed a high-contrast black-background theme and CSS Flexbox/Grid layout tuned to the half-mirror's light-transmission ratio, so displayed information reads clearly through the reflective surface.

#### 4. Hardware System Integration & Fabrication
- **System Architecture** — Structured the connections between Raspberry Pi 3B+, camera, microphone, and monitor with attention to power budgeting and thermal management.
- **Physical Prototyping** — Fabricated the frame in-house from aluminum profile and magic-mirror glass, then calibrated display brightness so the surface functions simultaneously as a mirror and as a readable display.

### 💡 Technical Achievements

- **Algorithm-Level Depth** — Went beyond library use to understand LBPH feature extraction internally, enabling informed optimization for embedded deployment.
- **Full-Stack Engineering** — Delivered the full system cycle — hardware sensors → Python backend → JavaScript frontend — as a single developer.
- **Problem Solving** — Resolved lighting-induced accuracy variance in face recognition through dataset augmentation and threshold tuning.

<div align="right"><a href="#-한국어">🇰🇷 한국어로 보기 ↓</a></div>

---

## 🇰🇷 한국어

**라즈베리 파이 기반 지능형 스마트 미러**로, 실시간 얼굴 인식과 음성 인터랙션을 결합하여 사용자별 맞춤 정보를 제공합니다. 하드웨어 조립 및 광학 튜닝에서부터 알고리즘 구현과 프론트엔드 시각화까지 end-to-end로 설계·제작했습니다.

### 📋 프로젝트 개요

단순한 정보 출력을 넘어, **OpenCV의 LBPH 알고리즘**을 이용한 사용자 식별과 **Google Cloud STT** 기반 자연어 상호작용을 통합한 지능형 개인 비서 솔루션입니다. 임베디드 알고리즘 최적화에서부터 물리적 프레임 제작까지 시스템 통합 전 과정을 수행했습니다.

- **역할:** 메인 개발자 — 시스템 설계, 알고리즘 구현, 하드웨어 통합
- **맥락:** 학부 졸업 작품
- **핵심 기술:** LBPH 기반 실시간 얼굴 인식, Google Cloud STT 연동, 임베디드 시스템 최적화

### 🛠 기술 스택

| 계층 | 기술 |
|---|---|
| **언어** | Python, JavaScript |
| **프론트엔드** | HTML, CSS, Vanilla JS |
| **비전** | OpenCV, Local Binary Patterns Histograms (LBPH) |
| **음성** | Google Cloud Speech-to-Text |
| **하드웨어** | Raspberry Pi 3B+, Logitech C920 Camera, USB Mic/Speaker, Magic Mirror Glass, Aluminum Profile Frame |

### 🚀 핵심 엔지니어링 기여

#### 1. LBPH 기반 실시간 얼굴 인식
저사양 임베디드 환경에서 안정적으로 동작하는 경량 식별 파이프라인을 구축했습니다.
- **데이터셋 구축 및 학습** — OpenCV의 `haarcascade_frontalface_default.xml`로 얼굴을 검출하고, 수집한 데이터를 **LBPH(Local Binary Patterns Histograms)** 모델로 학습시켜 사용자별 고유 특징 벡터를 생성했습니다.
- **프로필 매칭 트리거** — 실시간 카메라 피드에서 인식된 ID와 매칭되는 사용자 전용 대시보드(날씨, 일정, 인사말 등)를 즉시 활성화하는 트리거 로직을 구현했습니다.

#### 2. Google STT 기반 음성 상호작용
사용자가 핸즈프리로 미러를 조작할 수 있는 자연어 제어 계층을 구축했습니다.
- **음성 처리 파이프라인** — **Google Cloud Speech-to-Text API**를 연동해 마이크 입력을 텍스트로 변환하고, Python 백엔드에서 특정 키워드(날씨, 뉴스 등)에 따라 모듈 동작을 매핑했습니다.
- **핸즈프리 UX** — 음성 입력을 통한 화면 전환 및 정보 요청 기능을 구현하여 비접촉 미러 환경에서의 사용성을 극대화했습니다.

#### 3. 웹 기반 대시보드 및 모듈 커스터마이징
- **프레임워크 없는 UI** — 순수 Vanilla JS로 시계, 날씨, 구글 캘린더, 뉴스 헤드라인을 실시간 렌더링하는 경량 대시보드를 구축하여, 제한된 하드웨어에서 프레임워크 오버헤드를 제거했습니다.
- **광학 고려 레이아웃** — 하프 미러의 광 투과율을 고려하여 고대비 검정 배경 테마와 CSS Flexbox/Grid 레이아웃을 설계함으로써, 반사면을 투과한 정보가 선명하게 읽히도록 했습니다.

#### 4. 하드웨어 시스템 통합 및 기구 제작
- **시스템 아키텍처** — 라즈베리 파이 3B+, 카메라, 마이크, 모니터 간의 연결을 전력 예산 및 발열 관리를 고려하여 구성했습니다.
- **물리적 프로토타이핑** — 알루미늄 프로파일과 매직 미러 글라스를 직접 가공하여 프레임을 제작하고, 디스플레이 휘도를 튜닝하여 반사면이 거울과 디스플레이 기능을 동시에 수행하도록 했습니다.

### 💡 주요 성과

- **알고리즘 수준의 깊이** — 라이브러리 단순 활용을 넘어 LBPH 특징 추출 원리를 이해하고, 임베디드 배포를 위한 최적화를 수행했습니다.
- **풀스택 엔지니어링** — 하드웨어 센서 제어 → Python 백엔드 → JavaScript 프론트엔드에 이르는 전체 시스템 사이클을 1인 개발자로 완주했습니다.
- **문제 해결 역량** — 조명 환경에 따른 얼굴 인식 정확도 편차를 학습 데이터 보강과 임계값(Threshold) 튜닝으로 해결했습니다.

<div align="right"><a href="#-english">🇺🇸 View in English ↑</a></div>
