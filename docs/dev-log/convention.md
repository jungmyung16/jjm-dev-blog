---
sidebar_position: 99
slug: /dev-log/convention
---

# 운영 컨벤션 (URL 및 규칙)

이 문서는 블로그와 문서를 작성할 때 일관성을 유지하기 위한 규칙을 정의합니다.

## 1. URL 및 Slug 규칙

### 기본 원칙
- **영문 소문자** 사용을 원칙으로 합니다.
- 띄어쓰기는 **하이픈(-)**으로 대체합니다 (kebab-case).
- 명확한 키워드를 포함하여 의미를 전달합니다.

### 1) 블로그 (Blog)
블로그 포스트는 파일명에 날짜를 포함하는 것을 권장합니다.

- **파일 경로:** `blog/YYYY-MM-DD-my-post-title.md`
- **Slug 설정:** 프론트매터(Front Matter)의 `slug` 속성을 사용하여 짧은 주소를 지정할 수 있습니다.
  ```yaml
  ---
  slug: my-post-title
  ---
  ```
- **최종 URL:** `/blog/my-post-title` (slug 설정 시) 또는 `/blog/YYYY/MM/DD/my-post-title` (기본값)

### 2) 문서 (Docs)
문서는 디렉터리 구조를 반영하는 것을 기본으로 합니다.

- **파일 경로:** `docs/folder-name/doc-title.md`
- **Slug 설정:** 필요한 경우 명시적으로 지정하여 깊이를 조절할 수 있습니다.
  ```yaml
  ---
  slug: /folder/doc-title
  ---
  ```

## 2. 이미지 및 리소스

- 모든 정적 이미지 파일은 `static/img` 디렉터리에 저장합니다.
- 마크다운 내에서는 `/img/filename.png` 형식으로 절대 경로를 사용하여 참조합니다.
  ```markdown
  ![이미지 설명](/img/my-image.png)
  ```

## 3. 링크 규칙 (Cross-Linking)

- **블로그 → 문서:** `/docs/...` 경로를 사용합니다.
- **문서 → 블로그:** `/blog/...` 경로를 사용합니다.
- 상대 경로(`../../`)보다는 절대 경로(`/docs/...`) 사용을 권장합니다.
