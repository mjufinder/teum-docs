# teum-docs

teum (mjufinder) 프로젝트의 **문서 저장소**입니다.
요구사항 명세서, API 명세서, 회의록, 설계 문서, 멘토링 보고서 등을 종류별로 보관합니다.

## 디렉토리 구조

| 폴더 | 내용 |
| --- | --- |
| [`requirements/`](./requirements) | 요구사항 명세서, PRD |
| [`reports/`](./reports) | 공식 보고서 (개념설계·진행/상세설계·증빙서) |
| [`presentations/`](./presentations) | 발표자료 |
| [`api/`](./api) | API 명세서 (엔드포인트, 요청/응답 스펙) |
| [`design/`](./design) | 설계 문서 (시스템 아키텍처, ERD, DB 스키마, 화면 설계) |
| [`planning/`](./planning) | 기획 자료 (기능 정의/선정, 일정, 역할, 팀원 명단) |
| [`meetings/`](./meetings) | 회의록 (날짜별) |
| [`mentoring/`](./mentoring) | 멘토링 노트 |
| [`assets/`](./assets) | 이미지, 다이어그램, 캡처, 기타 첨부 파일 |

## 문서 인덱스

각 문서는 **md(바로 열람)** + **원본 파일**로 보관되어 있습니다.

| 문서 | md | 원본 |
| --- | --- | --- |
| PRD (마스터 제품 문서) | [PRD.md](./requirements/PRD.md) | — |
| 요구사항 명세서 | [md](./requirements/요구사항-명세서.md) | [pdf](./requirements/요구사항-명세서.pdf) |
| 개념설계보고서 | [md](./reports/개념설계보고서.md) | [pdf](./reports/개념설계보고서.pdf) |
| 진행보고서(상세설계) | [md](./reports/진행보고서-상세설계.md) | [pdf](./reports/진행보고서-상세설계.pdf) |
| 생성형 AI 활용 증빙서 | [md](./reports/생성형AI활용-증빙서.md) | [pdf](./reports/생성형AI활용-증빙서.pdf) |
| 개념설계 발표자료 | [md](./presentations/개념설계-발표자료.md) | [pptx](./presentations/개념설계-발표자료.pptx) |
| 상세설계 발표자료 | [md](./presentations/상세설계-발표자료.md) | [pptx](./presentations/상세설계-발표자료.pptx) |
| 팀원 명단 | [md](./planning/팀원-명단.md) | [xlsx](./planning/팀원-명단.xlsx) |
| 기술스택·개발계획 회의록 | [md](./meetings/2026-10-18-기술스택-개발계획.md) | — |

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
