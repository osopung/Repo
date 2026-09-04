---
title: "사서 스킬 — ingest"
type: note
domain: other
status: final
updated: 2026-08-29
media: []
---

# 사서 스킬 — ingest

> 사서 ingest 손순. 재탄생 문서는 **노트만.**

## 내 한 줄

inbox의 날것을 읽고, 핵심·사서 인사이트·연결로 노트를 재탄생시킨다. 원본은 보관한다.

- [x] 감수

## 언제

- 사서 세션이 **시작**될 때 (`inbox/*.md`, `README.md`·숨김·`.gitkeep` 제외)
- 편집장이 `ingest <파일>`이라고 집을 때 — 그 파일만

접속 전에는 inbox에 두어도 된다. 사서가 먼저 건드리지 않는다.

## 순서

1. `git pull --ff-only`
2. 지침 원문(`고문에게` · `코덱스에게` · `헤르메스에게`)은 **그대로 inbox에 둔다**
3. **헤르메스가 보낸 스킬 초안**은 notes로 재탄생하지 않는다. 사서 검토 후 **줄인 것만** `_archive/`에 보관한다. 긴 초안은 두지 않는다.
4. 그 외 원문을 읽고 `**library/notes/`에만** 재탄생시킨다 (`art/`·`essays/`·`projects/`·ideas 아님)
5. 노트에 둔다 — 핵심 정리 · **사서 인사이트 (초안)** · `## 내 한 줄` (초안) · `## 연결` · slug는 짧게 · `status: draft` · `- [ ] 감수`
6. 원본은 지우지 않고 `_archive/`로 옮긴다 · `## 연결`에 `[[_archive/…|원본]]`
7. `map/log.md` append · `map/index.md` 최근만 · [[map/감수-대기]]·탐색기 빨간 표시 갱신
8. 편집장에게 건수·경로만 짧게 보고

## 하지 말 것

- 핵심이 안 보이면 **제안만 하고 그 건은 보류**
- idea 페이지 자동 생성 · 개념 쪼개기는 **제목 후보만** · `art/`·`essays/`·`projects/`로 ingest하지 않음 (승격은 편집장)
- 미디어 삭제·강제 이동 · `map/log` 과거 수정 · index 전량 재작성
- 헤르메스 스킬의 **긴 초안**을 보관하거나, 줄인 판을 `library/notes/`로 재탄생시키지 않기
- 한 줄·사서 인사이트를 최종으로 단정하거나 감수 체크를 대신하기

## 결과물

- `library/notes/` 재탄생 노트 (draft) · `_archive/` 원본 · log 한 줄 · 감수 대기 목록
- 아직 commit·push 하지 않는다 (`맞춰` 또는 세션 끝)

## 연결

- [[AGENTS#Ingest-규칙|AGENTS ingest]]
- [[library/notes/AI-직원을-만드는-핵심-인사이트]]
- [[library/notes/스킬-먼저-Cron]]
- [[library/ideas (생각의 축)/입구로서의-inbox|입구로서의 inbox]]
- [[오소풍]]

