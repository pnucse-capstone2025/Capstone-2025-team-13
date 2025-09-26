# 멀티 클라우드 기반 연합학습 플랫폼

> 멀티 클라우드 환경에서 안전하고 효율적인 연합학습을 위한 통합 플랫폼
> 

---

## 1. 프로젝트 소개

기존 단일 클라우드 기반 연합학습의 한계(벤더 종속성, 비용/지연시간 최적화 부재, 보안 취약성)를 극복하기 위해 개발된 **멀티 클라우드 환경 기반 연합학습 플랫폼**입니다.

퍼블릭 클라우드에는 연합학습 집계자를, 프라이빗 클라우드에는 민감한 학습 데이터를 배치하는 하이브리드 구조로 데이터 보안성을 유지하면서도 비용과 성능을 최적화합니다.

### 🎯 해결하고자 하는 문제

- **클라우드 벤더 종속성**: 특정 클라우드 플랫폼에 종속되어 발생하는 비용 및 유연성 제약
- **비용 최적화 부재**: 클라우드 리전별 비용 차이와 네트워크 지연을 고려하지 않은 비효율적 배치
- **보안 취약성**: 민감한 데이터가 퍼블릭 클라우드에 노출되는 위험
- **동적 태스크 관리 부재**: 참여자 상태를 고려하지 않은 정적 작업 할당으로 인한 학습 실패

## 2. 팀소개

