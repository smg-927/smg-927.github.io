---
layout: default
title: 소개
permalink: /about/
---

<div style="padding: 40px 0 48px;">
  <div class="hero-tag">About</div>
  <h1 style="font-size: clamp(24px, 4vw, 36px); font-weight: 700; letter-spacing: -0.03em; margin: 16px 0 12px;">안녕하세요 👋</h1>
  <p style="font-size: 16px; color: var(--text-muted); line-height: 1.8; max-width: 540px;">저는 <strong style="color: var(--text);">{{ site.author }}</strong>입니다. 영화, 힙합, 게임을 사랑합니다.</p>
</div>

<div class="prose">

## 블로그에 대해

주인장의 공부 노트이자 개인 기록장입니다.

주로 다루는 내용:

- 유니티 게임개발 — 프로젝트 & 각종 기술들

- 그래픽스 — OpenGL, DirectX, Shader Programming

- 일상 — 게임 리뷰, 영화 리뷰 등등

## 연락하기

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