---
sidebar_position: 2
---

# 2. Blog 포스트 작성 가이드

회고, 개발 일지 등 **Blog** 글 작성 규칙.

## 파일 생성

`blog` 디렉토리에 생성. 날짜 정보 필수.

### A. 날짜 파일명 (단일 파일)
```bash
blog/2024-01-01-project-review.md
```

### B. 날짜 폴더 (이미지 포함 시)
```bash
blog/
└── 2024-01-01-trip-review/
    ├── index.md  # 글 본문
    └── img/      # 리소스
```

## Frontmatter

```markdown
---
slug: project-review-v1      # 커스텀 URL (생략 시 파일명)
title: 프로젝트 회고
authors: [me]                # authors.yml ID 참조
tags: [review, devops]
image: ./thumb.png           # OG Image
date: 2024-01-01
---

<!-- truncate -->

목록 노출 요약분.
이 구분선 위쪽 내용만 리스트에 보임.
```

## 설정 참고

### Truncate
`<!-- truncate -->` 주석 필수. 미작성 시 글 전체가 목록에 노출됨.

### Authors
`blog/authors.yml`에 작성자 정보 사전 등록 권장.

```yaml
me:
  name: 홍길동
  title: Backend Engineer
  url: https://github.com/...
  image_url: https://github.com/...
```
