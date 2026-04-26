---
layout: default
title: 소개
permalink: /about/
---

<div style="padding: 40px 0 48px;">
  <div class="hero-tag">About</div>
  <h1 style="font-size: clamp(24px, 4vw, 36px); font-weight: 700; letter-spacing: -0.03em; margin: 16px 0 12px;">안녕하세요 👋</h1>
  <p style="font-size: 16px; color: var(--text-muted); line-height: 1.8; max-width: 540px;">저는 <strong style="color: var(--text);">{{ site.author }}</strong>입니다. 소프트웨어 개발을 좋아하고, 배운 것들을 이곳에 기록합니다.</p>
</div>

<div class="prose">

## 이 블로그에 대해

코드를 작성하면서 마주치는 문제들, 새로 배운 기술들, 그리고 개발하면서 드는 생각들을 기록합니다.

주로 다루는 내용:

- **웹 개발** — Frontend, Backend, DevOps
- **알고리즘 & 자료구조** — 문제 풀이 및 최적화
- **도구 & 워크플로우** — 개발 생산성 향상
- **오픈소스** — 기여 경험 및 프로젝트

## 연락하기

궁금한 점이나 이야기하고 싶은 내용이 있다면 아래 채널로 연락해주세요.

</div>

<div class="about-links" style="gap: 16px; flex-wrap: wrap;">
  {% if site.github_username %}
    <a href="https://github.com/{{ site.github_username }}" target="_blank" rel="noopener" style="font-size: 14px; font-family: var(--font-mono); color: var(--text-muted); text-decoration: none; display: flex; align-items: center; gap: 6px; padding: 10px 16px; background: var(--bg-2); border: 1px solid var(--border); border-radius: var(--radius); transition: all 0.2s;" onmouseover="this.style.borderColor='rgba(124,106,255,0.4)';this.style.color='var(--accent)'" onmouseout="this.style.borderColor='var(--border)';this.style.color='var(--text-muted)'">
      ↗ github.com/{{ site.github_username }}
    </a>
  {% endif %}
  {% if site.email %}
    <a href="mailto:{{ site.email }}" style="font-size: 14px; font-family: var(--font-mono); color: var(--text-muted); text-decoration: none; display: flex; align-items: center; gap: 6px; padding: 10px 16px; background: var(--bg-2); border: 1px solid var(--border); border-radius: var(--radius); transition: all 0.2s;" onmouseover="this.style.borderColor='rgba(124,106,255,0.4)';this.style.color='var(--accent)'" onmouseout="this.style.borderColor='var(--border)';this.style.color='var(--text-muted)'">
      ↗ {{ site.email }}
    </a>
  {% endif %}
</div>
