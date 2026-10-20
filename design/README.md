# 설계 문서

시스템 구조와 데이터 모델을 정리합니다.

## 넣을 문서 예시

- `architecture.md` — 시스템 아키텍처 (Next.js ↔ FastAPI ↔ Supabase)
- `erd.md` — ERD (엔티티 관계도)
- `db-schema.md` — DB 테이블/컬럼 정의
- `wireframe.md` — 화면 설계 / 와이어프레임

## 다이어그램

- 간단한 구조도는 [Mermaid](https://mermaid.js.org/) 로 작성하면 GitHub에서 바로 렌더링됩니다.

```mermaid
flowchart LR
    FE[Next.js / Vercel] -->|REST API| BE[FastAPI]
    BE --> DB[(Supabase / PGVector)]
    FE -->|Auth| DB
```
