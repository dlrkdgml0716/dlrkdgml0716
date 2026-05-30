# 이강희 | Lee Kang-hee

> 계명대학교 컴퓨터공학과
> Backend Engineer

📧 [dlrkdgml0716@gmail.com](mailto:dlrkdgml0716@gmail.com)

---

### Featured Projects

#### 🍚 [bappul-msa](https://github.com/dlrkdgml0716/bappul-msa) — 학식 예약 플랫폼 (캡스톤, 6명+, 2학기 진행)
**3학년 2학기에 Flutter 프론트엔드로 참여한 모놀리식 학식 예약 서비스를, 4학년 1학기에 백엔드로 포지션을 옮겨 MSA 구조로 마이그레이션한 캡스톤 프로젝트.** 유지보수성·확장성이라는 MSA의 장점을 학식 예약 도메인에 직접 적용하기 위해 백엔드 팀원들과 공동으로 설계·구현. **하이브리드 캐시 설계를 학술 논문(한국정보기술학회)으로 정리하여 제출.**

- **포지션 전환** — 3-2 Flutter 프론트엔드 → 4-1 Java/Spring 백엔드. 백엔드 전환을 위해 Java/Spring을 독학으로 학습.
- **모놀리식 → MSA 마이그레이션 공동 설계** — 백엔드 팀원들과 도메인 경계, 서비스 분리 기준, 인증·인가 게이트웨이 구조를 함께 설계.
- **Caffeine(L1) + Redis(L2) 하이브리드 캐시** — JVM 로컬 캐시로 응답 지연 최소화, Redis로 인스턴스 간 정합성 확보. Redis Pub/Sub 기반 캐시 무효화로 MSA 환경에서의 stale read 방지.
- **실험 기반 검증** — 캐시 적용 전/후 응답 시간 비교 및 무효화 시나리오별 동작 검증을 학술 논문에 정량적 결과로 포함.
- **AI 에이전트 통합** — 학식 추천 기능에 AI 에이전트 연동.

`Java` `Spring Boot` `Spring Cloud` `Caffeine` `Redis` `MySQL` `Docker` `Gradle` `Flutter (3-2)`

#### 🎨 [The_Pixel_War](https://github.com/dlrkdgml0716/The_Pixel_War) — 실시간 협업 픽셀 배치 게임
지도 위 동일 좌표에 다수 사용자가 동시에 픽셀을 찍는 환경에서 **동시성 제어, 캐시 계층, 실시간 브로드캐스팅** 세 축의 상호작용을 다룬 모놀리스 프로젝트.

- **이중 방어 동시성 제어** — `userId` 기반 Redis TTL 쿨다운(1차) + 좌표 기반 Redisson 분산 락(2차).
- **Redis 자료구조 최적화** — 픽셀 색상은 String, 순위·핫픽셀은 ZSET(`ZINCRBY`/`ZREVRANGE`)으로 O(log N) 갱신.
- **WebSocket/STOMP 실시간 동기화** — 좌표 변경을 모든 구독자에게 즉시 브로드캐스트.
- **보안 개선 이력** — 외부 코드 리뷰로 식별된 시크릿 하드코딩·인증 우회·XSS를 단계적 리메디에이션, 노출된 AWS 키 즉시 로테이션.
- **Kakao OAuth 2.0 + S3 연동** — 인증 컨텍스트 기반 사용자 식별, 길드 청사진 이미지 업로드.

`Java` `Spring Boot` `Spring Security` `Redis` `Redisson` `MySQL` `WebSocket/STOMP` `AWS S3`

---

### Tech Stack

**Languages**
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)

**Backend**
- **Framework** — `Spring Boot` `Spring Cloud` `Spring Security` `Spring Data JPA`
- **Cache / Coordination** — `Caffeine` `Redis` `Redisson`
- **Real-time** — `WebSocket` `STOMP`
- **Database** — `MySQL` `H2`
- **Build** — `Gradle`

**Infrastructure**
`Docker` · `AWS (EC2, S3)` · `Linux`

**Tools**
`IntelliJ IDEA` · `Git / GitHub` · `Postman` · `draw.io`

---

### Currently Learning

- **관찰성** — Prometheus, Grafana, Spring Actuator + Micrometer
- **테스트 코드** — JUnit, Mockito, 동시성 시나리오 통합 테스트
- **메시지 브로커** — Kafka 기반 비동기 도메인 이벤트 처리

---

📧 **Contact** — [dlrkdgml0716@gmail.com](mailto:dlrkdgml0716@gmail.com)
