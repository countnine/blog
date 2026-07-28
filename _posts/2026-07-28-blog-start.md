---
title: 블로그를 시작합니다
date: 2026-07-28 10:00:00 +0900
categories: [Blog]
tags: [jekyll, github-pages]
description: Jekyll(Chirpy) + GitHub Pages 로 만든 블로그의 첫 글입니다.
---

## 무엇으로 만들었나

- **Jekyll** — 마크다운 파일을 정적 HTML로 변환하는 사이트 생성기
- **Chirpy** — 다크모드, 카테고리/태그, 목차, 검색을 기본 제공하는 테마
- **GitHub Pages** — 무료 호스팅. `main` 브랜치에 푸시하면 GitHub Actions가 자동으로 빌드·배포합니다

로컬에 Ruby를 설치하지 않아도 됩니다. 글을 쓰고 푸시하면 GitHub 서버가 알아서 빌드합니다.

## 글 쓰는 법

`_posts/` 폴더에 `YYYY-MM-DD-slug.md` 형식으로 파일을 만들고, 맨 위에 아래처럼 머리말(front matter)을 넣습니다.
이때 **파일명이 그대로 URL** 이 되므로 영문 소문자와 하이픈으로 짓는 편이 좋습니다.

```yaml
---
title: 글 제목
date: 2026-07-28 10:00:00 +0900
categories: [대분류, 소분류]
tags: [태그1, 태그2]
---
```

그다음 평소처럼 마크다운으로 본문을 쓰면 됩니다. 커밋하고 푸시하면 1~2분 뒤 사이트에 반영됩니다.

## 유용한 문법 몇 가지

이미지는 `assets/img/` 에 넣고 이렇게 씁니다.

```markdown
![설명](/assets/img/example.png)
_이미지 아래 설명글_
```

Chirpy 전용 강조 상자도 있습니다.

> 알아두면 좋은 팁입니다.
{: .prompt-tip }

> 주의가 필요한 내용입니다.
{: .prompt-warning }

## 앞으로

작업하면서 막혔던 것과 해결 과정을 그때그때 기록해 두려고 합니다.
