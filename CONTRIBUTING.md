# 기여 가이드 (Git 컨벤션)

teum 프로젝트는 **기능 단위로 이슈를 만들고 → 브랜치에서 작업 → PR로 병합**합니다.

## 작업 흐름

1. 작업할 기능으로 **이슈 생성** (이슈 템플릿 사용)
2. 이슈 번호로 **브랜치 생성** 후 작업
3. **PR 생성** (PR 템플릿 사용, `Closes #이슈번호` 로 이슈 연결)
4. 리뷰 후 **main 에 병합**

## 브랜치 네이밍

```
<type>/<short-description>
```

예: `feat/db-schema`, `fix/login-error`, `docs/readme-update`

## 커밋 컨벤션 (Conventional Commits)

```
<type>(<scope>): <subject>
```

- **type**: `feat`(기능) · `fix`(버그) · `docs`(문서) · `refactor`(리팩터링) · `test`(테스트) · `chore`(설정/빌드) · `style`(포맷)
- **scope**: 선택. 영향 범위 (예: `db`, `auth`, `meeting`)
- **subject**: 한글로 간결하게, 마침표 없이

예시

```
feat(db): 초기 DB 스키마 추가
fix(auth): 소셜 로그인 코드 검증 오류 수정
docs: README 실행 방법 보완
```

## PR

- 제목도 커밋 컨벤션을 따른다 (예: `feat(db): 초기 DB 스키마 추가`)
- 본문은 PR 템플릿을 사용하고, 관련 이슈를 `Closes #N` 으로 연결한다
