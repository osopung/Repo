# Log

append-only. 과거 블록은 수정하지 않는다.

## [2026-08-01] setup | 오소풍_wiki v2 골격

- 폴더 생성: inbox, library, essays, art, map, assets, _archive
- 초안: AGENTS · purpose · Home · art/_index · map/index
- DESIGN-v2 기준. 사람이 문장·이관 목록 보완 예정

## [2026-08-01] design | DESIGN-v2 완성본

- 최우선 C(기록·일상) · art/ 독립 · 미디어 필요첨부 허용
- 성공 기준·구축 체크리스트·v1 cherry-pick 원칙 확정
- 문서: `DESIGN-v2.md` = 설계 원본

## [2026-08-01] conversation | wiki-design-v2

- `conversations/` 폴더·규칙 추가 (주제·날짜 축적)
- 첫 대화록: `conversations/2026-08-01-wiki-design-v2.md`
- AGENTS에 `대화록` 명령 추가

## [2026-08-01] design | 사람 vs 에이전트 역할 분담

- DESIGN §2-1 · AGENTS 상단 · Home에 편집장/사서 분담 명시
- 사람: 수집·최종문장·미디어·Sync·승인 / 에이전트: ingest·초안·lint·대화록

## [2026-08-01] design | daily 사서 제안

- DESIGN §2-2 · AGENTS `daily` 명령 — 스캔 한정, 제안 1~3, Home「사서 제안」만 갱신
- `map/daily/` 선택 보관 · 자동 반영 금지

## [2026-08-01] setup | 시스템 구축

- `.obsidian` 최소 설정 · `templates/` 4종 · `SETUP.md`
- Cursor root → `~/오소풍_wiki`
- 다음: 사람이 Obsidian Sync 연결 후 첫 ingest/daily ([[SETUP]])

## [2026-08-01] cleanup | Sync 혼입 옛 구조 제거

- 삭제: `wiki/`, `raw/`, `schema/`, `gemini-scribe/`, `scripts/`
- 삭제: `LLM WIKI.md`, `wiki.md`, `환영합니다!.md`
- v1 원본은 Drive `오소풍의 모든것`에 유지

## [2026-08-01] ingest | 새집-구축-완료

- `library/notes/새집-구축-완료.md` — 볼트 첫 노트
- 편집장 문장: 「드디어 나의 새 집을 지었다…」

## [2026-08-01] daily | purpose 다듬은 날 — 기록 입구·미결·cherry-pick

- Home「사서 제안」갱신 · `map/daily/2026-08-01.md` 보관
- 제안: inbox에 오늘 한 줄 · 대화록 purpose 미결 체크 · CHERRY-PICK 1개 고르기
- 자동 반영 없음

## [2026-08-01] cherry-pick | v1 → inbox (5건)

- A2 Wispr → `inbox/wispr-flow.md`
- A3 기록강의 → `inbox/recording-course.md`
- A4 행신회동 → `inbox/haengsin-meeting-2026-07-28.md`
- B1 캘리 → `inbox/calligraphy-lessons.md` (미디어 복제 없음)
- C1 태국84일 → `inbox/thailand-84-days.md`
- ingest는 편집장 지시 대기

## [2026-08-01] ingest | from-v1 행신회동-2026-07-28

- `library/notes/행신회동-2026-07-28.md`
- 출처: `오소풍의 모든것/.../행신복지관 회동의 핵심 내용.md` (+ inbox A4)
- inbox → `_archive/haengsin-meeting-2026-07-28.md`
- `## 내 한 줄` (초안) — 편집장 수정 대기

## [2026-08-01] design | inbox 자동 ingest

- 합의: inbox 투입분 → 사서 자동 ingest (파일별 명령 불필요)
- 상한 턴당 5 · 애매하면 보류 · 무차별·대량·v1 전량은 금지 유지
- AGENTS · DESIGN-v2 §2-1·§7 · inbox/README 갱신

## [2026-08-01] ingest | inbox 일괄 5건 (자동)

- [[library/notes/일기-2026-08-01]] ← `8월 1일 금요일.Diary.md`
- [[library/notes/wispr-flow]] · [[library/notes/기록강의-1-3]] · [[library/notes/캘리수업-1-2]]
- [[library/projects/thailand-84-days]] (전문은 `_archive/`, 노트는 구간 요약)
- inbox 원본 → `_archive/` · `## 내 한 줄` (초안) — 편집장 수정 대기

## [2026-08-02] design | inbox 자동 ingest — 건수 상한 제거

- 합의: inbox 투입분 → 제한 없이 바로 ingest (턴당 5 폐기)
- 선별은 편집장이 inbox에 넣을 때 · 애매한 목적지 보류는 유지
- AGENTS · DESIGN-v2 · inbox/README · 대화록 갱신

## [2026-08-02] design | 내 한 줄 감수 → 정식

- 규칙: `- [ ] 감수` + `status: draft` → 편집장 체크 후 사서가 `status: final`·`(초안)` 제거
- 템플릿 note/essay/artwork · AGENTS · DESIGN 반영
- 기존 노트에 체크박스 부착 (새집만 final)