| Profile | Role                                | Email | GitHub |
|:------:|:------------------------------------|:------|:--------|
| <p align="center"><img src="https://github.com/Jeon-Jinhyeok.png?size=80" width="80"/><br/><strong>전진혁</strong></p> | Team Leader / AI & System Architect | aqwstn@gmail.com | [@Jeon-Jinhyeok](https://github.com/Jeon-Jinhyeok) |
| <p align="center"><img src="https://github.com/kim-minkyoung.png?size=80" width="80"/><br/><strong>김민경</strong></p> | Backend Developer, CloudOps | decomin02@naver.com | [@Kim-Minkyoung](https://github.com/kim-minkyoung) |
| <p align="center"><img src="https://github.com/JAEIL1999.png?size=80" width="80"/><br/><strong>박재일</strong></p> | Backend Developer, MLOps | pkyj040410@gmail.com | [@JAEIL1999](https://github.com/JAEIL1999) |



## 3. 시스템 구성도

<img src="https://github.com/user-attachments/assets/93b444a4-09e1-4028-991e-883de5102451" alt="시스템 아키텍처" width="800">


### 🏗️ 계층형 아키텍처

### 1) 퍼블릭 클라우드 계층

- **연합학습 집계자**: 모델 파라미터 수집 및 통합
- **글로벌 모델**: 라운드별 모델 저장 및 관리
- **높은 접근성과 확장성** 제공

### 2) 프라이빗 클라우드 계층 (OpenStack 기반)

- **학습 데이터**: 민감 정보 안전 보관
- **연합학습 참여자**: 로컬 모델 학습 수행
- **완전한 데이터 격리** 보장

### 🔧 핵심 모듈

| 모듈 | 설명 | 주요 기능 |
| --- | --- | --- |
| **Aggregator Deployment Optimizer** | 집계자 배치 최적화 | NSGA-II 기반 비용/지연시간 최적화 |
| **Cloud Authenticator** | 멀티 클라우드 인증 관리 | AWS/GCP 인증 정보 통합 관리 |
| **Federated Learning Initializer** | 연합학습 환경 자동화 | 라이브러리 설치, 환경 설정 자동화 |
| **Dynamic Task Orchestrator** | 동적 작업 관리 | 리소스 기반 필터링, 장애 복구 |
| **Model Manager** | 모델 생명주기 관리 | 버전 관리, 성능 모니터링, 다운로드 |

### 💻 기술 스택

| 분류 | 기술 |
| --- | --- |
| **Frontend** | Next.js 14, TypeScript, Tailwind CSS |
| **Backend** | Go (Gin), Python (Flower, PyTorch) |
| **Cloud Platform** | AWS, GCP, OpenStack |
| **Infrastructure** | Terraform, Docker, Docker Compose |
| **Monitoring** | Prometheus, Grafana |
| **ML/AI Framework** | Flower (Federated Learning), PyTorch, TensorFlow |
| **MLOps** | MLflow |
| **Database** | PostgreSQL |

## 4. 소개 및 시연 영상

[![Video Label](http://img.youtube.com/vi/KugrTo0gUVo/0.jpg)](https://youtu.be/KugrTo0gUVo)
> 위 이미지를 클릭하면 유튜브 영상이 재생됩니다.
> 
### ✨ 주요 특징

### 1) 요구사항 맞춤형 집계자 배치 최적화

<img width="663" height="424" alt="image" src="https://github.com/user-attachments/assets/820e949e-e0ad-44e8-8a21-0214996f3254" />

- 사용자 요구사항을 반영한 연합학습 집계자 최적 배포
- 사용자 요구사항: 최대 허용 비용 및 지연시간, 비용-지연시간 가중치 비율
- **NSGA-II 알고리즘** 이용
**=> 클라우드 비용 및 학습시간 최적화**

### 2) 계층 구조 기반 연합학습 수행

<img width="537" height="344" alt="image" src="https://github.com/user-attachments/assets/4f539384-170e-4b05-abda-1263db7c36ed" />


- **퍼블릭 - 프라이빗 클라우드 역할 분리를 기반으로 한 연합학습**
- 프라이빗 클라우드: 평가 데이터를 이용한 모델 학습
- 퍼블릭 클라우드: 파라미터 수집 및 통계 작업
**=> 데이터가 프라이빗 클라우드에 유지되어 데이터 노출 방지**

### 3) 동적 태스크 오케스트레이션

<img width="409" height="215" alt="image" src="https://github.com/user-attachments/assets/3bb2d189-c447-446f-a6b8-cec63be2fe09" />


- 참여자의 가상머신 자원 상태를 실시간 모니터링하여 **적절한 가상머신에 연합학습 할당**
  - 최소 사양 기반 필터링: 컴퓨팅 리소스, 상태
  - 원형 큐 기반 부하 분산

### 4) 멀티 클라우드 통합

- AWS, GCP, OpenStack 동시 지원
- Terraform 기반 인프라 자동화
- 클라우드 간 원활한 연동

### 🏥 사례 연구: COVID-19 진단 모델 학습

- **데이터셋**: Kaggle Covid-19 Image Dataset (정상 환자, COVID-19 확진 환자, 폐렴 환자 폐 X-ray 이미지)
- **시나리오**: 글로벌 의료기관 협력 (유럽, 아시아, 미국 리전에 분산 배치)
- **결과**: 데이터 프라이버시 완전 보장하면서 효율적인 글로벌 모델 학습 달성

### 📊 실험 결과

### 1) 비용 및 성능 최적화 효과

| 시나리오 | 평균 학습 시간 | 월간 비용 | 개선율 |
| --- | --- | --- | --- |
| **최적화 전** | 52.17초 | 38,938원 | - |
| **비용 우선 최적화** | 53초 | 23,026원 | **비용 41% 절감** |
| **지연시간 우선 최적화** | 48.4초 | 31,450원 | **속도 7% 향상, 비용 19% 절감** |

### 2) 동적 태스크 오케스트레이션 효과

| 방식 | 참여자 이탈률 | 연합학습 성공률 |
| --- | --- | --- |
| **무작위 선택** | 60% | 40% |
| **제안 알고리즘** | 0% | **100%** |

## 5. 설치 및 사용법

### 📋 사전 요구사항

- **클라우드 계정**: AWS, GCP
- **OpenStack 환경** (프라이빗 클라우드)
- **GitHub OAuth App** (인증용) (Optional)
- **PostgreSQL** 데이터베이스

### ⚙️ 환경 설정

### 1) 백엔드 환경변수 (`backend/.env`)

```
DB_HOST=
DB_USER=
DB_PASSWORD=
DB_NAME=
DB_PORT=
GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=
```

### 2) 프론트엔드 환경변수 (`frontend/.env.local`)

```
NEXT_PUBLIC_API_URL=
```

### 3) 실행 방법

```bash
cd frontend
npm install
npm run dev:all

# PostgreSQL & 모니터링 서비스 실행
docker-compose up -d postgres prometheus grafana
```
