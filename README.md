# 이재영 포트폴리오

**Email**: woduddl1000@gmail.com
<br>
**GitHub**: [@ljy0221](https://github.com/ljy0221)

---

## 전문 분야

풀스택 개발자로서 준비하고있습니다.
성능 개선에 관심이 많습니다.

**현재 학습 중**: Spring WebFlux, kafka, spark, n8n<br>
**진행 중인 프로젝트**: 

---

## 기술 스택

| 분류 | 기술 |
|------|------|
| **Frontend** | React, Next.js, TypeScript, JavaScript, Vue.js, Electron, Flutter, HTML5, CSS3 |
| **Backend** | Spring Boot, Node.js, Express, FastAPI, Flask |
| **Database** | PostgreSQL, MySQL, MongoDB, Redis, ChromaDB (Vector DB) |
| **Infrastructure** | Docker, Nginx, AWS EC2, GitLab CI/CD, Prometheus, Grafana, k6 |
| **Real-time** | WebRTC (Kurento), WebSocket, Yjs CRDT |

---

## 주요 프로젝트

### 1. SYNAPSE - 개발자를 위한 학습 노트 플랫폼

| 항목 | 내용 |
|------|------|
| **기간** | 2025.12 - 2026-02 (7주) |
| **역할** | 팀장, 풀스택 개발 (6인 팀) |
| **기술 스택** | Spring Boot 3.5, React 18, Electron 30, Docker, PostgreSQL, MongoDB, Redis, WebRTC |
| **저장소** | [SynapseNote](https://github.com/ljy0221/SynapseNote) |

#### 프로젝트 개요
개발자들이 학습 노트를 작성하면서 코드를 즉시 실행하고, AI 리뷰를 받으며, 실시간으로 협업할 수 있는 통합 데스크톱 플랫폼. 기존 노트 앱의 코드 실행 부재와 IDE의 학습 노트 작성 한계를 극복한 개발자 특화 학습 환경.

#### 핵심 기능

**1. Docker 샌드박스 코드 실행 엔진**
- Python 3.11, JavaScript (Node 20), Java 17 지원
- 7중 보안 정책: CPU/메모리 제한, 네트워크 격리, Read-only 파일시스템, PID 제한
- 리소스 제한: CPU 1.0코어, 메모리 512MB, PID 50개

**2. 세션 기반 REPL 시스템**
- 같은 노트 내 코드 블록 간 변수/함수 공유
- 컨테이너 재사용으로 실행 속도 20-30배 향상 (2-3초 → 0.1초)
- endMarker 패턴 기반 실행 완료 감지 (50ms 폴링)
- 30분 유휴 시 세션 자동 정리

**3. AI 멀티 프로바이더 코드 리뷰**
- Claude Sonnet 4.5, Gemini 2.0 Flash, GPT-4o 지원
- 코드 리뷰, 코드 요약, 선택 영역 질문 기능
- Factory/Strategy 패턴으로 확장성 확보

**4. 실시간 협업 시스템**
- Yjs CRDT 기반 동시 편집 및 충돌 자동 해결
- 50ms 이내 실시간 동기화
- 오프라인 편집 지원 (재접속 시 자동 병합)
- 사용자 커서 및 상태 실시간 공유

**5. 노트 초대 및 권한 관리**
- OWNER, EDITOR, VIEWER 3단계 권한 시스템
- JWT 티켓 기반 WebSocket 인증 (TTL 60초)
- 시간 기반 초대 링크 만료

#### 개발 업무 및 성과

**팀장 및 프로젝트 관리**
- 6인 팀 리드 및 업무 분배
- 시스템 아키텍처 설계 및 기술 스택 선정
- 하이브리드 DB 아키텍처 설계 (PostgreSQL + MongoDB + Redis)

**Backend 개발**
- Spring Boot 기반 RESTful API 설계 및 구현
- Docker 샌드박스 코드 실행 엔진 구현
- 세션 기반 REPL 시스템 구현
- AI 프로바이더 통합 (Factory Pattern)

**Frontend 개발**
- React 18 + TypeScript 기반 UI 개발
- Electron IPC 기반 Main-Renderer 프로세스 분리
- Zustand 상태 관리
- Yjs 실시간 협업 통합

**Infrastructure**
- Docker Compose 기반 개발 환경 구축

#### 기술적 구현 상세

| 분류 | 기술 및 도구 |
|------|-------------|
| **Backend** | Spring Boot 3.5.9, Java 17, Gradle 8.8 |
| **Database** | PostgreSQL 16 (메타데이터), MongoDB 8.0 (노트 블록), Redis 7.4 (토큰/캐시) |
| **Security** | Spring Security, JWT, OAuth 2.0, CORS |
| **Frontend** | React 18, TypeScript 5.4, Electron 30 |
| **Real-time** | Yjs 13.6, WebSocket, Zustand 5.0 |
| **WebRTC** | Kurento 7.1.0 |
| **Containerization** | Docker 27.4, Docker Compose |
| **Web Server** | Nginx 1.25 |
| **CI/CD** | jenkins |
| **Monitoring** | Prometheus, Grafana |

#### 프로젝트 성과
- electron IPC 통신을 이용한 로컬 시스템 활용
- 세션 코드 실행 속도 20~30배 향상
- 오프라인 지원

---

### 2. 갈래?말래? - AI 기반 즉흥 여행 추천 플랫폼

| 항목 | 내용 |
|------|------|
| **기간** | 2025.11 ~ 2025.12 (5-6주) |
| **역할** | AI/Backend 개발, 팀장 (2인 팀) |
| **기술 스택** | Vue.js, Spring Boot, FastAPI, ChromaDB, MySQL, AWS EC2 |
| **저장소** | [SpontaneousTrip](https://github.com/ljy0221/SpontaneousTrip) |

#### 프로젝트 개요
사용자의 위치와 선호도를 기반으로 즉흥 여행지를 추천하는 AI 챗봇 플랫폼. RAG 기술을 활용하여 15,000개 관광지 데이터에서 실시간으로 최적의 여행지를 제안.

#### 주요 성과
- AI RAG 챗봇 구현 (ChromaDB + sentence-transformers 기반)
- 15,000개 관광지 데이터 임베딩 및 벡터 검색 시스템 구축
- 위치 기반 실시간 추천 시스템 개발 (Geolocation + 날씨 API 통합)
- GIS 공간 인덱스 + MBR을 활용한 위치 검색 성능 최적화
- AI 스트리밍 응답 구현으로 사용자 경험 개선
- 게시판 및 마이페이지 풀스택 개발
- MVP 100% 달성 후 추가 기능 구현

#### 기술적 구현

**AI/ML 시스템**
- RAG (Retrieval-Augmented Generation) 파이프라인 구현
- ChromaDB Vector Database 구축 및 관리
- sentence-transformers 기반 임베딩 최적화
- 스트리밍 응답 구현 (SSE)

**Backend 개발**
- Spring Boot 기반 RESTful API 설계
- MyBatis 기반 xml 매퍼 구축
- FastAPI 기반 AI 서버 구축

**Database 최적화**
- MySQL GIS 확장 활용
- 공간 인덱스 (Spatial Index) 구축
- MBR (Minimum Bounding Rectangle) 기반 쿼리 최적화

**Frontend 개발**
- Vue.js 3 기반 SPA 구현
- Pinia 상태 관리
- SCSS 기반 반응형 디자인
- 날씨 API 및 Geolocation API 통합

**DevOps**
- AWS EC2 배포
- GitLab CI/CD 파이프라인 구성

#### 기술 스택 상세

| 분류 | 기술 |
|------|------|
| **Frontend** | Vue.js 3, Vuex, SCSS |
| **Backend** | Spring Boot, FastAPI |
| **Database** | MySQL (GIS), ChromaDB (Vector DB) |
| **AI/ML** | RAG, sentence-transformers, Embedding |
| **API** | Geolocation API, 날씨 API, 한국관광공사 API |
| **Deployment** | AWS EC2, Docker, GitLab CI/CD |

---

### 3. 마음씨 (마음°C) - 우울증 환자용 감정 관리 시스템

| 항목 | 내용 |
|------|------|
| **기간** | 2024.02~2024.06 (4개월) |
| **역할** | Frontend 개발 리드 (6인 팀) |
| **기술 스택** | Flutter, Spring Boot, Flask, Python |
| **저장소** | [RestProject-Heart](https://github.com/ljy0221/RestProject-Heart) |
| **언론 보도** | [기호일보](https://www.kihoilbo.co.kr/news/articleView.html?idxno=1092649) |

#### 프로젝트 개요
우울증 환자의 감정 관리를 위한 대화형 챗봇 및 일상 관리 애플리케이션. 자연어 입력 기반 상담과 감정 분석을 통한 행동 추천 시스템을 제공하여 일상에서의 지속적인 질환 관리를 지원.

#### 핵심 기능

**1. 상담형 AI 챗봇**
- 자연어 처리 기반 실시간 상담 기능
- 사용자 입력에 대한 맥락 이해 및 적절한 응답 생성

**2. 감정 기반 일기 시스템**
- 일기 작성 전후 감정 기록 및 비교 분석
- 달력 기반 일기 관리 (작성, 수정, 삭제)
- 감정 분석 결과 기반 배경 음악 자동 생성 및 재생

**3. 행동 추천 시스템**
- 사용자 감정 상태 기반 맞춤형 행동 추천
- 행동 전후 감정 변화 추적
- 부정→긍정 감정 전환 시 통계 데이터 누적

**4. 감정 통계 및 분석**
- 월간 감정 통계 시각화
- 전체 기간 감정 Top 3 분석
- 시간대별 감정 패턴 분석 (24시간 4분할)
- 효과적인 행동 패턴 리스트 제공

**5. 우울증 건강 설문**
- 우울 척도 진단 설문 시스템
- 이전 기록과 현재 기록 비교를 통한 상태 트래킹

**6. 게이미피케이션**
- 경험치 시스템 기반 캐릭터 성장

#### 개발 업무 및 성과

**Flutter 기반 모바일 앱 개발**
- Widget 기반 UI 컴포넌트 설계 및 구현 (31개 Dart 파일)
- MediaQuery를 활용한 반응형 디자인 적용
- 메인 화면, 로그인, 통계, 일기, 채팅 화면 개발

**백엔드 연동 및 데이터 처리**
- HTTP 패키지를 통한 RESTful API 연동
- SharedPreferences를 통한 로컬 데이터 저장소 구현
- Flutter Secure Storage를 활용한 보안 데이터 관리

**사용자 경험 최적화**
- Table Calendar를 통한 직관적인 일기 관리
- FL Chart를 활용한 감정 통계 시각화
- Just Audio를 통한 감정 기반 배경음악 재생
- Provider 패턴을 통한 상태 관리

#### 기술 스택 상세

| 분류 | 기술 및 패키지 |
|------|---------------|
| **Frontend** | Flutter SDK 3.4.0+, Dart |
| **UI Components** | Cupertino Icons, Salomon Bottom Bar, Table Calendar 3.1 |
| **Data & State** | Provider 6.1, SharedPreferences 2.2, Flutter Secure Storage 9.2 |
| **Networking** | HTTP 1.2 (RESTful API) |
| **Visualization** | FL Chart 0.68 |
| **Media** | Just Audio 0.9 |
| **Utilities** | Intl 0.19, URL Launcher 6.0, Flutter SpinKit 5.2 |
| **Backend** | Spring Boot (Java), Flask (Python) |

#### 프로젝트 성과
- 언어 구성: Dart 65.9%, Java 27.0%, Python 6.6%
- 캡스톤 프로젝트 완료 및 수상, 지역 언론 보도

---

### 4. Nonogram 모바일 게임

| 항목 | 내용 |
|------|------|
| **기간** | 2024 |
| **역할** | 개인 프로젝트 |
| **기술 스택** | Java, Android |
| **저장소** | [mobileProgramming_Nonogram](https://github.com/ljy0221/mobileProgramming_Nonogram) |

#### 프로젝트 개요
논리 퍼즐 게임 Nonogram의 Android 네이티브 구현

---

## 연락처

- **Email**: woduddl1000@gmail.com
- **GitHub**: https://github.com/ljy0221

---

*최종 수정일: 2026년 2월*
