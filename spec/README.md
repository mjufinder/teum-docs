# spec — 개발 기준 문서

개발자(백엔드·프론트엔드)가 구현의 근거로 삼는 문서를 모읍니다.
자료 간 충돌 시 **요구사항 명세서**를 우선합니다.

## 현재 문서

| 문서 | 설명 |
| --- | --- |
| [PRD.md](./PRD.md) | 마스터 제품 문서 (범위·기능·흐름 총괄) |
| [요구사항-명세서.md](./요구사항-명세서.md) · [pdf](./요구사항-명세서.pdf) | 기능 요구사항 (AUTH/TIME/MEET/MATCH/VOTE) |

## API 명세서는 손으로 쓰지 않습니다 (Swagger 자동생성)

백엔드는 **FastAPI** 를 쓰므로 API 명세가 코드(타입 힌트 + Pydantic 모델)에서 **자동 생성**됩니다. 별도 `api-*.md` 를 작성하지 마세요 — 코드와 어긋나 금방 낡습니다.

| 경로 | 내용 |
| --- | --- |
| `/docs` | **Swagger UI** (호출·테스트 가능한 대화형 문서) |
| `/redoc` | ReDoc (읽기용 문서) |
| `/openapi.json` | OpenAPI 3.x 원본 스펙 |

서버 실행 후 <http://localhost:8000/docs> 에서 확인. 샘플 라우터: [teum-backend `app/api/routes/auth.py`](https://github.com/mjufinder/teum-backend/blob/main/app/api/routes/auth.py)

**명세 품질은 코드로 올립니다** — 요청/응답을 Pydantic 모델로 정의(`response_model=`), 라우터에 `tags`·`summary`·docstring, `Field(..., examples=[...])` 로 예시까지 노출.

### 제출·공유용으로 스펙을 파일로 떠야 할 때

```bash
# teum-backend 에서 OpenAPI 스펙을 파일로 export
python -c "import json, app.main as m; print(json.dumps(m.app.openapi(), ensure_ascii=False, indent=2))" > spec/openapi.json
```

구현 전 프론트와 "계약"만 먼저 합의하는 경우에 한해 짧은 초안을 둘 수 있으나, 구현되면 Swagger 로 대체합니다.

## 그 외 추가할 문서

- `erd.md` / `db-schema.md` — DB 데이터 모델. 현재 상세 ERD·클래스 다이어그램은 [진행보고서(상세설계) §3](../deliverables/진행보고서-상세설계.md#3-설계-결정-진행-상황)에 있으니, DB 구현 시 이를 기준으로 분리·발전시키세요.
