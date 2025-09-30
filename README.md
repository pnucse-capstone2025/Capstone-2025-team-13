
<p align="center">
  <img src="https://github.com/user-attachments/assets/4a763cd4-2ed0-481b-aebc-1cd9fb60c5bc" style="width: 40%; max-width: 1000px;" alt="image" />
</p>

# 멀티 클라우드 인프라 기반 연합학습 환경 구축 플랫폼

> 멀티 클라우드 환경에서 안전하고 효율적인 연합학습을 위한 플랫폼

---

## 1. 프로젝트 배경

### 1.1. 배경 소개

#### - 연합학습이란?
- **연합학습(Federated Learning)** 은 참여자(Client)와 집계자(Aggregator)로 구성된 분산학습 기술
- 기존의 중앙 집중형 기계학습(Machine Learning)과 달리 학습 데이터를 중앙 서버로 모으지 않고 각 참여자의 로컬 환경에서 모델을 학습한 후 **모델의 파라미터만 집계자에게 전송**하고, 원본 데이터는 로컬 환경에 유지
- 이러한 연합학습의 특성은 데이터 유출 위험을 감소시켜, 민감한 데이터를 다루는 의료, 제약, 스마트시티 등의 분야에서 활발하게 활용

#### - 멀티 클라우드란?
- **멀티 클라우드(Multi-Cloud)** 는 이형의 클라우드 플랫폼(퍼블릭 클라우드, 프라이빗 클라우드)을 통합하여 단일 클라우드 플랫폼처럼 활용할 수 있는 기술
- 이를 통해 **클라우드 벤더 종속성을 탈피**하고, **각 클라우드 플랫폼의 장점을 조합**할 수 있는 전략 수립 가능

#### - 멀티 클라우드 + 연합학습
- 멀티 클라우드와 연합학습을 결합한 플랫폼은 **개별 클라우드에서 획득할 수 있는 장점(비용 효율성, 접근성, 보안성 등)을 적용**하여 구축 가능
- ex) 개인의 민감한 의료 정보와 같이 강력한 보안성을 요구하는 경우 데이터를 프라이빗 클라우드에 저장하여 보안 강화, 다수의 데이터를 집계했을 때 가치를 발휘하는 질병 통계와 같은 정보는 퍼블릭 클라우드에 저장하여 접근성 및 활용도 높이는 전략 수립 

### 1.2. 국내외 시장 현황 및 문제점

#### (1) 비용 및 지연 최적화 부재

<img src="https://github.com/user-attachments/assets/cefcc7c1-a191-45a8-b5c3-0345610de230" alt="비용 및 지연 최적화 부재" width="55%">

> 기존 클라우드 기반 연합학습의 경우, **단일 클라우드 플랫폼**에 한정되어 연합학습을 수행한다.  </br>이로인해 **리전별 비용 정책 차이와 네트워크 지연(latency)** 을 고려하지 못한다.
학습 참여자가 물리적으로 멀리 떨어져 있는 경우, 모델 파라미터 전송에 지연이 발생하여 **학습 속도가 저하**된다. 또한 비용이 높은 리전에 집계자가 배포되면 **클라우드 비용이 불필요하게 증가**한다.

#### (2) 보안 취약성 및 데이터 프라이버시 문제
<img src="https://github.com/user-attachments/assets/a6d5c405-913e-48eb-8c44-c7f59e460df1" alt="보안 취약성" width="50%">

> 기존 클라우드 기반 연합학습의 경우, 단일 클라우드 플랫폼만 사용하여, 클라우드 플랫폼에 **학습 데이터의 업로드가 요구**된다.
**학습 데이터가 클라우드 인프라 및 네트워크 환경에 노출**됨에 따라 세션 하이제킹, 중간자 공격(MITM), 무단 접근 등의 보안 문제가 발생할 수 있다.

#### (3) 동적 오케스트레이션 부재
<img src="https://github.com/user-attachments/assets/667f004b-9077-4a82-a394-823df0583052" alt="동적 오케스트레이션 부재" width="50%">


