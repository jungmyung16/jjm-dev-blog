---
sidebar_position: 100
slug: /dev-log/runbook
---

# 운영 Runbook

이 문서는 블로그를 운영하기 위한 핵심 절차를 다룹니다.

## 1. 새 글 작성하기 (Blog)

1. `blog` 디렉터리에 마크다운 파일을 생성합니다.
2. 파일명 규칙: `YYYY-MM-DD-title.md` (예: `2025-01-01-new-year.md`)
3. **Front Matter** 작성:
   ```yaml
   ---
   slug: new-year
   title: 새해 다짐
   authors: [me]
   tags: [life, goal]
   ---
   ```

## 2. 새 문서 작성하기 (Docs)

1. `docs` 디렉터리 내 적절한 폴더에 파일을 생성합니다.
2. `intro.md`나 `sidebar_position`을 통해 순서를 조절할 수 있습니다.

## 3. 로컬 미리보기

작성한 글을 배포하기 전에 반드시 로컬에서 확인합니다.

```bash
npm run start
```

## 4. 배포하기 (Deployment)

GitHub Pages에 배포합니다.

### Windows (CMD)
```cmd
set GIT_USER=사용자명 && npm run deploy
```

### Mac/Linux (Bash)
```bash
GIT_USER=사용자명 npm run deploy
```

> **주의:** 처음 배포 시 GitHub 인증이 필요할 수 있습니다.
