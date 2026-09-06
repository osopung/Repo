# 오소풍_wiki — 설계도 완성본 (DESIGN v2)

| 항목 | 값 |
|------|-----|
| 상태 | **완성** (2026-08-01) |
| 볼트 경로 | `/Users/gimjongho/오소풍_wiki` |
| Obsidian Sync 이름 | `오소풍_wiki` |
| 운영 규칙 | [[AGENTS]] |
| 존재 이유 | [[purpose]] |
| v1 archive | `내 드라이브/오소풍의 모든것` (동결) |
| 미디어 보관 | `내 드라이브/오소풍-미디어-보관` (원본) |
| 공유 미디어 | ★5 `내 드라이브/오소풍-공유폴더` · [[library/notes/오소풍-공유폴더]] |

---

## 1. 왜 다시 짓는가

v1(`오소풍의 모든것`)은 Karpathy식 LLM Wiki 연습이었다. 배운 점:

| 교훈 | v2 대응 |
|------|---------|
| Inbox 무차별 ingest → slug·중복 폭발 | 선별은 편집장이 inbox에 · 사서는 온 것 바로 소화 · 짧은 slug · idea 자동생성 금지 |
| index/overview 자동 전량 유지 실패 | map은 허브·최근만 · 사람이 목차 주인 |
| Sync / Drive / Git 미러 혼선 | 텍스트 볼트 하나 + 미디어 보관 하나 |
| 미디어 전면 금지/전면 외부화 극단 | **필요 첨부는 허용**, 대용량만 밖+링크 |
| 논지 없는 저장 | purpose에 논지 · 「내 한 줄」 필수 |

옛 `oso-wiki`는 삭제했다. **이력·복구용**으로 `오소풍_wiki`에 새 로컬 Git을 둔다(선택 시 private 원격). daily 예약 자동화와는 별개.

---

## 2. 한 줄 정의

> **매일의 기록을 입구로**, 문학·예술·에세이와 연결하는 개인 LLM 위키.  
> **사람 = 편집장 · 에이전트 = 사서.**

---

## 2-1. 사람 vs 에이전트 (역할 분담)

한 줄로:

| | 사람 | 에이전트 (Cursor) |
|--|------|-------------------|
| 정체 | **편집장** — 의미·취향·최종 책임 | **사서** — 정리·연결·초안·검사 |
| 결정 | 무엇을 남길지, 무엇이 맞는 문장인지 | 어떻게 구조에 넣을지 제안·실행(허용 범위 내) |

### 사람만 한다 (에이전트 금지·최종 불가)

| 영역 | 내용 |
|------|------|
| 수집 | 폰·맥에서 `inbox/`에 쏟아붓기, 일기·STT·클립 |
| 최종 문장 | `## 내 한 줄` 다듬기 + **`- [x] 감수`**, purpose 논지, 에세이·작품의 **내 언어** |
| 미디어 판단 | 대용량을 보관소로 옮길지, 노트에 남길지 |
| Sync·기기 | Obsidian Sync 연결, 아이폰 vault 선택 |
| 승격 | `idea` 생성 승인 · cherry-pick · **내 한 줄 감수→정식** |
| 승인 | `daily`·`weekly` 제안 반영 여부, 논지·모순의 최종 판단 |
| 취향 | 무엇을 art/essays에 올릴지, 작품·글의 완성도 |

### 에이전트가 한다

| 영역 | 내용 |
|------|------|
| **접속 시 ingest** | 편집장이 사서에게 **접속한 시점**에 `inbox/` 미처리 `.md`를 `library/notes/`로 재탄생 (핵심·사서 인사이트 초안 · 대기 중엔 쌓아 둠 · 핵심 없으면 보류) |
| 초안 | 핵심 정리 · 사서 인사이트 **(초안)** · `## 내 한 줄` **(초안)** + `- [ ] 감수` · `status: draft` |
| 정식 반영 | 편집장이 `- [x] 감수`한 노트 → `(초안)` 제거 · `status: final` |
| **daily** | 관심·중요 일 기준 **제안 1~3개** (제안의 자동 반영 없음 · inbox는 위 규칙으로 소화) |
| 대화록 · AI 로그 | 합의 + **세 줄 세이브**(한 일/미결/다음) → `conversations/` 또는 daily |
| query | 위키 근거 답변, 에세이 개요 제안 |
| lint | 깨진 링크·고아·누락 검사 / `--fix` 시 안전 수정만 |
| log | `map/log.md` **append만** |
| index | 허브·최근 **소량** 갱신 (전량 재작성 금지) |

