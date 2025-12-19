---
sidebar_position: 1
---

# 1. Dev Notes 작성 가이드

지식/정보 정리를 위한 **Dev Notes** 작성 규칙.

## 파일 생성

카테고리 폴더 내 마크다운(`md`) 파일 생성.

```bash
docs/
├── cs/
├── spring/
│   ├── jpa-n-plus-1.md
│   └── spring-security-architect.md
└── ...
```

> **규칙**: 파일명은 **영문 소문자**와 **하이픈(-)**만 사용 (URL 경로로 매핑됨).

## Frontmatter

문서 상단 메타데이터 정의 필수.

```markdown
---
sidebar_position: 1
title: JPA N+1 문제 해결
description: fetch join과 batch size를 이용한 최적화 방법 정리
tags: [jpa, box-sizing, optimization]
---

# JPA N+1 문제 해결

본문 내용...
```

*   `sidebar_position`: 사이드바 정렬 순서 (오름차순).
*   `title`: 문서 제목.
*   `description`: 메타 설명 (SEO).
*   `tags`: 하단 태그.

## 하위 폴더 구조

주제 세분화 필요 시 하위 폴더 생성. Docusaurus가 자동으로 하위 메뉴 구성함.

```
docs/
└── cs/
    ├── algorithm/
    │   ├── binary-search.md
    │   └── quick-sort.md
    └── network/
        ├── tcp-ip-handshake.md
        └── http-v2.md
```
