# 이상윤 (SangYoun Lee) · Backend Engineer

Java / Spring Boot / JPA 기반으로 **커머스 서비스**를 만듭니다.  
실서비스에서 터지는 문제 — 동시성 제어, 쿼리 최적화, 실시간 시스템 설계 — 를 주로 다룹니다.

- 🔭 Building: **HotSpot** — 라이브 커머스 플랫폼
- 🧱 Stack: **Java 21, Spring Boot 3.5.5, JPA/Hibernate, MySQL 8, Redis 7** / FE: **React 19 + TypeScript, Vite, Tailwind CSS v4**
- 🧠 Care about: Domain modeling, query tuning, clean APIs, concurrency control
- 🌱 Now learning: Index design / System design / Real-time architecture

---

## 🛒 HotSpot Platform (private)

스트리머가 치지직/숲에서 방송할 때 Hotspot 링크를 공유하면,  
시청자 구매 시 방송 화면에 **실시간 구매 알림 + 랭킹**이 오버레이되는 OBS 위젯을 제공하는 라이브 커머스 플랫폼.

> 구매가 단순 거래가 아니라 **방송 이벤트**가 되는 구조 — 도네이션 알림에서 착안.

- Backend: [kkiyong-company/backend](https://github.com/kkiyong-company/backend)
- Frontend: [kkiyong-company/react-frontend](https://github.com/kkiyong-company/react-frontend)

### 기술 스택

`Spring Boot 3.5.5` `Java 21` `JPA/Hibernate` `MySQL 8` `Redis ZSet` `SSE`  
`React 19 + TypeScript` `Vite` `Tailwind CSS v4` `Toss Payments` `AWS EC2/S3` `Sentry` `Docker Compose` `Nginx`

### 구현된 주요 시스템

```
✔ JWT 인증 — ADMIN / MANAGER / CREATOR / USER 4-tier 권한 구조 + 소셜 로그인(OAuth)
✔ Toss Payments 연동 — 카드 / 카카오페이 / 토스페이
✔ Redis ZSet 실시간 구매 랭킹(실시간/일간/주간/월간) + SSE 브로드캐스트
✔ OBS Browser Source 위젯 — 토큰 기반, 구매 알림 + Web Audio API 사운드
✔ 비관적 락 기반 재고 동시성 제어
✔ MANAGER ↔ CREATOR 파트너십 · 정산/출금 시스템 (Settlement, PromotionSettlement)
✔ 라이브 드롭 — 방송 중 한정 상품 노출 이벤트
✔ 팔로우 시스템 — USER → MANAGER 팔로우, 팔로잉 상품 피드
✔ S3 이미지 업로드 — JPEG 강제 변환 + 반복 압축
✔ 이메일 인증 · 비밀번호 재설정, Sentry 에러 모니터링
✔ Docker Compose 배포 — EC2 + MySQL + Redis + Nginx
```