### 에이전트가 하지 않는다

- idea 자동 생성 · v1 전량 이관(사람이 inbox에 넣지 않은 것을 끌어오기)
- 미디어 삭제·강제 외부 이동
- log 과거 블록 수정, index 전량 자동 재작성
- 「내 한 줄」·논지를 사람 승인 없이 최종본으로 단정
- Sync 설정 변경, 볼트/원격 삭제·생성 (사람 명시 요청 전)
- v1 전량 이관

### 협업 흐름

```
사람:  capture(inbox) / 승인 / 문장 고치기 / 미디어·Sync
에이전트: 접속 시 inbox ingest · 초안 · daily · lint · 대화록·AI 로그 · weekly 제안
         ↓
사람:   (초안)→내 문장 · daily/weekly 반영 · idea 승격
```

세부 실행 규칙은 [[AGENTS]]가 우선한다.

---

## 2-2. daily — 사서의 하루 제안

전체를 매일 순회하지 않는다. **짧은 스캔 + 제안 ≥ 1 · ≤ 3.**

**언제:** 매일 09:00(KST) 이후, 그날 사서와 처음 대화할 때 자동 준비. 클라우드 예약 없음(Git은 이력용일 뿐).  
**전달:** 채팅 맨 앞에 **Cursor 클릭 링크** — `[오늘의 daily](map/daily/YYYY-MM-DD.md)` (wikilink만 금지 · 채팅에서 안 열림). 가능하면 파일도 연다.  
**weekly:** `[주간 weekly](map/weekly/YYYY-MM-Wn.md)` 같은 방식으로 채팅에 올린다. 파일명 = 그달의 월요일 시작 주(`2026-08-W4`).  
**언제:** **주일 아침**, 그날 사서와 처음 대화할 때 — 편집장이 말하지 않아도 **지난주**를 작성(없으면)·띄운다. 지난주 = 직전 월요일 시작 주. 기준은 편집장이 행한 가치 있는 일.

### 스캔 범위 (이것만)

1. `오소풍.md` 사서 메모리 카드 · `purpose.md` 논지 · `Home.md` 오늘/이번 주·이번 달 초점  
2. `inbox/` 미처리  
3. 최근 `library/notes/`, `projects/` (수일)  
4. 손 닿는 `art/` · `essays/` · `conversations/` 미결  

### 제안 종류 (예시)

- **오늘의 하이라이트** — 그날 한 줄. 사서가 `(초안)` 추천 · 편집장이 감수  
- 오늘 이을 **한 줄·한 장면**  
- (inbox 미처리는 **접속 시** ingest — daily 제안 목록에 넣지 않아도 됨)  
- art/essays로 옮길 조각  
- 이을 `[[링크]]`  
- weekly에 올릴 논지 후보  

### 출력

- 위치: `Home.md` → **오늘의 하이라이트** · **사서 제안 (오늘)** 을 덮어씀 (당일분)  
- `map/daily/YYYY-MM-DD.md`에 **오늘의 하이라이트** 절을 매일 둠 (`(초안)` + `- [ ] 감수`)  
- (선택) 남기고 싶으면 `map/daily/YYYY-MM-DD.md`에 복사  
- `map/log.md`에 `daily | …` **append**  
- daily **제안**으로는 노트 생성·논지 확정하지 않음 (inbox **접속 시** ingest는 §7·[[AGENTS]] 별도)

### daily vs weekly

| | daily | weekly |
|--|-------|--------|
| 리듬 | 매일 (또는 여는 날) | **주일 아침** 첫 대화 (지난주 · 말하지 않아도) |
| 초점 | 지금 관심·중요 일 **한두 가지** | 논지·Home·moc 손질 |
| 분량 | 제안 1~3줄 블록 | 좀 더 넓은 제안 |

---

## 3. 우선순위

