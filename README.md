# 이상윤 (SangYoun Lee) · Backend Engineer

Java / Spring Boot / JPA 기반으로 **커머스 서비스**를 만듭니다.  
실서비스에서 터지는 문제 — 동시성 제어, 쿼리 최적화, 실시간 시스템 설계 — 를 주로 다룹니다.

- 🔭 Building: **HotSpot** — 라이브 커머스 플랫폼
- 🧱 Stack: **Java 21, Spring Boot, JPA/Hibernate, MySQL, Redis** / FE: **React + TypeScript**
- 🧠 Care about: Domain modeling, query tuning, clean APIs, concurrency control
- 🌱 Now learning: Index design / System design / Real-time architecture

---

## 🛒 HotSpot Platform (private)

스트리머가 치지직/숲에서 방송할 때 Hotspot 링크를 공유하면,  
시청자 구매 시 방송 화면에 **실시간 구매 알림 + 랭킹**이 오버레이되는 OBS 위젯을 제공하는 라이브 커머스 플랫폼.

> 구매가 단순 거래가 아니라 **방송 이벤트**가 되는 구조 — 도네이션 알림에서 착안.

### 기술 스택

`Spring Boot` `Java 21` `JPA/Hibernate` `MySQL` `Redis ZSet` `SSE`  
`React + TypeScript` `Toss Payments` `AWS EC2/S3` `Docker Compose` `Nginx`

### 구현된 주요 시스템

```
✔ JWT 인증 — ADMIN / MANAGER / USER 3-tier 권한 구조
✔ Toss Payments 연동 — 카드 / 카카오페이 / 토스페이
✔ Redis ZSet 실시간 구매 랭킹 + SSE 브로드캐스트
✔ OBS Browser Source 위젯 — 토큰 기반, 구매 알림 + Web Audio API 사운드
✔ 비관적 락 기반 재고 동시성 제어
✔ 정산/출금 시스템 (SellerBankAccount, Settlement)
✔ S3 이미지 업로드 — JPEG 강제 변환 + 반복 압축
✔ Docker Compose 배포 — EC2 + MySQL + Redis + Nginx
```
