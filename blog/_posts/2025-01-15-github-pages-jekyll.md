---
layout: post
title: "GitHub Pages + Jekyll로 개발 블로그 시작하기"
description: "정적 사이트 생성기 Jekyll과 GitHub Pages를 활용해 무료로 개인 기술 블로그를 운영하는 방법을 소개합니다."
date: 2025-01-15
tags: [Jekyll, GitHub]
---

GitHub Pages와 Jekyll을 사용하면 **무료로** 빠르고 깔끔한 개발 블로그를 만들 수 있습니다. 이 포스트에서는 전체 셋업 과정을 단계별로 설명합니다.

## 왜 GitHub Pages인가?

정적 사이트 호스팅 옵션은 많지만 GitHub Pages를 선택하는 이유는:

- 완전 **무료** 호스팅
- GitHub 저장소와 **자동 배포** 연동
- `yourusername.github.io` 도메인 제공
- 커스텀 도메인 연결 가능

## Jekyll 설치

로컬 개발 환경 세팅:

```bash
# Ruby 설치 확인
ruby -v

# Jekyll & Bundler 설치
gem install jekyll bundler

# 새 Jekyll 사이트 생성
jekyll new my-blog
cd my-blog

# 로컬 서버 실행
bundle exec jekyll serve
```

이제 `http://localhost:4000`에서 블로그를 미리 볼 수 있습니다.

## GitHub Pages 배포

```bash
# Git 저장소 초기화
git init
git add .
git commit -m "Initial commit"

# GitHub 원격 저장소 연결
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

저장소 Settings → Pages → Source를 `main` 브랜치로 설정하면 자동으로 배포됩니다.

## 포스트 작성하기

`_posts` 폴더에 `YYYY-MM-DD-title.md` 형식으로 파일을 만들면 됩니다.

```markdown
---
layout: post
title: "나의 첫 포스트"
date: 2025-01-15
tags: [블로그]
---

본문 내용을 마크다운으로 작성합니다.
```

> **팁**: Front Matter의 `description` 필드를 작성하면 카드와 SEO 메타태그에 활용됩니다.

## 마치며

한번 설정해두면 글 쓰는 것에만 집중할 수 있어서 편리합니다. 다음 포스트에서는 댓글 기능(Giscus)과 구글 애널리틱스 추가하는 방법을 다루겠습니다.