## [2026-08-02] design | 노트 원본 위키링크 필수

- ingest 시 `## 연결`에 `[[_archive/…|원본]]` 삽입 (경로 문자열만 금지)
- 기존 from-v1·일기 노트 링크 보강 · AGENTS · DESIGN · 템플릿

## [2026-08-02] ingest | 하림에게-그림편지

- `library/notes/하림에게-그림편지.md`
- 사진 3장: `assets/IMG_5085.jpeg` · `IMG_5086.jpeg` · `IMG_5130.jpeg` (Obsidian 첨부 폴더)
- inbox → `_archive/하림에게_아빠의 그림편지.md`
- `## 내 한 줄` (초안) — 감수 대기

## [2026-08-02] design | 노션 시화 갤러리 연동

- 허브: [[art/_index]] ← 오소풍의 갤러리/시화 갤러리
- URL: https://app.notion.com/p/osopung58/53279f80606d4f878ae6f9107c53d6c7
- 역할: 원본=노션 · 위키 art/=링크·한 줄 · Drive 보관함=갤러리 밖 대용량
- DESIGN §6 · AGENTS · Home 갱신

## [2026-08-02] design | daily = B (첫 대화 시)

- git·클라우드 예약 자동화 안 씀
- 규칙: 매일 09:00 이후 사서와 처음 대화할 때 당일 daily 자동 준비
- AGENTS · DESIGN §2-2 · Home · 대화록 갱신

## [2026-08-02] ingest | 일기-2026-08-02 · 먼저-행동하라-캘리

- [[library/notes/일기-2026-08-02]] · [[library/notes/먼저-행동하라-캘리]]
- inbox → `_archive/` · 감수 대기

## [2026-08-02] daily | 깊은 잠·STT·캘리·감수

- Home「사서 제안」갱신 · `map/daily/2026-08-02.md` 보관
- 제안: 한 줄 감수 1건 · 노션 갤러리 · draft 1개만 정식

## [2026-08-02] lint | 감수→정식 반영

- final: wispr-flow · 기록강의-1-3 · 행신회동 · 일기-2026-08-01 · 캘리수업-1-2 · 하림에게-그림편지
- 아직 draft: 일기-2026-08-02 · 먼저-행동하라-캘리 · thailand-84-days
- daily/Home 제안 문구 갱신 (옛 draft 안내 삭제)

## [2026-08-02] move | 하림에게-그림편지 → art/drawing

- `library/notes/` → [[art/drawing/하림에게-그림편지]] (type: artwork)
- 사진 IMG_5085·5086·5130은 `assets/` 그대로

## [2026-08-02] cleanup | .gitkeep · .DS_Store 제거

- git 자리표시·시스템 찌꺼기 삭제 (폴더 골격은 유지)

## [2026-08-02] idea | 3건 승격 (편집장 승인)

- [[library/ideas (생각의 축)/기록하는-인간]] · [[library/ideas (생각의 축)/입구로서의-inbox]] · [[library/ideas (생각의 축)/몸과-말]]
- `## 내 한 줄` (초안) — 감수 대기
- index · Home · purpose · 관련 note 연결 보강

## [2026-08-02] rename | ideas → ideas (생각의 축)

- 폴더명 변경 · 위키링크·AGENTS·DESIGN 경로 갱신

## [2026-08-02] conversation | record-moc-star5 ★5

- 대화록: `conversations/2026-08-02-record-moc-star5.md` (star: 5)
- MOC: [[map/moc/record|기록]]
- chats 탭명: ★5 기록·ideas·MOC

## [2026-08-02] essay | 말이-기록이-되다 (초안)

- `essays/말이-기록이-되다.md` — Wispr·기록강의·행신·새집·ideas 한 줄 직조
- `## 내 한 줄` (초안) — 편집장 감수 대기

## [2026-08-02] essay | 말이-기록이-되다 → final

- 편집장 다듬음 · `- [x] 감수` → `status: final`
- 내 한 줄: 말이 기록이 되고, 문장이 되고, 캘리가 된다…

## [2026-08-02] ingest | 슬기로운-은퇴생활 (원고)

- [[library/projects/슬기로운-은퇴생활]] — 책 원고 허브
- 본문: `assets/『슬기로운 은퇴생활』.md` (복제 없음)
- inbox → `_archive/슬기로운 은퇴생활_나의 책.md`

## [2026-08-03] design | 오소풍.md 사서 메모리 카드

- 신설: `오소풍.md` — 매 대화 전 필독 · 확인 사실만 append
- AGENTS · DESIGN daily 스캔 · Home · index 연결

## [2026-08-03] design | 오소풍.md = 살아 있는 카드

- 합의: 정체 금지 · 날이 갈수록 업그레이드
- AGENTS · 오소풍.md 업그레이드 규칙 명시 · 한 줄 초상 final

## [2026-08-03] design | Git Repo 재도입 (이력·복구)

- `git init -b main` · `.gitignore` (workspace · 대용량 원고 제외)
- Sync와 병행 · daily 예약 자동화와 무관
- 첫 커밋 · 원격: **https://github.com/osopung/Repo** (private)