| 순위 | 영역 | 폴더·루프 |
|------|------|-----------|
| **1** | **기록·일상 (C)** | `inbox/` → `library/notes/` 가 메인 |
| 2 | 문학·예술 | `essays/`, `art/` |
| 3 | 기타 (투자 등) | 필요할 때만 `library/notes/` |

문학·예술은 “관심의 무게”가 크지만, **운영의 최우선은 끊기지 않는 기록**이다.

---

## 4. 폴더 구조

```
오소풍_wiki/
├── DESIGN-v2.md          ← 이 문서 (설계 원본)
├── AGENTS.md             ← LLM/Cursor 운영 규칙
├── purpose.md            ← 목표 · 핵심 질문 · 논지
├── Home.md               ← 사람용 입구 (오늘/이번 주)
│
├── inbox/                ← 쏟아붓기. 분류·요약·링크 작업 금지
│
├── library/
│   ├── notes/            ← ingest 재탄생 (핵심·사서 인사이트 초안)
│   ├── ideas (생각의 축)/ ← 반복 개념 (소수 · 승격제)
│   ├── projects/         ← 여행·루틴·진행 중 일
│   ├── ops/              ← 에이전트 지침 (헤르메스·고문·코덱스 — 상주 운영 문서)
│   └── skills/           ← 확정·활성 스킬 (매일 자료검색 등)
│
├── essays/               ← 에세이·시상·칼럼 초고
│
├── art/                  ← 캘리·그림·사진 작품
│   ├── calligraphy/
│   ├── drawing/
│   ├── photo/
│   └── _index.md
│
├── conversations/        ← Cursor·사람 대화록 (주제·날짜로 축적)
│   ├── _index.md         ← 주제별 · 날짜별 목차
│   └── YYYY-MM-DD-주제.md
│
├── map/
│   ├── index.md          ← 허브·최근 (전량 자동 재작성 금지)
│   ├── log.md            ← append-only 변경 이력
│   ├── daily/            ← (선택) daily 제안 보관
│   └── moc/              ← 주제 지도 (선택)
│
├── 집 설계도/             ← 집의 구조·설계 문서 (완성 설계도 · 맥 폴드 트리)
├── assets/               ← 노트에 붙는 가벼운 첨부
└── _archive/             ← v1 이관 대기 · CHERRY-PICK.md
```

### 폴더 역할 한 줄

| 폴더 | 한 줄 |
|------|--------|
| `inbox/` | 일단 넣는다 |
| `library/notes/` | ingest로 재탄생한 것 (핵심·사서 인사이트 초안). 승격 전 전부 여기 |
| `library/ideas (생각의 축)/` | 세 번 이상 만나거나, 내가 축으로 쓰는 개념만 |
| `library/projects/` | 끝나지 않은 일 |
| `library/ops/` | 에이전트 지침 — 상주 운영 문서 (inbox 아님) |
| `library/skills/` | 확정·활성 스킬 — Cron이 부르는 손 |
| `essays/` | 문장으로 쓰는 작업실 |
| `art/` | 작품(시각) 작업실 — 글과 섞지 않음 |
| `conversations/` | LLM·Cursor 대화 결정·합의 축적 |
| `map/` | 지도·목차·이력 |
| `집 설계도/` | 집의 구조·설계 문서 |
| `assets/` | Sync에 올려도 되는 작은 미디어 |

연결은 폴더가 아니라 `[[wikilink]]`와 `map/moc/`가 한다.

---

## 4-1. 대화록 (`conversations/`)

위키를 키우는 **대화 자체**도 지식이다. 채팅 전문을 덤프하지 않고,  
**주제·날짜·결정**만 남겨 쌓는다.

### 파일명

```
conversations/YYYY-MM-DD-짧은주제.md
```

예: `2026-08-01-wiki-design-v2.md`

### Frontmatter

```yaml
---
title: ""
type: conversation
topics: [design, media, sync]    # 주제 태그 (복수 OK)
date: YYYY-MM-DD
agents: [cursor]
updated: YYYY-MM-DD
---
```

### 본문 형식

```markdown
## 맥락
한두 문장 — 왜 이 대화를 했는가.

## 세 줄 세이브 (AI 로그)
- **한 일:** …
- **미결:** …
- **다음:** …

## 합의 · 결정
- 결정 1
- 결정 2

## 미결
- 남은 질문

## 연결
- [[DESIGN-v2]] · [[관련 노트]]

## 메모
필요한 인용·세부만 (전문 붙여넣기 금지)
```

