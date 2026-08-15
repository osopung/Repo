---
title: "위키 v2 설계 — 대화 합의"
type: conversation
topics: [design, media, sync, life]
date: 2026-08-01
agents: [cursor]
updated: 2026-08-10

---

## 맥락

v1 LLM Wiki가 마음에 들지 않아 연습으로 두고, `오소풍_wiki`로 처음부터 다시 짓기로 함.  
설계 합의와 미디어·동기화 혼선을 정리한 대화.

## 합의 · 결정

- 볼트 이름: **오소풍_wiki** (오소풍_텍스트 아님)
- 경로: **`~/오소풍_wiki`** (Google Drive 밖)
- 최우선 쓰임: **C 기록·일상** — 문학·예술은 관심 영역으로 `essays/`·`art/`
- `art/` 폴더 (calligraphy / drawing / photo)
- 미디어: **전면 금지 아님** — 필수 사진·PDF는 노트·`assets/` OK. 대용량만 `오소풍-미디어-보관` + 링크 (판단은 사람)
- `oso-wiki` 로컬·GitHub **삭제** — 혼동 제거
- v1(`오소풍의 모든것`)은 archive · 전량 이관 금지 · cherry-pick만
- `map/log.md` = **append-only**
- 대화록을 `conversations/`에 주제·날짜로 **축적**하기로 함
- 설계 원본: [[DESIGN-v2]]
- **inbox 자동 ingest:** 투입된 `.md`는 **제한 없이 바로** 소화 (파일별 `ingest` 명령 불필요 · 애매하면 보류). 선별은 편집장이 inbox에 넣을 때. v1 아카이브 전체를 사서가 끌어오지는 않음.
- **내 한 줄 감수:** `- [ ] 감수` + `status: draft` → 편집장이 문장 다듬고 `- [x] 감수` → 사서가 `(초안)` 제거·`status: final` (정식 노트)
- **아트 원본 = 노션:** [시화 갤러리](https://app.notion.com/p/osopung58/53279f80606d4f878ae6f9107c53d6c7) · 위키 `art/`는 링크·한 줄·연결만
- **daily 준비:** 매일 09:00 이후 사서와 처음 대화 시 자동 (git·예약 자동화 안 씀)

## 미결

- [x] Obsidian Sync를 `오소풍_wiki`에 연결 (맥·아이폰)
- [x] purpose 논지를 내 문장으로 다듬기
- [x] 첫 inbox → ingest 성공
- [x] CHERRY-PICK 3~5개 체크 후 이관
- [x] inbox 자동 ingest 규칙 반영

## 연결

- [[DESIGN-v2]] · [[AGENTS]] · [[purpose]] · [[Home]]
- [[_archive/CHERRY-PICK]]
- [[conversations/_index|대화록 목차]]

## 메모

- v1에서 아이폰에 링크가 안 보이던 이슈: Sync 본체는 Drive v1볼트였고, Mac `file://` 링크는 아이폰에서 무용. v2는 볼트 단일화로 혼선을 줄임.
