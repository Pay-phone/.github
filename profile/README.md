# Payphone: Financial Service Platform

## **서비스 소개**

**Payphone**은 사용자가 금융 서비스를 간편하게 사용할 수 있도록 설계된 **금융 서비스 플랫폼**입니다. 회원 가입, 로그인, 가상 계좌 생성, 송금 등의 주요 금융 기능을 구현하였으며, AWS를 활용하여 클라우드 환경에서 안정적이고 효율적으로 운영됩니다. 이 프로젝트는 금융권 IT 시스템에 필요한 기술적 역량을 어필할 수 있는 실질적 경험을 제공합니다.

---

## **핵심 기능**

### 1. **사용자 인증**

- **JWT 기반 회원가입 및 로그인**
    - 안전한 인증/인가 처리.
    - 회원가입 시 기본 사용자 정보를 등록하고 JWT 토큰 발급.

### 2. **가상 계좌 관리**

- **계좌 생성 및 조회**
    - 사용자 별로 가상 계좌를 생성.
    - 계좌의 잔액 정보를 포함한 상세 조회 기능.

### 3. **송금 기능**

- **송금 트랜잭션 처리**
    - 송금자 잔액 감소 및 수신자 잔액 증가를 트랜잭션으로 처리.
    - 송금 실패 시 롤백 기능.

### 4. **AWS 기반 배포**

- **프론트엔드:** AWS S3와 CloudFront를 통한 정적 파일 호스팅 및 HTTPS 적용.
- **백엔드:** AWS Lambda와 API Gateway를 활용한 서버리스 배포.
- **CI/CD:** GitHub Actions로 자동화된 빌드 및 배포.

---

## **프로젝트 포인트**

1. **안전성과 신뢰성을 강조한 설계**
    - JWT를 활용한 인증/인가 및 트랜잭션 처리.
    - AWS CloudFront로 HTTPS 지원 및 데이터 암호화.
2. **클라우드 기반 운영 경험**
    - AWS S3, Lambda, API Gateway, CloudFront를 활용한 **클라우드 친화적 설계**.
    - GitHub Actions를 활용한 CI/CD로 **자동화된 배포 환경** 구축.
3. **핵심 금융 서비스 구현 경험**
    - 송금, 계좌 관리 등 금융권에서 필수적인 기능 설계.
    - 트랜잭션 처리 및 데이터 무결성 보장.
4. **UI/UX 개선으로 사용자 경험 향상**
    - 송금 결과 및 계좌 내역 시각화 (Chart.js 활용).
    - 직관적이고 간단한 사용자 인터페이스.

---

## **기술 스택**

### **Backend**

- Spring Boot
- MyBatis
- MySQL
- AWS Lambda

### **Frontend**

- Vue.js (Vite 기반)
- Pinia (상태 관리)
- Chart.js

### **CI/CD 및 배포**

- GitHub Actions
- AWS S3
- AWS API Gateway
- AWS CloudFront

---

## **프로젝트 구조**

### **디렉토리 구조**

```
project-root/
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

## **설치 및 실행 방법**

### **1. Backend**

1. Spring Boot 프로젝트 설정:
    
    ```bash
    cd backend
    mvn clean install
    mvn spring-boot:run
    
    ```
    
2. MySQL 데이터베이스 구성:
    - `application.yml` 파일에 데이터베이스 설정 추가.
    - 초기 테이블 생성 및 데이터 마이그레이션.

### **2. Frontend**

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
    

### **3. CI/CD**

- GitHub Actions를 활용한 자동 빌드 및 배포.

---

## **향후 확장 계획**

1. **최적화 및 모니터링 추가**
    - AWS CloudWatch와 Grafana를 활용한 성능 모니터링.
    - Redis 캐싱을 통해 API 응답 속도 개선.
2. **고급 보안 기능**
    - AES 데이터 암호화.
    - 비정상 트래픽 탐지 및 차단 (AWS GuardDuty).
3. **추가 금융 서비스**
    - 사용자 신용 점수 조회.
    - 투자 시뮬레이션 기능.

---

## **작성자**

- Jiwoo
