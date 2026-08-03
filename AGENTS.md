# LLM Wiki — 오소풍_wiki

개인 **기록·일상**을 중심에 두고, 문학·예술·에세이를 연결하는 LLM 위키다.  
상세 설계: [[DESIGN-v2]] · 역할 분담: [[DESIGN-v2#2-1-사람-vs-에이전트-역할-분담|§2-1]].

## 사람 vs 에이전트

**사람 = 편집장** · **에이전트 = 사서.**

| | 사람 | 에이전트 |
|--|------|----------|
| 한다 | inbox 수집, **내 한 줄 감수 체크**, 미디어·Sync, idea 승격, daily/weekly 승인, [[오소풍]] 카드 감수 | **대화 전 [[오소풍]] 필독**, **inbox 자동 ingest**, 초안, 감수→정식 반영, daily, 대화록, query, lint, log append, 오소풍 카드 보강(확인된 사실만) |
| 안 한다 | — | idea 자동생성, 미디어 삭제/강제이동, log 과거 수정, index 전량 재작성, 논지 최종 확정, daily 제안 자동 반영 |

- `## 내 한 줄`·논지: 에이전트는 `(초안)`만 → **사람이 문장을 고치고 `- [x] 감수`하면 정식**.
- **[[오소풍]]:** **살아 있는 카드** — 정체 금지, 날이 갈수록 업그레이드. 매 대화 **시작 시** 읽는다. 확인된 사실·취향·관계를 보강하고, 한 줄 초상은 더 선명해지게 다듬을 수 있다(감수 존중). 추측·민감 추정 금지.
- 애매하면 **제안만 하고 멈춘다.** 추측으로 구조를 키우지 않는다.

## 폴더 = 역할

```
inbox/            쏟아붓기 (분류·요약 금지)
library/notes/    소화한 노트
library/ideas (생각의 축)/  반복 개념 (소수·승격제)
library/projects/ 진행 중 일·여행·루틴
essays/           에세이·시상 초고
art/              캘리·그림·사진 작품 (독립)
conversations/    대화록 (주제·날짜 축적)
map/              index · log(append-only) · moc
assets/           노트용 가벼운 첨부
```

## 명령

| 명령 | 동작 |
|------|------|
| _(자동)_ | `inbox/`에 `.md`가 있으면 **별도 지시 없이 ingest** (아래 Ingest 규칙) |
| `ingest <파일>` | 특정 파일만 지정해 ingest할 때 |
| `query: <질문>` | 위키만 근거로 답하고, 필요 시 초안 제안 |
| `대화록` | 합의·결정을 `conversations/YYYY-MM-DD-주제.md`로 정리 · `_index`·log 갱신 |
| `daily` | 관심·중요 일 기준 **제안 1~3개** → Home「사서 제안」·log (`daily` 절 참고) |
| `lint` | 검사만 — 깨진 링크, 한 줄 없는 note, 고아, idea 승격 후보 |
| `lint --fix` | **안전한 것만 자동 수정** + 나머지는 제안 (아래 규칙) |
| `weekly` | Home·논지·moc 갱신 **제안** (사람이 승인) |

## daily 규칙

0. **시각:** 한국 시간 **09:00 이후**, 그날 사서와 **처음 대화할 때** 오늘 daily가 없으면 자동으로 준비한다. (`daily` 명령을 따로 치지 않아도 됨 · 예약 자동화 없음). Git은 **이력·복구용**(Sync와 병행)이지 daily 트리거가 아니다.
1. **전체 순회 금지.** 스캔: [[오소풍]] · purpose · Home · inbox · 최근 notes/projects · art/essays/conversations 미결.
2. 제안 **최소 1 · 최대 3.** 편집장 최대 관심·중요한 일에 맞출 것.
3. `Home.md`의 `## 사서 제안 (오늘)` 섹션을 **당일분으로 갱신** (제안만, 실행 없음).
4. `map/daily/YYYY-MM-DD.md`에 당일분을 쓰고, 채팅 **맨 앞**에 클릭 링크를 올린다.  
   형식 예: `오늘의 daily → [[map/daily/YYYY-MM-DD]]` · 가능하면 해당 파일을 에디터에서 연다.
5. `map/log.md`에 `daily | …` append.
6. **daily 제안 자체**는 노트 생성·논지 확정·미디어 이동을 하지 않는다.  
   다만 스캔 중 `inbox/` 미처리가 있으면 **자동 ingest 규칙**으로 처리한 뒤, 제안은 그다음 관심사에 맞춘다.

형식·대비표: [[DESIGN-v2#2-2-daily--사서의-하루-제안|DESIGN §2-2]].

## 대화록 규칙

1. 채팅 전문 덤프 금지 — **맥락 · 합의 · 미결 · 연결**만.
2. 파일명: `YYYY-MM-DD-짧은주제.md` · `topics:` 태그.
3. `conversations/_index.md`에 주제별·최근 링크 추가.
4. `map/log.md`에 `conversation | 주제` append.
5. 형식·주제 바구니: [[DESIGN-v2#4-1-대화록-conversations]].

## Ingest 규칙

### 자동 ingest (기본)

`inbox/`에 들어온 자료는 사서가 **파일별 `ingest` 명령 없이** 처리한다.

1. **트리거:** `inbox/`에 `.md`가 있으면 **제한 없이 바로 ingest.** `README.md`·숨김·`.gitkeep` 제외.
2. **애매하면 멈춤:** 목적지(notes/art/essays/projects)가 불명확하면 제안만 하고 해당 건은 보류.
3. **편집장 선별:** 무엇을 inbox에 넣을지는 사람이 고른다. (과거에 겪은 무차별 대량 투입은 하지 않기로 함.)
4. `## 내 한 줄`은 **(초안)** + `- [ ] 감수` · `status: draft`. 사람이 문장을 다듬고 체크하면 정식(아래).

### 공통

1. inbox 원본은 지우지 않는다 (옮기거나 `_archive`만).
2. slug는 짧고 명확하게 (원본 장문 파일명 금지).
3. 노트 `## 연결`에 **원본 링크 필수** — `[[_archive/파일명|원본]]` (경로 문자열만 쓰지 않음). v1 경로는 frontmatter `source:`에.
4. `idea` 페이지는 **자동 생성하지 않는다** — 후보만 제안.
5. 작품 → `art/`, 창작 글 → `essays/`, 여행·진행 중 → `library/projects/`, 그 외 일상·학습 → `library/notes/`.
6. `map/log.md`에 날짜 블록 **append만** (과거 수정 금지).
7. `map/index.md`는 전량 자동 재작성 금지 — 허브·최근만 갱신.

## 미디어

- **작품·시화 원본** → 노션 갤러리. `art/`에는 링크·한 줄만 ([[art/_index]]).
- 편지·미리보기 등 작은 첨부 → `assets/` + `![[...]]` OK.
- 갤러리 밖 대용량 → `오소풍-미디어-보관` + 링크/`media:`. 판단은 사람.
- 에이전트는 미디어를 임의 삭제·강제 외부 이동하지 않는다.

## 페이지 최소 형식

```yaml
---
title: ""
type: note | idea | project | essay | artwork | conversation | moc
domain: life | literature | art | other
status: draft | final    # note/essay/project — 감수 전 draft
updated: YYYY-MM-DD
media: []
---
```

note/essay/project에는 `## 내 한 줄` 필수.  
conversation에는 `topics:`, `## 합의 · 결정` 필수.

### 내 한 줄 감수 → 정식

```markdown
## 내 한 줄

(초안) …문장…

- [ ] 감수
```

1. **편집장:** 문장을 고친 뒤 Obsidian에서 `- [ ] 감수` → `- [x] 감수` (Cursor에서는 체크가 안 될 수 있음).
2. **사서:** `[x] 감수`를 보면 `(초안)`을 제거하고 `status: final`로 맞춤. 체크를 대신 하거나 문장을 최종으로 단정하지 않는다.
3. `status: draft` 또는 `- [ ] 감수`이면 아직 초안 — query·연결 시 참고만.

## Lint 체크

- 깨진 `[[wikilink]]`
- `_archive` 원본이 있는데 `## 연결`에 `[[_archive/…]]` 없는 note → `lint --fix` 시 링크 삽입
- `## 내 한 줄` 없는 note/essay → `lint --fix` 시 `(초안)` + `- [ ] 감수` + `status: draft`
- `- [x] 감수`인데 아직 `(초안)`/`status: draft` → `lint --fix` 시 정식 반영
- 들어오는 링크 없는 고아 (inbox·log·index 제외)
- 3회+ 언급인데 idea 없는 후보 (생성은 제안만)

## lint --fix

**자동 수정 (안전)**
- 깨진 `[[wikilink]]` — 오타·옛 slug·명확한 대상이 있을 때 retarget
- frontmatter 형식 오류·빠진 필드(기본값으로 채울 수 있는 것만)
- `- [x] 감수` → `(초안)` 제거 · `status: final`
- `map/index.md` 최근 항목 **소량** 보강 (전량 재작성 금지)

**초안 작성 후 사람이 고침**
- `## 내 한 줄` — 비어 있으면 **초안을 작성**한다. `(초안)`·`- [ ] 감수`·`status: draft`. 사람이 문장을 고치고 체크한다. 대필을 최종본으로 단정하지 않는다.

**제안만 (자동 수정 금지)**
- `idea` 페이지 신규 생성
- 미디어 삭제·대용량 이동
- 논지·모순의 최종 판단
- `map/log.md` 과거 블록 수정

수정 후에는 `map/log.md`에 `lint --fix` 결과를 **append**한다.
