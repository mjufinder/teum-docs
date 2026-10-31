# teum-docs

teum (mjufinder) 프로젝트의 **문서 저장소**입니다. 용도별로 3개 폴더에 보관합니다.

## 디렉토리 구조

| 폴더 | 용도 | 내용 |
| --- | --- | --- |
| [`spec/`](./spec) | 개발 기준 | PRD, 요구사항 명세, (향후) API 명세·ERD·DB 스키마 |
| [`dev/`](./dev) | 개발 가이드 | 로컬 개발 환경 셋업 등 개발자용 안내 |
| [`deliverables/`](./deliverables) | 제출 산출물 | 보고서(개념설계·진행/상세설계·증빙서), 발표자료 |
| [`notes/`](./notes) | 운영 기록 | 회의록, 멘토링, 팀원 명단 |

> 개발자(백/프론트)는 **`spec/`** 만 보면 됩니다. 각 문서는 **md(바로 열람) + 원본 파일**로 보관됩니다.

## 문서 인덱스

| 문서 | md | 원본 |
| --- | --- | --- |
| PRD (마스터 제품 문서) | [spec/PRD.md](./spec/PRD.md) | — |
| 요구사항 명세서 | [spec/요구사항-명세서.md](./spec/요구사항-명세서.md) | [pdf](./spec/요구사항-명세서.pdf) |
| 개념설계보고서 | [deliverables/개념설계보고서.md](./deliverables/개념설계보고서.md) | [pdf](./deliverables/개념설계보고서.pdf) |
| 진행보고서(상세설계) | [deliverables/진행보고서-상세설계.md](./deliverables/진행보고서-상세설계.md) | [pdf](./deliverables/진행보고서-상세설계.pdf) |
| 생성형 AI 활용 증빙서 | [deliverables/생성형AI활용-증빙서.md](./deliverables/생성형AI활용-증빙서.md) | [pdf](./deliverables/생성형AI활용-증빙서.pdf) |
| 개념설계 발표자료 | [deliverables/개념설계-발표자료.md](./deliverables/개념설계-발표자료.md) | [pptx](./deliverables/개념설계-발표자료.pptx) |
| 상세설계 발표자료 | [deliverables/상세설계-발표자료.md](./deliverables/상세설계-발표자료.md) | [pptx](./deliverables/상세설계-발표자료.pptx) |
| 로컬 개발 환경 셋업 | [dev/로컬-개발-환경-셋업.md](./dev/로컬-개발-환경-셋업.md) | — |
| 팀원 명단 | [notes/팀원-명단.md](./notes/팀원-명단.md) | [xlsx](./notes/팀원-명단.xlsx) |
| 기술스택·개발계획 회의록 | [notes/2026-10-18-기술스택-개발계획.md](./notes/2026-10-18-기술스택-개발계획.md) | — |

## 작성 규칙

- 문서는 **Markdown(.md)** 으로 작성 (GitHub에서 바로 렌더링).
- 회의록·보고서 파일명: `YYYY-MM-DD-주제.md`. 그 외는 kebab-case 권장, 한글 제목은 공백 대신 하이픈(`-`).
- Word/PPT/Excel 등 원본은 해당 폴더에 함께 두고, 핵심 내용은 md로도 정리.
- 표/다이어그램은 Markdown 표 또는 [Mermaid](https://mermaid.js.org/) 사용 권장.

## 연관 레포

- 프론트엔드: [teum-frontend](https://github.com/mjufinder/teum-frontend)
- 백엔드: [teum-backend](https://github.com/mjufinder/teum-backend)
