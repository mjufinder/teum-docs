# teum-docs

teum (mjufinder) 프로젝트의 **문서 저장소**입니다.
요구사항 명세서, API 명세서, 회의록, 설계 문서, 멘토링 보고서 등을 종류별로 보관합니다.

## 디렉토리 구조

| 폴더 | 내용 |
| --- | --- |
| [`requirements/`](./requirements) | 요구사항 명세서 (기능/비기능 요구사항) |
| [`api/`](./api) | API 명세서 (엔드포인트, 요청/응답 스펙) |
| [`design/`](./design) | 설계 문서 (시스템 아키텍처, ERD, DB 스키마, 화면 설계) |
| [`planning/`](./planning) | 기획 자료 (기능 정의/선정, 개발 일정, 역할 분담) |
| [`meetings/`](./meetings) | 회의록 (날짜별) |
| [`mentoring/`](./mentoring) | 멘토링 / 제작 보고서 |
| [`assets/`](./assets) | 이미지, 다이어그램, 캡처, 기타 첨부 파일 |

## 파일 네이밍 규칙

- **회의록 / 보고서**: `YYYY-MM-DD-주제.md`  (예: `2026-10-20-제작보고서-멘토링.md`)
- **일반 문서**: 소문자 + 하이픈(kebab-case).  (예: `api-auth.md`, `db-schema.md`)
- 한글 제목을 써도 되지만, 가능하면 공백 대신 하이픈(`-`)을 사용합니다.
- 이미지 등 첨부는 `assets/` 에 넣고 문서에서 상대경로로 참조합니다.

## 작성 가이드

- 문서는 **Markdown(.md)** 로 작성합니다. (GitHub에서 바로 렌더링됨)
- 표/다이어그램이 필요하면 Markdown 표 또는 [Mermaid](https://mermaid.js.org/) 사용을 권장합니다.
- 큰 변경은 PR로, 가벼운 수정은 바로 커밋해도 됩니다.
- Word/PPT/Excel 등 바이너리 원본은 `assets/` 하위에 보관하되, 핵심 내용은 가능하면 Markdown으로도 정리합니다.

## 연관 레포

- 프론트엔드: [teum-frontend](https://github.com/mjufinder/teum-frontend)
- 백엔드: [teum-backend](https://github.com/mjufinder/teum-backend)