### AI 로그 (세 줄 세이브) — 오소풍 최소안

긴 Cursor 세션 끝에 **한 일 / 미결 / 다음**만 남긴다. (`map/log`는 시스템용 · 작업 세이브와 분리)  
짧은 세션이면 당일 `map/daily/`에 같은 세 줄만 append. 규칙: [[AGENTS#AI-로그-세-줄-세이브]].

### 축적 규칙

| 규칙    | 내용                                              |
| ----- | ----------------------------------------------- |
| 언제 쓰나 | 설계·정책·큰 ingest 방향이 바뀔 때 · 사용자가 `대화록`/`AI 로그`를 요청할 때 · **긴 세션 끝** |
| 주제    | `topics:` + `_index.md`의 주제 섹션에 링크              |
| 날짜    | 파일명 앞날짜 · `_index.md` 최근 목록                     |
| 분량    | 결정 중심 + 세 줄 세이브. 채팅 로그 원문 전체 복붙 금지                        |
| index | `conversations/_index.md`에 주제별·최근만 갱신 (전량 자동 X) |
| log   | `map/log.md`에 `conversation \| 주제` append       |

### 주제 바구니 (시작 세트 — 늘려 감)

- `design` — 구조·규칙·DESIGN
- `media` — 첨부·보관소·Sync 용량
- `sync` — 볼트·기기·원격 이름
- `ingest` — 이관·선별·루프
- `art` / `literature` / `life` — 영역별 대화
- `ops` — lint, weekly, 도구

---

## 5. 페이지 타입·형식

### 타입

| type | 위치 | 생성 조건 |
|------|------|-----------|
| `note` | `library/notes/` | ingest 확정 |
| `idea` | `library/ideas (생각의 축)/` | 사람 승인 후에만 (에이전트는 후보 제안) |
| `project` | `library/projects/` | 진행 중인 일 |
| `essay` | `essays/` | 창작 글 |
| `artwork` | `art/**` | 캘리·그림·사진 작품 |
| `conversation` | `conversations/` | 설계·정책 합의 대화 정리 |
| `moc` | `map/moc/`, `art/_index.md`, `conversations/_index.md` | 주제 지도 |

### Frontmatter (공통)

```yaml
---
title: ""
type: note | idea | project | essay | artwork | moc
domain: life | literature | art | other
status: draft | final  # 감수 전 draft · 감수 후 final
updated: YYYY-MM-DD
media: []          # 외부 대용량 경로 (있을 때만)
---
```

### note / essay 본문 최소

```markdown
## 한 줄 요약
## 핵심
## 내 한 줄          ← 없으면 ingest 미완료
(초안) …             ← 사서 초안일 때
- [ ] 감수           ← 편집장이 체크하면 정식 (사서가 status: final)
## 연결
## 모순               ← 있을 때만
```

### artwork 본문 최소

```markdown
## 작품
## 의도 · 재료 · 구도
## 내 한 줄
## 연결               ← essays, notes 등
```

### slug

- 짧고 읽히게 (권장 ≤ 40자)
- inbox 원본 장문 파일명을 slug로 쓰지 않음
- 예: `2026-08-01-diary`, `nataeju-selected`, `calligraphy-lesson-1`

---

## 6. 미디어 정책

### 원칙

**노트에 사진·PDF를 금지하지 않는다.**  
의미에 필요하면 넣는다.  
**용량이 큰 것**만 볼트 밖으로 빼고 링크한다 — 판단은 작성자.

### 배치

| 상황 | 위치 | 노트 |
|------|------|------|
| **작품·시화·갤러리 원본** | **노션 아트갤러리** | `art/` 노트에 URL · `media:` 필드. 허브: [[art/_index]] |
| 미리보기·편지 등 필수 첨부 (작은 이미지) | 볼트 `assets/` | `![[파일]]` OK |
| **위키에 걸 미디어 (맥·아이폰)** | ★5 `오소풍-공유폴더/` | `https://drive.google.com/file/d/FILE_ID/view` · [[library/notes/오소풍-공유폴더]] |
| 원본·비공유 대용량 (갤러리 밖) | `오소풍-미디어-보관/` | 참고 경로 · 클릭용 `file://` 금지 |

노션 갤러리: [오소풍의 갤러리 / 시화 갤러리](https://app.notion.com/p/osopung58/53279f80606d4f878ae6f9107c53d6c7)

### 에이전트 금지

- 미디어 임의 삭제
- 대용량을 사람 동의 없이 외부로 강제 이동
- Sync 용량 “최적화”를 이유로 첨부 일괄 제거

사람은 언제든 큰 파일을 미디어 폴더로 옮기고 링크만 남길 수 있다.

---

## 7. 명령어 (Cursor)

| 명령 | 동작 |
|------|------|
| _(접속 시)_ / `ingest <파일>` | 사서 **접속(대화 시작) 시점**에 inbox 미처리 ingest. 특정 파일만 `ingest <파일>`. **내 한 줄**(초안) 필수. log append |
| `query: <질문>` | 위키만 근거로 답변. 필요 시 essays 초안 제안 |
| `대화록` / `conversation` | 이번 대화의 합의·결정을 `conversations/YYYY-MM-DD-주제.md`로 정리 · `_index`·log 갱신 |
| `AI 로그` | 긴 세션 끝 **세 줄 세이브**(한 일/미결/다음) · conversations 또는 당일 daily |
| `daily` | §2-2 — 관심·중요 일 기준 제안 1~3개 → Home「사서 제안」·log append (자동 반영 없음) |
| `lint` | 검사만 보고 |
| `lint --fix` | 안전 수정만 자동 + 나머지는 초안/제안 ([[AGENTS]] 참고) |
| `weekly` | Home·논지·moc 갱신 **제안** + **스킬 개선 후보 1개** ([[map/moc/스킬]] 상행 루프) — 사람 승인 후 반영 |

### Ingest 워크플로

**기본:** 사람이 파일마다 `ingest …`를 치지 않는다. inbox에 쌓아 두고, **사서에게 접속한 시점**에 소화한다.

1. 세션 시작 시 `inbox/` 스캔 (README·숨김 제외) — **건수 제한 없이** 처리  
2. `map/index.md`, `purpose.md`로 맥락 파악  
3. 목적지: **`library/notes/` 전부.** 핵심 정리 · 사서 인사이트(초안) · `## 내 한 줄`(초안)으로 재탄생. `art/`·`essays/`·`projects/`·ideas는 ingest가 아님 (승격은 편집장)  
   - 핵심이 안 보이면 **제안만 하고 해당 건 보류**  
4. 짧은 slug로 노트 작성  
5. idea는 **후보만** 제안 (자동 생성 금지)  
6. inbox 원본 → `_archive/`(또는 유지) · 파일 덤프 복사 금지  
7. `## 연결`에 **원본 위키링크** `[[_archive/…|원본]]` 넣기 (경로 문자열만 금지)  
8. `map/log.md`에 append  
9. `map/index.md` 허브·최근만 손댐 (전량 재작성 금지)  
10. 변경 요약 출력  

**선별은 입구에서:** 무엇을 inbox에 넣을지는 편집장. 사서는 inbox에 온 것을 막지 않고 소화한다. (v1처럼 아카이브 전체를 끌어오지는 않음.)

### log = append-only

`map/log.md`는 **뒤에만 붙인다.**  
과거 날짜 블록을 수정·삭제·덮어쓰지 않는다.

```markdown
## [YYYY-MM-DD] ingest | 짧은-제목
- …
```

---

## 8. Lint

**검사**

- 깨진 `[[wikilink]]`
- `## 내 한 줄` 없는 note/essay
- 고아 페이지 (inbox·log·index·DESIGN·AGENTS·purpose·Home 제외)
- 3회+ 언급이나 idea 없는 후보
- media 링크 표기만 있고 경로 메모가 모호한 경우 (제안)

**`lint --fix`**

| 자동 | 초안(사람 고침) | 제안만 |
|------|-----------------|--------|
| 명확한 깨진 링크 retarget | `## 내 한 줄` `(초안)` | idea 신규 생성 |
| frontmatter 기본 필드 보정 | | 미디어 이동·삭제 |
| index 최근 항목 소량 보강 | | 논지·모순 최종 판단 |
| | | log 과거 수정 |

---

## 9. 일상 루프 (C 중심)

```
[아이폰 Obsidian]
  inbox에 메모·STT·클립
        │ Sync
        ▼
[맥 Obsidian] 읽기·가벼운 링크
        │
        ▼
[맥 Cursor]
  inbox 접속 시 ingest → library/notes/ | projects/ | art/ | essays/
  map/log append
        │
        ▼
[주 1회] weekly
  purpose 논지 · Home · moc 손질
```

### 기기·저장소

| 위치 | 역할 |
|------|------|
| `~/오소풍_wiki` | 유일한 텍스트 위키 + Obsidian Sync |
| `오소풍-미디어-보관` | 대용량 원본 (비공유) |
| ★5 `오소풍-공유폴더` | 위키 클릭용 공유 미디어 · [[library/notes/오소풍-공유폴더]] |
| `오소풍의 모든것` | v1 archive — 신규 작업 금지 |
| Git (`osopung/Repo`) | 이력·복구 (Sync와 병행). inbox push는 **헤르메스·고문·코덱스** — 문은 inbox 하나 (2026-09-05). **Cursor Cloud는 집 Git 경로가 아님.** 공장: `osopung/Factory` (비밀 파일 금지) |

---

## 10. v1에서 가져오기

원칙: **전량 이관 금지.**  
목록·체크: [[_archive/CHERRY-PICK]]

방법:

1. 체크한 항목만 v1에서 읽는다  
2. **새 slug·새 형식**으로 v2에 다시 쓴다 (파일 덤프 복사 금지)  
3. log에 `ingest | from-v1 …` append  

우선 후보: 일기·Wispr·기록강의·회동·여행 · (선택) 시·캘리.

테슬라·대량 이미지 카탈로그는 일상 루프가 안정된 뒤.

---

## 11. 구축 순서 (실행 체크리스트)

### 에이전트가 한 것 (시스템 구축)

- [x] 볼트 경로·이름 확정 (`~/오소풍_wiki`)
- [x] 옛 oso-wiki 로컬·원격 삭제 → 이력용 새 Git 재도입 (2026-08-03)
- [x] 폴더 골격 · AGENTS · purpose · Home · map · art · conversations
- [x] DESIGN-v2 완성 · 역할 분담 · daily
- [x] `.obsidian` 최소 설정 (새 노트→inbox, 첨부→assets, Sync on)
- [x] `templates/` (note · essay · artwork · conversation)
- [x] [[SETUP]] — 사람용 마무리 체크리스트
- [x] Cursor 워크스페이스 → `오소풍_wiki`

### 사람이 할 일 (다음) — [[SETUP]] 상세

- [x] Obsidian에서 `오소풍_wiki` vault 열기  
- [x] Sync 맥·아이폰 연결  
- [x] purpose 문장 다듬기 · inbox 1건 · `ingest` · `daily`  
- [x] CHERRY-PICK 3~5개 (선택)  

### 하지 말 것

- v1 91소스를 한 번에 ingest  
- index 전량 자동 생성에 의존  
- 미디어를 에이전트에게 “전부 밖으로” 맡기기  

---

## 12. 성공 기준 (1주 후)

1. 아이폰 inbox → 맥 ingest가 **막히지 않고** 돈다  
2. 새로 만든 note마다 `## 내 한 줄`이 있다  
3. `art/` 또는 `essays/`에 손이 가는 항목이 **1개 이상** 있다  
4. Sync가 버틸 만큼 볼트가 가볍다 (큰 파일은 내가 밖으로)  
5. “어느 폴더가 진짜 볼트지?” 질문이 다시 나오지 않는다  

---

## 13. 문서 관계

```
DESIGN-v2.md       ← 설계 원본 (왜·무엇·어디에)
AGENTS.md          ← 에이전트 실행 규칙 (어떻게)
purpose.md         ← 철학·논지 (무엇을 위해)
Home.md            ← 매일 여는 문
conversations/     ← 대화에서 나온 합의 축적
```

설계를 바꿀 때는 이 문서를 고치고, `map/log.md`에  
`## [날짜] design | …` 로 append한다.  
큰 합의가 나온 대화는 `conversations/`에도 남긴다.
