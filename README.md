## 💡 소개

### **1. 관측 가능성(Observability) 시스템 설계 및 구축**
MSA 환경에서 Prometheus, Grafana, Loki를 활용한 관측 가능성 시스템을 직접 설계하고 구축했습니다. AOP 기반 커스텀 로깅 라이브러리를 개발하여 비즈니스 도메인별 로그를 자동 분류했으며, 모든 MSA 요청에 requestId를 전파하는 분산 추적 시스템을 구현하여 7개 서비스의 엔드투엔드 흐름을 추적할 수 있게 만들었습니다. Fluent Bit, Kinesis, Kinesis Data Analytics를 연동한 실시간 로그 파이프라인 구축으로 **디버깅 시간을 80% 단축**하고, 장애 발생 시 근본 원인을 즉시 파악할 수 있는 운영 기반을 마련했습니다.

### **2. DevOps 파이프라인 자동화를 통한 개발 생산성 극대화**
인프라 설계부터 배포, 운영까지 DevOps 전 과정을 직접 수행하며 개발 생산성을 극대화합니다. GitHub Actions의 git diff와 matrix 전략을 활용하여 변경된 서비스만 병렬로 자동 배포하는 CI/CD 파이프라인을 구축했으며, **전체 배포 시간을 1시간에서 25분으로 58% 단축**했습니다. AWS ECS 환경에서 Blue/Green 무중단 배포 시스템을 구현했습니다.

### **3. 문제의 근본 원인을 해결하는 백엔드 아키텍처 설계 능력**
반복적인 문제를 시스템 레벨에서 해결하는 백엔드 아키텍처 설계 역량을 보유하고 있습니다. 15개 테이블에 60개의 중복 컬럼이 존재하던 문제를 JPA Entity Listener와 Reflection 기반 범용 리포지토리로 해결했으며, **코드 중복률 90% 감소, 주 23건 발생하던 휴먼 에러를 0건으로 만들고, 엔티티 개발 시간을 82% 단축**했습니다. 또한 Cache-Aside 패턴 적용으로 api 응답시간을 90% 개선하여 성능 문제를 아키텍처 개선으로 근본 해결한 경험이 있습니다.

---

## 🎓 교육
- **가톨릭대학교** 컴퓨터공학/중국언어문화학과 (2025.08 졸업, 전공 학점 4.0)
- **하나은행 금융 서비스 개발 부트캠프** 우수 수료 (2024.08 - 2025.02)
- **구름 프로펙트 클라우드 엔지니어링** (2025.07 - 2025.09)

## 📜 자격증
- **정보처리기사** (2023)

---

## 🚀 대표 프로젝트

### **1. MSA 로깅 모니터링 시스템 구축** `2025.09` 
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/Profect-cloud/profect-eatcloud-msa-v2)

**Backend + DevOps | EKS, Kinesis, Kinesis Data Analytics, Loki, Grafana**

<details>
<summary><b>프로젝트 상세보기</b></summary>

#### 📈 주요 성과
```
✨ 개발 생산성 300% 향상: 커스텀 로깅 라이브러리로 애노테이션 하나로 로그 분류 자동화
🔍 분산 추적: 7개 MSA에서 Request ID 하나로 전체 추적 가능 → 디버깅 시간 80% 단축
📊 통합 모니터링: Prometheus + Loki + Grafana 스택 구축 → 장애 대응 70% 단축
```

#### 🔧 핵심 구현
- **커스텀 로깅 라이브러리**: AOP 기반 도메인별 자동 로그 분류 (`@StatefulLog`, `@StatelessLog`, `@RecommendationLog`)
- **분산 추적 시스템**: MDC + Filter로 16자리 Request ID 생성/전파, Kafka 헤더 전파로 비동기 처리 추적
- **실시간 로그 파이프라인**: Fluent Bit → Kinesis (3개 타입별 스트림) → Kinesis Data Analytics 듀얼 스트림 처리
- **통합 모니터링**: Helm Chart 기반 Loki/Prometheus/Grafana 표준화 배포, Alert Manager SNS 연동

</details>

---

### **2. MSA 인프라 구축** `2025.08`
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/Profect-cloud/profect-eatcloud-msa-v1)

**Infrastructure Design & DevOps | AWS ECS, GitHub Actions**

<details>
<summary><b>프로젝트 상세보기</b></summary>

#### 📈 주요 성과
```
🚢 배포 시간 58% 단축 (1시간→25분): Git diff 변경 감지 + Matrix 병렬 배포
🔄 무중단 배포: ECS Blue/Green 전환 + 자동 롤백
📦 중복 코드 80% 제거: auto-time/auto-response 공통 라이브러리
```

#### 🔧 핵심 구현
- **CI/CD 자동화**: GitHub Actions Git diff로 변경 서비스만 자동 감지, Matrix 병렬 배포로 시간 단축
- **무중단 배포**: ECS Blue/Green 전환, 헬스체크 실패 시 자동 롤백
- **환경별 설정 관리**: AWS Secrets Manager + Spring Profile로 local/dev/prod 환경 분리

</details>

---

### **3. 배달 주문 관리 플랫폼** `2025.07`
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/Profect-cloud/profect-eatcloud)

**Backend Architecture | JPA, Redis, PostgreSQL**

<details>
<summary><b>프로젝트 상세보기</b></summary>

