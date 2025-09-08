NAFAL (Not A Fake Auction League)
프로젝트 개요

NAFAL은 실시간 경매 기반 마켓플레이스와 포인트/지갑 시스템, 커뮤니티 기능을 제공하는 종합 플랫폼입니다.
사용자는 개인/기업 계정으로 참여할 수 있으며, 상품 등록·입찰·거래를 투명하게 관리할 수 있습니다.

기술 스택

Backend: Spring Boot, MyBatis, MySQL

Frontend: React, Tailwind CSS

Authentication: Spring Security, OAuth2 (Google, Kakao)

DevOps: Tomcat 9, IntelliJ, VSCode

프로젝트 구조
NAFAL/
├── backend/          # Spring Boot 백엔드
├── frontend/         # React 프론트엔드
└── README.md

설치 및 실행
백엔드 설정

backend/env.example 파일을 backend/.env로 복사

backend/application.properties.example 파일을 backend/src/main/resources/application.properties로 복사

환경 변수 설정:

# Google OAuth2
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret

# Kakao OAuth2
KAKAO_CLIENT_ID=your_kakao_client_id
KAKAO_CLIENT_SECRET=your_kakao_client_secret

# Database
DB_HOST=localhost
DB_PORT=3306
DB_NAME=nafaldB
DB_USERNAME=your_username
DB_PASSWORD=your_password

프론트엔드 설정

frontend/env.example 파일을 frontend/.env로 복사

환경 변수 설정:

REACT_APP_API_BASE_URL=http://localhost:8080/NAFAL

데이터베이스 설정

MySQL 데이터베이스 생성

backend/nafaldb.sql 파일 실행하여 테이블 생성

실행
# 백엔드 실행
cd backend
./mvnw spring-boot:run

# 프론트엔드 실행
cd frontend
npm install
npm start

개발 서버

백엔드: http://localhost:8080/NAFAL

프론트엔드: http://localhost:3000

주요 기능

사용자 유형: NAFAL / USER / ADMIN

상품 등록 및 경매 참여

포인트 충전/사용 (Wallet + Transaction 관리)

커뮤니티 게시글, 댓글/대댓글

OAuth2 기반 로그인 (Google, Kakao)

주의사항

.env와 application.properties는 절대 커밋하지 마세요

개인정보(API 키, 비밀번호 등)는 환경 변수로 관리하세요

localhost:8080은 개발 환경 전용입니다

라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.
