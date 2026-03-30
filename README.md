# 🪞 Intelligent Smart Mirror
> **얼굴 인식 및 음성 인식을 결합한 개인 맞춤형 지능형 거울 (졸업 작품)**

일상적인 거울에 IoT 기술과 AI 알고리즘을 접목하여, 사용자를 식별하고 음성 명령에 따라 개인화된 정보를 제공하는 **라즈베리 파이 기반 스마트 시스템**입니다.

---

## 📋 프로젝트 개요 (Project Overview)
단순한 정보 출력을 넘어, OpenCV의 **LBPH 알고리즘**을 통한 사용자 식별과 **Google STT** 기반의 음성 인터랙션을 통합한 지능형 비서 솔루션을 개발했습니다. 하드웨어 설계부터 소프트웨어 파이프라인 구축까지 전 과정을 수행하며 시스템 통합 역량을 확보했습니다.

* **역할:** 메인 개발자 (시스템 설계, 알고리즘 구현 및 하드웨어 통합)
* **핵심 기술:** LBPH 기반 실시간 얼굴 인식, Google Cloud STT 엔진 연동, 임베디드 시스템 최적화

## 🛠 기술 스택 (Tech Stack)
- **Language:** Python, JavaScript
- **Frontend:** HTML, CSS, JavaScript (Vanilla JS)
- **Libraries:**
    - **Vision:** OpenCV, Local Binary Patterns Histograms (LBPH)
    - **Voice:** Google Speech Recognition (STT)
- **Hardware:** Raspberry Pi 3B+, Camera Module (Logitech C920), USB Mic/Speaker, Magic Mirror Glass, Aluminum Profile

---

## 🚀 Core Engineering Tasks

### 1. LBPH 알고리즘 기반 실시간 얼굴 인식 (Vision)
저사양 임베디드 환경(Raspberry Pi)에서도 안정적인 식별이 가능하도록 경량 알고리즘을 적용했습니다.
- **데이터셋 구축 및 학습:** OpenCV의 `haarcascade_frontalface_default.xml`을 활용해 사용자 얼굴을 검출하고, 수집된 데이터를 **LBPH(Local Binary Patterns Histograms)** 모델로 학습시켜 개인별 고유 특징 벡터를 생성했습니다.
- **사용자 맞춤형 프로필 매칭:** 실시간 카메라 피드에서 인식된 ID와 매칭되는 사용자 전용 대시보드(날씨, 일정, 인사말 등)를 활성화하는 트리거 로직을 구현했습니다.

### 2. Google STT 기반 음성 인식 시스템 (Voice)
사용자의 자연어 명령을 해석하고 시스템을 제어하는 인터페이스를 구축했습니다.
- **음성 명령 처리 파이프라인:** **Google Cloud Speech-to-Text API**를 연동하여 마이크 입력을 텍스트로 변환하고, 특정 키워드(날씨, 뉴스 등)에 따라 모듈을 제어하는 백엔드 로직을 Python으로 구현했습니다.
- **실시간 상호작용:** 음성 입력을 통한 화면 전환 및 정보 요청 기능을 구현하여 핸즈프리 사용자 경험(UX)을 극대화했습니다.

### 3. 웹 기반 대시보드 및 모듈 커스터마이징 (Frontend)
- **Vanilla JS 기반 UI 설계:** 프레임워크 없이 순수 자바스크립트를 활용하여 시계, 날씨, 구글 캘린더, 뉴스 헤드라인 등의 정보를 실시간으로 렌더링하는 경량 대시보드를 구축했습니다.
- **레이아웃 최적화:** 하프 미러(Half Mirror)의 투과율을 고려하여 고대비(High Contrast) 검정 배경 테마와 CSS Flexbox/Grid를 활용한 정보 배치를 설계했습니다.

### 4. 하드웨어 시스템 통합 및 기구 설계
- **시스템 아키텍처 설계:** 라즈베리 파이 3B+를 중심으로 카메라, 마이크, 모니터를 유기적으로 연결하고 전력 관리 및 발열을 고려한 설계를 수행했습니다.
- **물리적 프로토타이핑:** 알루미늄 프로파일과 매직 미러 글라스를 활용하여 하드웨어 프레임을 직접 제작하고, 디스플레이 광량을 조절하여 거울과 정보 출력 기능이 공존하도록 튜닝했습니다.

---

## 💡 Technical Achievements
- **알고리즘 구현 능력:** 라이브러리의 단순 활용을 넘어 LBPH 특징 추출 원리를 이해하고 실제 임베디드 시스템에 적용 및 최적화
- **풀스택 엔지니어링:** 하드웨어 센서 제어부터 백엔드 로직(Python), 프론트엔드 시각화(JS)까지 연결되는 전체 시스템 사이클 경험
- **문제 해결 역량:** 조명 환경에 따른 얼굴 인식 정확도 편차를 학습 데이터 보강 및 임계값(Threshold) 조정으로 해결
