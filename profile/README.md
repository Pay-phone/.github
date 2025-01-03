# 📱 **Payphone**: 금융 서비스 플랫폼

---

## 🌟 **서비스 소개**

**Payphone**은 사용자들에게 간편하고 효율적인 금융 서비스를 제공하기 위해 설계된 **금융 서비스 플랫폼**입니다. 회원가입, 로그인, 가상 계좌 생성, 송금 등 금융권 필수 기능을 구현하였으며, **AWS**를 활용한 클라우드 환경에서 운영됩니다.

---

## 🚀 **핵심 기능**

### 🔐 **1. 사용자 인증**
- **JWT 기반 회원가입 및 로그인**: 안전한 인증/인가 처리.
- **Session 관리**: 새로고침 시에도 유지되는 상태 복구.

### 🏦 **2. 가상 계좌 관리**
- **계좌 생성 및 조회**: 사용자별 가상 계좌 생성.
- **상세 정보 제공**: 잔액, 거래 내역 조회 가능.

### 💸 **3. 송금 기능**
- **안정적인 송금 트랜잭션 처리**:
  - 송금자 잔액 감소와 수신자 잔액 증가를 트랜잭션으로 처리.
  - 송금 실패 시 롤백 지원.

### ☁️ **4. AWS 기반 배포**
- **프론트엔드**: S3 + CloudFront를 활용한 정적 파일 호스팅 및 HTTPS 지원.
- **백엔드**: Lambda와 API Gateway를 통한 서버리스 구조.
- **CI/CD**: GitHub Actions로 자동화된 빌드 및 배포.

---

## 💎 **프로젝트 포인트**

| **특징**                     | **설명**                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------|
| **안전성과 신뢰성**           | JWT를 활용한 인증 및 트랜잭션 처리.                                                        |
| **클라우드 기반 운영 경험**   | AWS S3, Lambda, API Gateway 등 클라우드 친화적 설계.                                       |
| **핵심 금융 서비스 구현 경험** | 송금, 계좌 관리 등 금융 서비스 필수 기능 설계 및 트랜잭션 무결성 보장.                    |
| **UI/UX 개선**               | 송금 결과 및 계좌 내역을 시각화하고 직관적인 인터페이스 제공.                              |

---

## 🛠 **기술 스택**

| **파트**      | **기술**                                                                                      |
|---------------|-----------------------------------------------------------------------------------------------|
| **Backend**   | Spring Boot, MyBatis, MySQL, AWS Lambda                                                      |
| **Frontend**  | Vue.js (Vite 기반), Pinia (상태 관리), Chart.js                                              |
| **CI/CD**     | GitHub Actions, AWS S3, AWS API Gateway, AWS CloudFront                                      |

---

## 📂 **프로젝트 구조**

```plaintext
Payphone/
├── backend/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   ├── resources/
│   ├── pom.xml
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── views/
│   │   ├── store/
│   ├── package.json
│
├── README.md
```

---

## 📦 **설치 및 실행 방법**

### 1️⃣ **Backend**

1. Spring Boot 프로젝트 설정:
    ```bash
    cd backend
    mvn clean install
    mvn spring-boot:run
    ```

2. MySQL 데이터베이스 설정:
    - `application.yml`에 DB 설정 추가.
    - 초기 테이블 생성 및 데이터 마이그레이션.

---

### 2️⃣ **Frontend**

1. Vue.js 프로젝트 설정:
    ```bash
    cd frontend
    npm install
    npm run dev
    ```

2. 빌드 및 S3 배포:
    ```bash
    npm run build
    aws s3 sync dist/ s3://your-bucket-name
    ```

---

### 3️⃣ **CI/CD**

- **GitHub Actions**를 활용한 자동 빌드 및 배포 설정.

---

## 📈 **향후 확장 계획**

- **모니터링**:
  - AWS CloudWatch와 Grafana를 활용한 성능 모니터링.
- **보안 강화**:
  - AES 데이터 암호화.
  - 비정상 트래픽 탐지 및 차단 (AWS GuardDuty).
- **추가 기능**:
  - 사용자 신용 점수 조회.
  - 투자 시뮬레이션 기능.

---

## ✍️ **작성자**

- **Jiwoo**