#### 📈 주요 성과
```
✅ 휴먼 에러 100% 제거: JPA Entity Listener로 TimeData 자동 관리 (주 23건→0건)
⚡ 응답시간 90% 개선 (200ms→20ms): Redis Cache-Aside 패턴
🏗️ 개발 시간 82% 단축: 범용 Repository로 엔티티 개발 45분→8분
```

#### 🔧 핵심 구현
- **JPA Entity Listener 자동화**: UUID 기반 TimeData 중앙 관리, `@PrePersist`/`@PreUpdate`로 생성/수정 시간 자동 설정
- **범용 Repository**: Reflection 기반 동적 쿼리, JOIN FETCH로 N+1 방지, 소프트 삭제 자동화
- **성능 최적화**: Redis Cache-Aside 패턴으로 장바구니 DB 부하 90% 감소

</details>

---

### **4. 라이프온하나 - 금융 슈퍼앱** `2025.01-02`
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/Hanaro-JSON)

**AI Recommendation System | KB-ALBERT, Redis Vector Search, Claude API**

<details>
<summary><b>프로젝트 상세보기</b></summary>

#### 📈 주요 성과
```
🤖 추천 정확도 향상: KB-ALBERT 금융 특화 모델 + 하이브리드 추천 (컨텐츠 70% + 협업 필터링 30%)
📚 용어 접근성 개선: BERT 기반 어려운 용어 자동 추출 + Claude API 실시간 설명
⚡ 응답 속도 개선: Redis Vector Search로 1초 이내 추천, Redis 캐싱으로 DB 부하 90% 감소
```

#### 🔧 핵심 구현
- **KB-ALBERT 벡터 검색**: Redis Stack HNSW 인덱스 기반 유사도 검색, 컨텐츠 기반 + 협업 필터링 하이브리드
- **어려운 용어 추출**: BERT 문맥 분석(70%) + Korpora 빈도 분석(30%) 하이브리드

</details>

---

### **5. 스케줄 하나로 - 상담 통합 관리 플랫폼** `2024.10-12`
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/Hanbang-NeungYo-Baeksook/Schedule-Hanaro-Back)

**Backend | Spring Boot, MySQL, WebSocket**

<details>
<summary><b>프로젝트 상세보기</b></summary>

#### 📈 주요 성과
```
💬 FAQ 추천 시스템: TF-IDF + 코사인 유사도로 유사 질문 자동 추천
🔄 실시간 동기화: WebSocket 기반 대면상담 번호표 실시간 업데이트
```

#### 🔧 핵심 구현
- **FAQ 추천 알고리즘**: TF-IDF 벡터화 + 코사인 유사도로 기존 FAQ 중 유사한 답변 자동 추천
- **실시간 번호표 시스템**: WebSocket을 활용한 대면상담 번호표 실시간 동기화

</details>

---

## 🛠 Tech Stack

<div align="center">

### 💻 Backend & Languages
<p>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" alt="Spring Boot"/>
  <img src="https://img.shields.io/badge/Spring_Cloud-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring Cloud"/>
  <img src="https://img.shields.io/badge/JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white" alt="JPA"/>
  <img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white" alt="Hibernate"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask"/>
</p>

### 🗄️ Database & Cache
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis"/>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="DocumentDB"/>
</p>

### 📡 Streaming & Messaging
<p>
  <img src="https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apache-kafka&logoColor=white" alt="Kafka"/>
  <img src="https://img.shields.io/badge/Amazon_MSK-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="MSK"/>
  <img src="https://img.shields.io/badge/Kinesis_Data_Streams-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="Kinesis"/>
  <img src="https://img.shields.io/badge/Kinesis_Data_Analytics-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="Kinesis Analytics"/>
</p>

### 🤖 AI & Machine Learning
<p>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/🤗_Transformers-FFD21E?style=for-the-badge" alt="Transformers"/>
  <img src="https://img.shields.io/badge/BERT-412991?style=for-the-badge&logo=bert&logoColor=white" alt="BERT"/>
  <img src="https://img.shields.io/badge/Claude_API-8E75B2?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude"/>
  <img src="https://img.shields.io/badge/Redis_Vector_Search-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Vector Search"/>
</p>

### ☁️ Cloud & Infrastructure
<p>
  <img src="https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS"/>
  <img src="https://img.shields.io/badge/Amazon_EKS-FF9900?style=for-the-badge&logo=amazon-eks&logoColor=white" alt="EKS"/>
  <img src="https://img.shields.io/badge/Amazon_ECS-FF9900?style=for-the-badge&logo=amazon-ecs&logoColor=white" alt="ECS"/>
  <img src="https://img.shields.io/badge/Amazon_ECR-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="ECR"/>
  <img src="https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white" alt="S3"/>
  <img src="https://img.shields.io/badge/CloudWatch-FF4F8B?style=for-the-badge&logo=amazon-cloudwatch&logoColor=white" alt="CloudWatch"/>
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes"/>
  <img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=Helm&logoColor=white" alt="Helm"/>
</p>

### 📊 Monitoring & Observability
<p>
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white" alt="Prometheus"/>
  <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana"/>
  <img src="https://img.shields.io/badge/Loki-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Loki"/>
  <img src="https://img.shields.io/badge/Fluent_Bit-49BDA5?style=for-the-badge&logo=fluentbit&logoColor=white" alt="Fluent Bit"/>
</p>

### 📦 Tools
<p>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>
  <img src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=Jira&logoColor=white" alt="Jira"/>
  <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" alt="Slack"/>
</p>

</div>

---

## 🏆 Algorithm

<div align="center">

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=dharmavarsa)](https://solved.ac/dharmavarsa/)

</div>

