# 이상윤 (SangYoun) · Backend Engineer

Java / Spring Boot / JPA 기반으로 **커머스 서비스**를 만드는 데 관심이 많습니다.  
최근에는 **상품 옵션(SKU/Variant) 설계**, **권한/인증(JWT)**, **쿼리 최적화**, **파일 업로드(S3/Local)** 같은 “실서비스에서 터지는 문제”를 주로 다루고 있어요.

- 🔭 Building: **HotSpot** (e-commerce + seller ranking + fan loyalty ranking)
- 🧱 Favorite stack: **Java, Spring Boot, JPA/Hibernate, MySQL**, (FE: **React + TS**)
- 🧠 I care about: Domain modeling, SQL performance, clean APIs, pragmatic refactoring
- 🌱 Now learning: Query tuning / Indexing / System design

---

## What I'm working on (Private repos, but here's the outline)

### 🛒 HotSpot Platform (private)

---

## Architecture (overview)

```mermaid
flowchart LR
  FE[React + TS] -->|REST| API[Spring Boot]
  API --> DB[(MySQL)]
  API --> FS[File Storage: Local/S3]
  API --> AUTH[JWT Auth & Role]
