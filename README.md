## 1. 프로젝트 소개

### ☁️ **멀티 클라우드 환경 기반 연합학습 플랫폼**

기존 단일 클라우드 기반 연합학습의 한계(비용, 지연시간, 보안)를 해결하기 위해 여러 클라우드를 통합 활용하는 연합학습 플랫폼입니다.

### ✨ 주요 특징

- **스마트 클라우드 선택**: 비용과 지연시간을 고려한 최적 클라우드 배치
- **하이브리드 보안 전략**: 민감 데이터는 프라이빗, 일반 데이터는 퍼블릭 클라우드 활용
- **동적 오케스트레이션**: 참여자 상태 모니터링을 통한 실시간 태스크 관리
- **벤더 종속성 탈피**: 다중 클라우드 환경으로 특정 업체 의존도 최소화

### 🏥 사용 사례

COVID-19 폐 이미지 진단 CNN 모델 학습

## 2. 팀소개

| Profile | Role                                | Email | GitHub |
|:------:|:------------------------------------|:------|:--------|
| <p align="center"><img src="https://github.com/Jeon-Jinhyeok.png?size=80" width="80"/><br/><strong>전진혁</strong></p> | Team Leader / AI & System Architect | aqwstn@gmail.com | [@Jeon-Jinhyeok](https://github.com/Jeon-Jinhyeok) |
| <p align="center"><img src="https://github.com/kim-minkyoung.png?size=80" width="80"/><br/><strong>김민경</strong></p> | Backend Developer, CloudOps | decomin02@naver.com | [@Kim-Minkyoung](https://github.com/kim-minkyoung) |
| <p align="center"><img src="https://github.com/JAEIL1999.png?size=80" width="80"/><br/><strong>박재일</strong></p> | Backend Developer, MLOps | pkyj040410@gmail.com | [@JAEIL1999](https://github.com/JAEIL1999) |



## 3. 시스템 구성도

<img src="https://github.com/user-attachments/assets/93b444a4-09e1-4028-991e-883de5102451" alt="시스템 아키텍처" width="800">



본 시스템은 퍼블릭 클라우드와 프라이빗 클라우드의 장점을 결합한 하이브리드 연합학습 플랫폼입니다.

**🔹 퍼블릭 클라우드 계층**

- 연합학습 집계자와 글로벌 모델 배치
- 모델 파라미터 집계 및 글로벌 모델 업데이트 담당
- 높은 접근성과 확장성 제공

**🔹 프라이빗 클라우드 계층 (OpenStack 기반)**

- 로컬 모델, 연합학습 참여자, 학습 데이터셋 배치
- 민감한 데이터를 안전하게 보호하면서 로컬 학습 수행
- 모델 파라미터만 퍼블릭 클라우드로 전송

### 🔧 핵심 모듈

**Aggregator Deployment Optimizer** - 사용자 요구사항 기반 최적 집계자 배치로 비용 및 지연시간 최적화

**Cloud Authenticator** - 멀티 클라우드 인증 정보 관리 및 참여자 등록

**Federated Learning Initializer** - 연합학습 환경 자동 설정 (라이브러리 설치, 환경 변수, 학습 코드 배포)

**Dynamic Task Orchestrator** - 참여자 리소스 상태 모니터링을 통한 동적 작업 할당 및 장애 복구

**Model Manager** - 라운드별 글로벌 모델 관리, 평가 지표 모니터링, 사용자 맞춤 모델 다운로드 지원



## 4. 소개 및 시연 영상

TODO

## 5. 설치 및 사용법

### 1. 환경 변수 설정

**백엔드 환경 변수** (`backend/.env`)

```
DB_HOST=
DB_USER=
DB_PASSWORD=
DB_NAME=
DB_PORT=
GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=
```

**프론트엔드 환경 변수** (`frontend/.env.local`)

```
NEXT_PUBLIC_API_URL=
```

### 2. 실행

```bash
cd frontend
npm install
npm run dev:all
```

**+) 사전 요구사항:** PostgreSQL, GitHub OAuth App, AWS/GCP 계정, OpenStack 환경
