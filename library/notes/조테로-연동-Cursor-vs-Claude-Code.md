---
title: "옵시디언 LLM Wiki에 조테로 연동 — Claude Code 대신 Cursor"
type: note
domain: other
status: final
updated: 2026-08-11
media: []
source: "https://docs.google.com/document/d/1GzJJX7SS4tOWtRzc2Ll5nplzscZqVGvaNuCigxI97RI/edit"
---

# 조테로 연동 — Claude Code 대신 Cursor

> Drive 추출 · 원본: [Google Doc](https://docs.google.com/document/d/1GzJJX7SS4tOWtRzc2Ll5nplzscZqVGvaNuCigxI97RI/edit)  
> (원문 Curse → **Cursor**)

## 내 한 줄

조테로·옵시디언 연동 작업은 Cursor로 충분하다 — 파일을 보며 고치는 쪽이 피로가 덜하다.

- [x] 감수

Claude Code와 Cursor는 형태만 다르고, **로컬 볼트·스크립트를 읽고 고치는 AI 에이전트**라는 점은 같다. 오소풍은 **Cursor 사서**가 본체다.

## Cursor를 써도 되는 이유

1. **파일 제어** — CLI든 IDE든 `.md`를 읽고 쓰면 결과는 같다.  
2. **시각적 확인** — 연동 스크립트·프론트매터·태그를 화면에서 바로 본다. Composer로 여러 파일 지시 가능.  
3. **규칙** — 프로젝트 규칙(AGENTS 등)으로 메타데이터·형식을 지키게 할 수 있다.

## 추천 워크플로 (오소풍)

1. Cursor로 `오소풍_wiki` 연다.  
2. 설치·템플릿은 [[library/notes/조테로-옵시디언-설치-사용법|설치·사용법]] 체크리스트대로.  
3. 논문 메모가 들어오면 사서에게 요약·백링크·`## 내 한 줄` 초안을 맡긴다.

## 결론

Claude Code = 터미널 경량 실행에 강함.  
**Cursor = 문서·코드를 눈으로 보며 튜닝** — 로컬 지식 베이스에는 이쪽이 편하다.

## 연결

- 원본: [[_archive/조테로-연동-Cursor-vs-Claude-Code|원본]]
- ★공부 [[library/notes/조테로-옵시디언-설치-사용법|설치·사용법]] · [[library/notes/조테로-LLM위키-연동-이점|연동 이점]]
- [[오소풍]] · [[AGENTS]]