### 1.3. 필요성과 기대효과
#### **필요성**
#### **기대효과 ** 

## 2. 개발 목표

### 2.1. 목표 및 세부 내용
(1) 클라우드 별 비용 및 지연 시간을 고려한 멀티 클라우드 기반 연합학습 환경 구축

(2) 연합학습 집계자 - 연합학습 참여자 계층 기반의 멀티 클라우드 지원 연합학습 방법 도출

(3) 연합학습 참여자 모니터링을 통한 동적 태스크 오케스트레이션 기술 구현

### 2.2 기존 서비스 대비 차별성

### 2.3. 사회적 가치 도입 계획
- **공공성 강화**: 의료·교육·금융 등 민감 데이터 기반 사회 문제 해결 지원  
- **지속 가능성 확보**: 특정 벤더 종속을 피하고 멀티 클라우드 활용으로 장기적 확장성 제공  

---

## 3. 시스템 설계

### 3.1. 유스케이스 다이어그램

<img width="60%" alt="유스케이스 다이어그램" src="https://github.com/user-attachments/assets/ca75fb9a-7299-439c-a76e-514773fffbcd" />


### 3.2. 시스템 구성도
<p align="center">
  <img src="https://github.com/user-attachments/assets/93b444a4-09e1-4028-991e-883de5102451" alt="시스템 아키텍처" width="90%">
</p>

본 프로젝트에서는 **퍼블릭 클라우드와 프라이빗 클라우드의 기능을 명확히 구분하여 연합학습을 수행할 수 있는 멀티 클라우드 기반 연합학습 시스템**을 구축한다.  

- 퍼블릭 클라우드에는 **연합학습 집계자(Aggregator)** 와 **글로벌 모델**이 배치되어, 모델 파라미터 집계와 글로벌 모델 업데이트를 담당한다.  
- 프라이빗 클라우드(OpenStack 기반)에는 **로컬 모델, 연합학습 참여자 VM, 학습 데이터셋**이 배치되어, 각 참여자는 로컬 환경에서 개별적으로 학습을 수행한다.  
- 학습된 파라미터는 퍼블릭 클라우드의 집계자에게 전송되며, 집계자는 이를 통합하여 글로벌 모델을 개선한다.  

이러한 계층 구조를 통해 데이터는 프라이빗 클라우드 내부에 안전하게 유지되면서도, 퍼블릭 클라우드의 **확장성·접근성**을 활용한 효율적인 연합학습을 지원한다.

#### 시스템 핵심 모듈
- **Aggregator Deployment Optimizer**  
  사용자 요구사항 기반 최적 집계자 명세(클라우드 리전, 스펙) 추천 및 배포를 통한 비용·학습시간 최적화  

- **Cloud Authenticator**  
  멀티 클라우드 연동을 위한 클라우드 인증 정보 관리 및 인증 정보 기반 연합학습 참여자 등록 지원  

- **Federated Learning Initializer**  
  연합학습 집계자 - 연합학습 집계자를 연계한 연합학습 수행을 위해 환경 설정(라이브러리 설치, 환경 변수, 학습 코드) 및 학습 수행 명령 전달  

- **Dynamic Task Orchestrator**  
  VM 자원 상태·장애 여부 기반 작업 할당, 실패 시 재시도로 안정성 보장  

- **Model Manager**  
  라운드별 글로벌 모델 관리, 저장·평가 지표 모니터링, 모델 다운로드 지원  

### 3.3. 사용 기술
| 분류 | 기술 |
| --- | --- |
| **Frontend** | Next.js 14, TypeScript, Tailwind CSS |
| **Backend** | Go (Gin) |
| **Cloud Platform** | AWS, GCP, OpenStack |
| **Infrastructure** | Terraform, Docker, Docker Compose |
| **Monitoring** | Prometheus, Grafana |
| **ML/AI Framework** | PyTorch, TensorFlow |
| **Federated Learning**|  Flower (Federated Learning) |
| **MLOps** | MLflow |
| **Database** | PostgreSQL |

