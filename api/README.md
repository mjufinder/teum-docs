# API 명세서

백엔드(teum-backend) API 엔드포인트의 요청/응답 스펙을 정리합니다.
백엔드 모듈 구현 후 명세를 공유해야 프론트엔드 연동이 가능합니다.

## 작성 방식

- 기능(모듈) 단위로 파일을 나눕니다. (예: `api-auth.md`, `api-search.md`)
- FastAPI 는 `/docs` (Swagger) 에서 명세가 자동 생성되므로, 여기엔 **확정된 계약**과 예시를 정리합니다.

## 엔드포인트 템플릿

```md
### POST /api/v1/auth/login

소셜 로그인 처리.

**Request**
​```json
{ "provider": "google", "code": "..." }
​```

**Response 200**
​```json
{ "access_token": "...", "user": { "id": "...", "name": "..." } }
​```

**Errors**
| 코드 | 설명 |
| --- | --- |
| 400 | 잘못된 요청 |
| 401 | 인증 실패 |
```
