---
title: "Factory 안내"
type: note
domain: other
status: final
updated: 2026-09-09
media: []
source: "https://docs.google.com/document/d/1cQ0eq_kZ9T6nOLfupPRIfXKVAeiAfo4L6zjv1KTa3QE/edit"
---

# Factory

Factory 경로: 루트 `README.md`

오소풍의 **공장**. 오소풍 AI Studio의 책·수묵 캘리그래피·AI 제품 작업을 기록하고 인계하는 GitHub 작업장.

`osopung/Repo`는 별도의 위키. 이 저장소에는 제품 작업과 인수인계 기록을 둔다.

## 내 한 줄

일은 Factory, 맥락의 집은 위키. 둘을 한 레포로 합치지 않는다.

- [x] 감수

## Studio

회사 기준과 에이전트별 작업방은 `studio/` 아래.

| 담당 | 역할 | 작업방 |
|---|---|---|
| Cursor | 출판 제작 | `studio/agents/cursor/` |
| Gemini | 수묵 캘리그래피 구현 | `studio/agents/gemini/` |
| Codex | AI 제품 개발 | `studio/agents/codex/` |
| Hermes | 조사·운영 지원 | `studio/agents/hermes/` |

각 에이전트는 자기 방과 작업지시서가 배정한 위치만 수정한다. 저장소 전체 규칙은 `AGENTS.md`.

## 비밀

API 키·비밀번호·OAuth 파일은 저장소에 넣지 않는다. 실제 값은 로컬 `.env`에서만.

## 앱

- Prompt List Dashboard — 에세이·이미지·대화·기타 프롬프트 보관함
- AI Agent Practice — AI 에이전트 학습을 정리하고 실습하는 개인용 AI 제품

앱의 기존 기술 지침은 유지한다. 수정 담당과 범위는 기획실장의 작업지시서에서 정하고, 오소풍이 착수와 결과를 승인한다.

## 연결

- [[library/projects/프롬프트-리스트-대시보드]]
- [[오소풍 AI Studio/02-Factory/공용-작업-규칙]] · [[오소풍 AI Studio/_index]]