---

## 4. 개발 결과

### 4.1 전체 시스템 흐름도
<img width="1457" height="368" alt="image" src="https://github.com/user-attachments/assets/d165ae7e-2c41-4939-94a7-02c361da233d" />

### 4.2 기능 설명
---

## 5. 설치 및 실행 방법

### 사전 요구사항

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
```
---

### 6. 소개 자료 및 시연 영상
#### 6.1 프로젝트 소개 자료

#### 6.2 시연 영상
[![뭉게구름 졸업과제 영상](http://img.youtube.com/vi/KugrTo0gUVo/0.jpg)](https://youtu.be/KugrTo0gUVo)

---

### 7. 팀 구성
#### 7.1. 팀원별 소개 및 역할 분담

| Profile | Role                                | Email | GitHub |
|:------:|:------------------------------------|:------|:--------|
| <p align="center"><img src="https://github.com/Jeon-Jinhyeok.png?size=100" width="80"/><br/><strong>전진혁</strong></p> | Team Leader / Federated Learning & System Architect | aqwstn@gmail.com | [@Jeon-Jinhyeok](https://github.com/Jeon-Jinhyeok) |
| <p align="center"><img src="https://github.com/kim-minkyoung.png?size=100" width="80"/><br/><strong>김민경</strong></p> | Backend Developer, CloudOps | decomin02@naver.com | [@Kim-Minkyoung](https://github.com/kim-minkyoung) |
| <p align="center"><img src="https://github.com/JAEIL1999.png?size=100" width="80"/><br/><strong>박재일</strong></p> | Backend Developer, MLOps | pkyj040410@gmail.com | [@JAEIL1999](https://github.com/JAEIL1999) |

### 7.2 팀원 별 느낀점

---

### 8. 참고 문헌 및 출처
[1]  B. McMahan, E. Moore, D. Ramage, S. Hampson, and B. A. y Arcas, "Communication-Efficient Learning of Deep Networks from Decentralized Data," Proceedings of the 20th International Conference on Artificial Intelligence and Statistics (AISTATS), PMLR 54, pp. 1273-1282, Apr. 2017.

[2] J. Dean, G. Corrado, R. Monga, K. Chen, M. Devin, Q. Le, M. Mao, M. Ranzato, A. Senior, P. Tucker, K. Yang, and A. Ng, "Large Scale Distributed Deep Networks," Proceedings of the 25th International Conference on Neural Information Processing Systems (NeurIPS), pp. 1223-1231, Dec. 2012.

[3] L. Yuan, et al., "Decentralized federated learning: A survey and perspective," IEEE Internet of Things Journal, vol. 11, no. 21, pp. 34617-34638, 2024.

[4] J. Hong, T. Dreibholz, J. A. Schenkel, and J. A. Hu, “An Overview of Multi-cloud Computing,” Web, Artificial Intelligence and Network Applications, pp. 1055-1068, 2019.

[5] J. Alonso, et al., "Understanding the challenges and novel architectural models of multi-cloud native applications – a systematic literature review," Journal of Cloud Computing, vol. 12, no. 1, p. 6, 2023.

[6] AWS, “클라우드 컴퓨팅 서비스 - Amazon Web Services(AWS),” [Online]. Available: https://aws.amazon.com. [Accessed: Sep. 11, 2025].

[7] Microsoft, “Azure란? | Microsoft Azure,” [Online]. Available: https://azure.microsoft.com/ko-kr/resources/cloud-computing-dictionary/what-is-azure. [Accessed: Sep. 11, 2025].

[8] Google, “클라우드 컴퓨팅 서비스 | Google Cloud,” [Online]. Available: https://cloud.google.com.  [Accessed: Sep. 11, 2025].

[9] IBM, “Welcome to IBM Federated Learning — ibm-federated-learning,” [Online]. Available: https://ibmfl-api-docs.res.ibm.com. [Accessed: Sep. 11, 2025].

[10] AWS, “Amazon SageMaker AI Documentation,” [Online]. Available: https://docs.aws.amazon.com/sagemaker. [Accessed: Sep. 11, 2025].

[11] Google, “Vertex AI 문서 | Google Cloud,” [Online]. Available: https://cloud.google.com/vertex-ai/docs. [Accessed: Sep. 11, 2025].

[12] FedML, “TensorOpera® Documentation,” [Online]. Available: https://doc.fedml.ai/ [Accessed: Sep. 11, 2025].

[13] J. Proudman, “Openstack Docs: 2025.1,” [Online]. Available: https://docs.openstack.org. [Accessed: Sep. 11, 2025].

[14] Prometheus Authors, “Overview | Prometheus,” [Online]. Available: https://prometheus.io/docs. [Accessed: Sep. 13, 2025].

[15] Grafana, “Technical documentation | Grafana Labs,” [Online]. Available: https://grafana.com/docs. [Accessed: Sep. 11, 2025].

[16] Hashicorp, “Terraform | Terraform | HashiCorp Developer,” [Online]. Available: https://developer.hashicorp.com/terraform. [Accessed: Sep. 11, 2025].

[17] Flower, “Flower Documentation,” [Online]. Available: https://flower.dev/docs. [Accessed: Sep. 11, 2025].

[18] MLflow, “MLflow,” [Online]. Available: https://mlflow.org. [Accessed: Sep. 11, 2025].

[19] PyTorch, “PyTorch documentation - PyTorch 2.8 documentation,” [Online]. Available: https://pytorch.org/docs. [Accessed: Sep. 11, 2025].

[20] TensorFlow, “TensorFlow,” [Online]. Available: https://www.tensorflow.org. [Accessed: Sep. 11, 2025].

[21] Docker, “Docker Docs,” [Online]. Available: https://docs.docker.com. [Accessed: Sep. 11, 2025].

[22] J.Liu, and X.Chen, “An Improved NSGA-II Algorithm Based on Crowding Distance Elimination Strategy,” International Journal of Computational Intelligence Systems, Vol.12, No.2, pp.513-518, 2019.

[23] Z.Osika, P.Koch, and T.Wagner, “What lies beyond the Pareto front? A survey on decision-support methods for multi-objective optimization,” in arXiv preprint, pp.1-9, 2023.

[24] Kaggle, “Covid-19 Image Dataset,” [Online]. Available: https://www.kaggle.com/datasets/pranavraikokte/covid19-image-dataset/data. [Accessed: Sep. 11, 2025].

[25] N. Gavric, A. Shalaginov, A. Andrushevich, A. Rumsch, and A. Paice, "Enhancing International Data Spaces Security: A STRIDE Framework Approach," Preprints, 2024.

[26] ALI-POUR, Amir, et al. Towards a distributed federated learning aggregation placement using particle swarm intelligence. arXiv preprint arXiv:2504.16227, 2025.


### 🎯 해결하고자 하는 문제

- **클라우드 벤더 종속성**: 특정 클라우드 플랫폼에 종속되어 발생하는 비용 및 유연성 제약
- **비용 최적화 부재**: 클라우드 리전별 비용 차이와 네트워크 지연을 고려하지 않은 비효율적 배치
- **보안 취약성**: 민감한 데이터가 퍼블릭 클라우드에 노출되는 위험
- **동적 태스크 관리 부재**: 참여자 상태를 고려하지 않은 정적 작업 할당으로 인한 학습 실패

### 🏗️ 계층형 아키텍처

### 1) 퍼블릭 클라우드 계층

- **연합학습 집계자**: 모델 파라미터 수집 및 통합
- **글로벌 모델**: 라운드별 모델 저장 및 관리
- **높은 접근성과 확장성** 제공

### 2) 프라이빗 클라우드 계층 (OpenStack 기반)

- **학습 데이터**: 민감 정보 안전 보관
- **연합학습 참여자**: 로컬 모델 학습 수행
- **완전한 데이터 격리** 보장


### 💻 기술 스택


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


# PostgreSQL & 모니터링 서비스 실행
docker-compose up -d postgres prometheus grafana
```
