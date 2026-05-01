---
layout: ../../layouts/MarkdownPostLayout.astro
title: Setting
author: sixtick
description: "setting up astro"
image:
    url: "https://docs.astro.build/default-og-image.png"
    alt: "The word astro against an illustration of planets and stars."
pubDate: 2026-04-28
tags: ["astro", "setting", "sixtick"]
---
# SETTING


## 개발환경 준비하기
```sh
bun create astro@latest .
bun install
bun run dev
```
### vscode 확장 astro

### tailwind
```sh
bun x astro add tailwind
```
내부적으로 `bun add @tailwindcss/vite@^4.2.4 tailwindcss@^4.2.4` 를 실행한다.

프런트매터에 `import '../styles/global.css'` 를 추가해서 써야한다


## RSS 피드
### 패키지 설치
```
bun add @astrojs/rss
```
### 피드 문서 만들기
- src/pages/rss.xml.js
```
import rss, { pagesGlobToRssItems } from '@astrojs/rss';

export async function GET(context) {
  return rss({
    title: 'Astro Learner | Blog',
    description: 'My journey learning Astro',
    site: context.site,
    items: await pagesGlobToRssItems(import.meta.glob('./**/*.md')),
    customData: `<language>en-us</language>`,
  });
}
```
- astro.config.mjs 에 site 를 지정해야 한다


## 아일랜드
### preact 추가
```
bun x astro add preact --yes
```
- 경량 astro react
- bun add @astrojs/preact@^5.1.2 preact@^10.29.1 가 깔리며 설정을 수정해준다

### preact 사용
-  확장자 .jsx 를 사용한다
- client 지시어를 사용한다 (load, idle, visible, media, only)



- pages
- components
- layouts
- [tag].astro 
- getStaticPaths
- const allPosts = Object.values(import.meta.glob('./posts/*.md', { eager: true }));

