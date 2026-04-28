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


