# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Henrry Lee의 개인 프로필 웹사이트. 빌드 도구 없이 HTML/CSS/JS만으로 구성된 싱글페이지 정적 사이트.

## Development

빌드/번들링 과정 없음. 브라우저에서 `index.html`을 직접 열면 동작한다.
Tailwind CSS는 CDN(`https://cdn.tailwindcss.com`)으로 로드되므로 인터넷 연결이 필요하다.

## Architecture

- `index.html` — 전체 페이지 마크업 + Tailwind 유틸리티 클래스 (Nav, Hero, About, Skills, Projects, Contact, Footer)
- `style.css` — Tailwind로 커버되지 않는 커스텀 스타일 (fade-in 애니메이션, blob morph 애니메이션, 스크롤바, 셀렉션 색상)
- `script.js` — 모바일 메뉴 토글, Intersection Observer 기반 스크롤 애니메이션, 스크롤 위치 기반 네비게이션 하이라이트

## Conventions

- 라이트 테마: `bg-cream`(#FFF8F0) 배경, `text-dark`(#2B2B2B) 기본 텍스트
- 포인트 컬러: `mustard`(#E8A838) 주요 액센트, `teal`(#2D8B8B) 보조 액센트
- 헤딩 폰트: Playfair Display (Google Fonts CDN), 본문: Pretendard / system-ui
- Tailwind 커스텀 색상은 `index.html` 내 인라인 `tailwind.config`에 정의
- 섹션 추가 시 `fade-in` 클래스를 부여하면 스크롤 시 자동으로 페이드인 애니메이션 적용
- 레퍼런스 디자인은 `reference_designs/` 디렉토리에 보관
