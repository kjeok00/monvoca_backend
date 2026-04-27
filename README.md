# monVoca Backend
> AI 기술을 접목한 스마트 단어장 및 학습 관리 플랫폼

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.5-6DB33F?style=flat-square&logo=springboot)
![Java](https://img.shields.io/badge/Java-17-007396?style=flat-square&logo=java)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker)

## 📖 프로젝트 소개
**monVoca**는 단순한 텍스트 입력 방식을 넘어 이미지(OCR)를 통해서도 손쉽게 학습 콘텐츠를 생성할 수 있는 스마트 단어장 서비스의 백엔드입니다. 
지능형 번역 서비스와 단어 자동 분류 기능을 제공하여 사용자의 학습 편의성을 극대화하며, 사용자 맞춤형 퀴즈 생성 기능을 통해 체계적인 자가 학습 환경을 지원합니다.

## ✨ 주요 기능
- **📷 OCR 기반 단어 추출:** 이미지 내 텍스트를 자동으로 인식하여 단어장에 신속하게 등록
- **🌐 지능형 번역 서비스:** NAVER Papago API 연동을 통한 고품질 텍스트 및 이미지 번역 지원
- **📝 단어장 및 노트 관리:** 사용자별 학습 노트 생성 및 단어 상세 정보(뜻, 예문 등) 체계적 관리
- **🧠 맞춤형 퀴즈 및 학습:** 학습된 내용을 기반으로 선택형 및 예시 질문을 자동 생성하여 복습 지원
- **📂 단어 자동 분류:** 수집된 단어를 카테고리별로 자동 분류해 직관적인 학습 관리 제공

## 🛠️ 기술 스택
### Framework & Language
- **Java 17**
- **Spring Boot 3.3.5**

### Database
- **MongoDB** (Spring Data MongoDB 활용)

### External API
- **NAVER Papago API** (Text/Image Translation)
- **CLOVA OCR** (Image Text Recognition)

### Infrastructure & Tools
- **Gradle** (Build Tool)
- **Docker / Docker Compose**
- **Springdoc OpenAPI** (Swagger 2.6.0)
- **Lombok, Jackson**

## ⚙️ 실행 방법 (Getting Started)

### 요구 사항
- Java 17 이상
- MongoDB
- Docker (선택 사항)

### 환경 변수 설정
실행 전, 루트 경로 혹은 시스템 환경 변수에 NAVER Papago 및 CLOVA OCR 연동을 위한 API Key 정보가 필요합니다.

### 빌드 및 실행
```bash
# 레포지토리 클론
$ git clone https://github.com/your-repo/monVoca_backend.git
$ cd monVoca_backend

# Gradle 빌드
$ ./gradlew build

# 애플리케이션 실행
$ ./gradlew bootRun
```

### Docker로 실행 (Docker Compose)
```bash
$ docker-compose up -d --build
```

## 📚 API 문서
서버 실행 후 아래 주소로 접속하여 Swagger UI를 통해 상세한 API 명세를 확인할 수 있습니다.
- **Swagger UI:** `http://localhost:8080/swagger-ui/index.html` (기본 포트 설정 시)

## 💡 주요 아키텍처 및 고려사항
- **비정형 데이터 관리:** 사용자의 다양한 학습 데이터를 유연하게 저장하기 위해 NoSQL인 MongoDB를 채택했습니다.
- **비동기 처리(예정/진행 중):** 외부 API(OCR, 번역) 호출 시 발생하는 네트워크 지연을 최소화하기 위해 비동기 로직 처리를 지향합니다.

- ## 🎥 시연 영상
https://github.com/user-attachments/assets/2300d228-fa23-4309-81e1-4985730568cf
