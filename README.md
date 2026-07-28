# blog

[Jekyll](https://jekyllrb.com/) + [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 테마로 만든 블로그.
GitHub Pages 에서 무료로 호스팅됩니다.

- 사이트: <https://countnine.github.io/blog/>
- 배포: `main` 브랜치에 푸시하면 `.github/workflows/pages-deploy.yml` 이 자동으로 빌드·배포 (약 1~2분)

## 글 쓰기

`_posts/YYYY-MM-DD-slug.md` 파일을 만들고 머리말을 넣습니다.

> **파일명이 곧 URL 입니다.** 제목은 한글로 써도 되지만 파일명은 영문 소문자·하이픈으로 쓰세요.
> `2026-07-28-blog-start.md` → `https://countnine.github.io/blog/posts/blog-start/`
> 파일명에 한글을 쓰면 URL 이 퍼센트 인코딩되어 지저분해집니다.

```yaml
---
title: 글 제목
date: 2026-07-28 10:00:00 +0900
categories: [대분류, 소분류]
tags: [태그1, 태그2]
---
```

그다음 커밋 & 푸시:

```bash
git add .
git commit -m "post: 글 제목"
git push
```

> 미래 시각으로 `date` 를 적으면 그 시각까지 사이트에 나오지 않습니다.

## 이미지

`assets/img/` 에 넣고 `![설명](/assets/img/파일명.png)` 으로 참조합니다.
`baseurl` 이 `/blog` 이므로 경로 앞에 `/blog` 를 직접 붙이지 마세요 — Jekyll 이 알아서 처리합니다.

## 설정

주요 항목은 모두 `_config.yml` 에 있습니다.

| 항목 | 설명 |
| --- | --- |
| `title`, `tagline`, `description` | 사이트 제목/부제/소개 |
| `avatar` | 사이드바 프로필 이미지 경로 |
| `baseurl` | `/blog` (프로젝트 리포이기 때문) |
| `comments.provider` | 댓글 기능 — giscus (GitHub Discussions 연동) |
| `analytics.goatcounter.id` | 방문 통계 — GoatCounter 코드 `countnine` |
| `pageviews.provider` | 글마다 조회수 표시 (goatcounter) |

### 댓글 (giscus)

`countnine/blog` 의 Discussions **Announcements** 카테고리에 글 URL 별로 스레드가 자동 생성됩니다.
방문자는 GitHub 계정으로 로그인해 댓글을 답니다. 댓글 관리는 Discussions 탭에서 하면 됩니다.

### 방문 통계 (GoatCounter)

대시보드: <https://countnine.goatcounter.com>

본인 방문을 통계에서 빼려면 브라우저 콘솔에서 아래를 한 번 실행합니다.

```js
localStorage.setItem('skipgc', 't')
```

## 로컬 미리보기 (선택)

로컬에 Ruby 를 설치하지 않아도 배포는 되지만, 미리 보고 싶다면 Docker 로:

```bash
docker run --rm -it -v "${PWD}:/srv/jekyll" -p 4000:4000 jekyll/jekyll:4 \
  bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

<http://localhost:4000/blog/> 에서 확인할 수 있습니다.

## 라이선스

테마는 [MIT](https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/LICENSE) 라이선스를 따릅니다.
