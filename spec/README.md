# spec — 개발 기준 문서

개발자(백엔드·프론트엔드)가 구현의 근거로 삼는 문서를 모읍니다.
자료 간 충돌 시 **요구사항 명세서**를 우선합니다.

## 현재 문서

| 문서 | 설명 |
| --- | --- |
| [PRD.md](./PRD.md) | 마스터 제품 문서 (범위·기능·흐름 총괄) |
| [요구사항-명세서.md](./요구사항-명세서.md) · [pdf](./요구사항-명세서.pdf) | 기능 요구사항 (AUTH/TIME/MEET/MATCH/VOTE) |

## 앞으로 추가할 문서

- `api-*.md` — API 명세서. 기능(모듈) 단위로 파일 분리 (예: `api-auth.md`, `api-match.md`). FastAPI `/docs`(Swagger)에 자동 생성되므로 여기엔 **확정된 계약**과 예시를 정리.
- `erd.md` / `db-schema.md` — DB 데이터 모델. 현재 상세 ERD·클래스 다이어그램은 [진행보고서(상세설계) §3](../deliverables/진행보고서-상세설계.md#3-설계-결정-진행-상황)에 있으니, DB 구현 시 이를 기준으로 분리·발전시키세요.

### API 엔드포인트 템플릿

```md
### POST /api/v1/auth/login
소셜 로그인 처리.

**Request**  { "provider": "google", "code": "..." }
**Response 200**  { "access_token": "...", "user": { ... } }
**Errors**  400 잘못된 요청 / 401 인증 실패
```
