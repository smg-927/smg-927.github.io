# DevLog — GitHub Pages 블로그

다크 테마의 개발/기술 블로그 템플릿입니다.

---

## 🚀 빠른 시작

### 1단계: GitHub 저장소 만들기

저장소 이름을 반드시 **`yourusername.github.io`** 형식으로 만드세요.  
(예: `hong123.github.io`)

### 2단계: 파일 업로드

```bash
git clone https://github.com/yourusername/yourusername.github.io.git
cd yourusername.github.io

# 이 블로그 파일들을 모두 복사한 후
git add .
git commit -m "블로그 초기 설정"
git push origin main
```

### 3단계: GitHub Pages 활성화

1. GitHub 저장소 → **Settings** 탭
2. 왼쪽 메뉴 → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** / **(root)** 선택 → **Save**

약 1~2분 후 `https://yourusername.github.io`에서 확인 가능합니다.

---

## ✏️ 개인 정보 수정

`_config.yml` 파일을 열어서 수정하세요:

```yaml
title: "내 블로그 이름"
description: "블로그 소개 문구"
author: "홍길동"
email: "hong@example.com"
github_username: "honggildong"
url: "https://honggildong.github.io"
```

---

## 📝 포스트 작성 방법

`_posts/` 폴더에 파일을 만들 때 **반드시** 이 형식을 따르세요:

**파일명**: `YYYY-MM-DD-영문-제목.md`  
예: `2025-02-01-my-first-post.md`

**파일 내용**:
```markdown
---
layout: post
title: "포스트 제목"
description: "간단한 설명 (카드에 표시됩니다)"
date: 2025-02-01
tags: [JavaScript, React]
---

여기에 본문을 마크다운으로 작성하세요.

## 소제목

코드 블록도 지원합니다:

```python
def hello():
    print("Hello, World!")
```
```

---

## 🔧 로컬에서 미리보기

```bash
# Ruby & Jekyll 설치 (최초 1회)
gem install bundler jekyll

# 의존성 설치
bundle install

# 로컬 서버 실행
bundle exec jekyll serve

# 브라우저에서 확인
# http://localhost:4000
```

---

## 🎨 커스터마이징

### 색상 변경
`assets/css/main.css` 파일의 `:root` 섹션에서 CSS 변수를 수정하세요:

```css
:root {
  --accent: #7c6aff;    /* 메인 포인트 컬러 */
  --bg:     #0a0a0f;    /* 배경색 */
}
```

### 소개 페이지 수정
`about.md` 파일을 자유롭게 편집하세요.

---

## 💡 포스트 팁

- **태그**는 배열 형식으로 작성: `tags: [JavaScript, 알고리즘]`
- **description** 필드가 있으면 목록 카드에 표시됩니다
- 코드 블록 문법 하이라이팅: \`\`\`언어이름 형식 사용
- 이미지는 `assets/` 폴더에 넣고 `![alt]({{ '/assets/image.png' | relative_url }})` 형식으로 참조

---

Made with Jekyll & ❤️
