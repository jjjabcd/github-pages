---
layout: post
title: "Post Render + Image Load Test"
date: 2026-01-06
category: "Paper Review"
tags: ["Markdown", "Jekyll", "Image"]
permalink: /posts/2026-01-06-test-post/
---

## TL;DR
- Markdown이 post.html 레이아웃으로 렌더링되는지 확인
- assets/test 아래 png가 baseurl 포함 경로로 로드되는지 확인

## Image Test (Markdown)
![test-1]({{ site.baseurl }}/assets/test/1.png)

![test-2]({{ site.baseurl }}/assets/test/2.png)

![test-3]({{ site.baseurl }}/assets/test/3.png)

## Image Test (Figure + Caption)
<figure>
  <img src="{{ site.baseurl }}/assets/test/1.png" alt="test-1" />
  <figcaption>Figure 1. assets/test/1.png 렌더링 및 스타일 확인.</figcaption>
</figure>

## Code Test
```bash
ls -al
```

---

## 4) 빌드/배포 후 확인 URL

- 글: `https://jjiabcd.github.io/github-pages/posts/2026-01-06-test-post/`
- 이미지 직접 접근(정상 여부 확인용):  
  - `https://jjiabcd.github.io/github-pages/assets/test/1.png`

---

## 이어서 사용자가 할 수 있는 꼬리 질문 3개
1) 이미지가 큰 경우를 대비해서 `post.html`에 “click to zoom” 같은 lightbox 없이도 동작하는 순수 CSS/HTML 확대 뷰를 추가해줄까?  
2) `posts/`에서 `category` 기준으로 “Paper Review” 글만 모아보는 자동 리스트 페이지를 추가해줄까?  
3) Markdown에서 수식(MathJax)과 code highlighting(Rouge)을 안정적으로 쓰기 위한 최소 설정을 붙여줄까?

