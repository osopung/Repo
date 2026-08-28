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

## [2026-08-03] daily | 초안 감수 · weekly · (선택) 오늘 기록

- Home「사서 제안」갱신 · `map/daily/2026-08-03.md`

## [2026-08-03] weekly | W32 제안 (승인 대기)

- `map/weekly/2026-W32.md` — purpose·Home·moc·index 제안만 (미반영)

## [2026-08-03] design | daily·weekly 채팅 링크 필수

- 합의: 채팅은 Cursor용 `[…](map/….md)` · 볼트 안은 `[[wikilink]]`
- `[[…]]`만 올리면 채팅에서 링크가 안 열림 → 형식 수정
- AGENTS · DESIGN · [[오소풍]] 반영

## [2026-08-03] weekly | W32 A-1 반영

- purpose 논지 4: Sync는 기기 · Git은 이력

## [2026-08-03] weekly | W32 A-2 반영

- purpose 논지 5: 사서가 daily로 기록·창작 · 편집장 감수 하에

## [2026-08-03] weekly | W32 A-3 반영

- purpose 헤더: `현재 논지 (편집장 감수 · weekly 손질)`

## [2026-08-03] weekly | W32 B·D 반영

- Home: 오늘/이번 주 · 이번 달 초점
- index: [[오소풍]] · ★5 대화록을 최근에

## [2026-08-03] weekly | W32 C 반영

- [[map/moc/record|기록]] moc — 에세이 final · 책 원고 · updated
- W32 A~D **전부 반영 완료**

## [2026-08-03] media | 슬기로운-은퇴생활 본문 → 미디어 보관

- `assets/『슬기로운 은퇴생활』.md` → `오소풍-미디어-보관/manuscripts/`
- 허브 [[library/projects/슬기로운-은퇴생활]] embed 제거 · 경로·`media:` 갱신

## [2026-08-03] note | 옵시디언-지식-꺼내쓰기-구요한 (초안)

- [[library/notes/옵시디언-지식-꺼내쓰기-구요한]] — youtu.be/k2FQEZx8g4E 요약
- 오소풍 대응 · Share 여지 · 내 한 줄 감수 대기

## [2026-08-03] ops | Smart Composer 플러그인 설치

- `.obsidian/plugins/obsidian-smart-composer` v1.2.9
- `community-plugins.json`에 `smart-composer` 활성화
- API/구독 연결은 편집장이 Obsidian 설정에서

## [2026-08-03] ops | Smart Composer · Google 연동 성공

- 편집장 확인: Gemini(Google) 연결 완료

## [2026-08-03] ops | Smart Composer · Gemini 모델 사용 성공

- 기본 모델이 Anthropic로 남아 키 오류 → Gemini로 전환 후 정상

## [2026-08-03] note | 임베딩-embedding (초안)

- [[library/notes/임베딩-embedding]] — 공부 첨부 정리 · `assets/IMG_8839-embedding.png`

## [2026-08-03] viz | Mermaid — 루프 · CMDS

- [[map/moc/record|기록 MOC]] 메인 루프
- [[library/notes/옵시디언-지식-꺼내쓰기-구요한]] CMDS 단계

## [2026-08-03] note | Smart Composer 시스템 프롬프트 (초안)

- [[library/notes/Smart-Composer-시스템-프롬프트]] — 설정에 붙여넣을 고정문

## [2026-08-03] ops | Smart Composer 시스템 프롬프트 보류

- 편집장: 자유도 과제한 느낌 → 설정 미적용 · 노트만 보관

## [2026-08-03] note | ★5 질문 — AI가 되묻게

- [[library/notes/질문-AI가-되묻게]] · keywords: 질문 · star 5
- 대화록: [[conversations/2026-08-03-question-star5]]

## [2026-08-03] design | 질문·반대 규칙 정식화

- AGENTS · [[오소풍]]: 질문 우선 · 사실·위험 시 분명한 반대 · 아첨·맹목 복종 금지

## [2026-08-03] note | ★5 탐침 복붙 3종

- [[library/notes/탐침-복붙-3종]] — 채팅용 한 줄 3개 · keywords: 질문·탐침

## [2026-08-04] ingest | inbox 일괄 5건 (자동)

- [[library/notes/일기-2026-08-04]] ← `8월 4일 화요일 다이어리.md` — 안중근 「일일무독서」· AI와 독서 다짐
- [[library/notes/일기-2026-08-03-전철]] ← `Ttimes.md` + `8월 3일, 1기.md` (중복 원본 2건)
- [[library/notes/Smart-Composer-사용법]] ← `Smart Composer 사용법.md` + `System Prompt.md`
- [[library/notes/AI-독서-파트너-활용법]] ← `AI와 함께하는 독서 파트너 활용법.md` — Gemini 링크, 로그인 요구로 **요약 불가** (편집장 확인 필요)
- inbox 원본 6건 → `_archive/` · `## 내 한 줄` (초안) — 편집장 감수 대기
- 보류: `inbox/쥬디 할머니.md` — **빈 파일**이라 ingest 안 함 (편집장에게 질문)

## [2026-08-04] essay | 두 개의 울타리 (초안)

- [[essays/두 개의 울타리]] — 쥬디 할머니 함께읽기 → 둔내 소풍헌 1년·소로우 모델과 연결
- [[library/notes/쥬디-할머니-박완서]] — 책 정보·함께 읽은 기록 (원문 전재는 안 함, 저작물)
- `## 내 한 줄` (초안) — 편집장 감수 대기

## [2026-08-04] note | 오소풍 타임라인 — 둔내 홀로 1년 · 소로우 모델

- 편집장 확인: 은퇴 후 둔내 소풍헌 통나무집에서 홀로 1년, 「나는 작가다」 역할 자임, 월든·소로우가 모델
- [[library/projects/슬기로운-은퇴생활|슬기로운 은퇴생활]] 3부(열매 — 홀로서기와 새로운 시작, 10~14장)와 직결 가능성
- [[오소풍]] 타임라인 반영

## [2026-08-04] conversation | 쥬디-할머니-함께읽기 방식 합의

- 편집장 선택: **장면 단위**로 끊어 가져오기 · 이번 회 초점 = **인물(쥬디 할머니)의 태도·심리**
- 사서는 해석·요약 대신 **탐침 질문 2~3개**로 응답 (본문 미보유 확인 · 추측 금지)
- [[오소풍]] 사서 메모 반영

## [2026-08-05] daily | 제안 3

- [[map/daily/2026-08-05]] — 에세이 정식화 · 쥬디 다음 장면 · 일기 감수
- inbox `쥬디 할머니.md` 빈 파일 — ingest 보류 유지

## [2026-08-06] daily | 제안 3

- [[map/daily/2026-08-06]] — 브레인 트리니티 감수 · 숲채원/파크골프 한 줄 · 쥬디 장면

## [2026-08-06] ingest | YouTube 스크립트 · 일기 · 영상 요약

- [[library/notes/브레인-트리니티-LLM-wiki-RAG]] ← `브레인-트리니티-LLM-wiki-스크립트.md` + `브레인 트리니티.md` — youtu.be/t4XEda3CB3Q 자막 전문(Web Clipper 대신 사서 저장)
- [[library/notes/솔트룩스-이경일-온톨로지]] ← `솔트룩스 이경일 온톨로지.md`
- [[library/notes/일기-2026-08-05-파크골프]] ← `8월 5일 수요일 다이어리, 파크골프.md` (`IMG_5433` assets 없음)
- [[library/notes/일기-2026-08-06-숲채원-정상]] ← `습채원정상.md`
- [[AI-뉴스레터-구독-무엇을?]] ← `전문 AI 뉴스레터 구독하기.md`
- inbox 원본 → `_archive/` · `## 내 한 줄` (초안) — 편집장 감수 대기

## [2026-08-06] note | 브레인 트리니티 도구 조목

- [[library/notes/브레인-트리니티-LLM-wiki-RAG]]에 「도구 조목 (실제 활용용)」추가 — 의도·실행·현실·수집·회고별 + 오소풍 대응표

## [2026-08-06] note | 브레인 트리니티 형광·대화·인사이트

- [[library/notes/브레인-트리니티-형광-대화-인사이트]] — 스크립트 형광 추출 · 대화 핵심 · 사서 인사이트
- 원 노트 [[library/notes/브레인-트리니티-LLM-wiki-RAG]]에 링크

## [2026-08-06] conversation | AI 로그 세 줄 세이브

- 합의: 긴 Cursor 세션 끝 **한 일 / 미결 / 다음** → conversations 또는 daily ([[AGENTS#AI-로그-세-줄-세이브]])
- [[conversations/2026-08-06-brain-trinity-ai-log]] · DESIGN §4-1 · [[오소풍]] 반영

## [2026-08-06] ops | 유튜브 공부 루프

- 합의: 옵시디언 유튜브는 자막만 쌓지 않고 **오늘 Brain Trinity처럼 공부**
- [[AGENTS#유튜브-공부-루프]] · [[오소풍]] · 기준 세션 [[conversations/2026-08-06-brain-trinity-ai-log]]

## [2026-08-06] ops | 유튜브 — 요약 우선

- 보완: 유튜브 공부 = **영상 요약 먼저** · 스크립트/자막 전문은 **별도 요청 시에만**
- [[AGENTS#유튜브-공부-루프]] · [[오소풍]]

## [2026-08-06] design | inbox ingest = 사서 접속 시점

- 합의: inbox는 파일 유입 즉시가 아니라 **편집장이 사서에게 접속(대화 시작)한 때** 소화
- [[AGENTS]] · [[DESIGN-v2]] · [[Home]] · inbox/README · [[오소풍]] 반영

## [2026-08-06] design | 개념 쪼개기 — 사서 제안만

- 합의: 엔티티/개념 다장 전개는 **필요할 듯할 때 사서 제안** · 자동 생성 금지 ([[AGENTS]] ingest 공통)

## [2026-08-06] conversation | 온톨로지와 오소풍_wiki 마무리

- [[library/notes/솔트룩스-이경일-온톨로지]] 형광·토론 핵심·인사이트
- 합의: 기업/지식그래프 온톨로지 구축 안 함 · 문서 질서([[오소풍]]·purpose·ideas)로 충분
- [[conversations/2026-08-06-ontology-wiki]]

## [2026-08-07] daily | 헤르메스·아이폰

- [[map/daily/2026-08-07]] — 오늘 초점: Hermes → Telegram → iPhone
- inbox 유튜브 3 → notes (요약 stub) · [[library/notes/헤르메스-아이폰-설치]]

## [2026-08-07] youtube | Hermes VPS 후보 3편 요약

- 1 [[헤르메스 역대급 업데이트 4가지 ;Jay-Choi-의견수락-내시스템-도입]] · 2 [[헤르메스로 언제 어디서든 AI 비서 -코드깎는노인-유튜브]] · 3 [[헤르메스 — 노트북 꺼도 24시간 AI 팀-실밸개발자-유튜브]]
- 공통: Hostinger(클라우드) · KVM2 · 메인 PC 비권장 · 아이폰은 텔레그램

## [2026-08-07] decision | Hermes 2번 경로

- 확정: Hostinger KVM2 **원클릭** + **Nexus AI** + **Telegram** → 아이폰
- [[library/notes/헤르메스-아이폰-설치]] 체크리스트 1~8

## [2026-08-07] ops | Hostinger 결제 완료

- 편집장: Apple Pay · **2년** · 약 **$200** · KVM2
- 다음: hPanel **Hermes Deploy** → Nexus → Telegram
- [[library/notes/헤르메스-아이폰-설치]]

## [2026-08-07] ops | Hermes 배포 실행

- 편집장: 설정 폼에서 **「배포」** 클릭
- 다음: 설치 완료 → Nexus 키 확인 → Telegram

## [2026-08-07] ops | Hermes Telegram connected

- Keys에 bot token · allowed user 설정 · Gateway restart
- 상태: gateway **running** · telegram **connected**
- 다음: 아이폰에서 봇 시험 메시지

## [2026-08-08] ops | Hermes inbox Git 연결 (A안)

- VPS clone: `/opt/data/osopung-wiki` · MCP inbox_fs · PAT(자격증명 store)
- 다음: 텔레그램에서 inbox 쓰기 시험 · 맥 pull · (권장) PAT Revoke/재발급
- [[library/notes/헤르메스-아이폰-설치]]

## [2026-08-09] note | 헤르메스 핵심 · 지침 업그레이드

- Drive Docs 2건 → [[헤르메스-에이전트-핵심정리-어디에쓰나-커스-역할분담]] (A4 요약)
- 지침: [[헤르메스에게_8.17.수정]] · [[library/notes/헤르메스-아이폰-설치]] (역할 분담·Drive OAuth 금지·inbox A안)
- 사서: Gmail·Drive·Calendar 플러그인 연결 · Luna·Nexos 충전 반영

## [2026-08-09] decision | Hermes push → 사서 pull·보고

- 헤르메스 push 성공 알림 → 사서가 맥 `git pull` → 파일·커밋을 편집장에게 보고 → ingest
- 편집장은 직접 pull 하지 않음 · [[AGENTS#Hermes--Git--사서]]

## [2026-08-05] daily | 제안 3

- [[map/daily/2026-08-05]] — 에세이 정식화 · 쥬디 다음 장면 · 일기 감수
- inbox `쥬디 할머니.md` 빈 파일 — ingest 보류 유지

## [2026-08-06] daily | 제안 3

- [[map/daily/2026-08-06]] — 브레인 트리니티 감수 · 숲채원/파크골프 한 줄 · 쥬디 장면

## [2026-08-06] ingest | YouTube 스크립트 · 일기 · 영상 요약

- [[library/notes/브레인-트리니티-LLM-wiki-RAG]] ← `브레인-트리니티-LLM-wiki-스크립트.md` + `브레인 트리니티.md` — youtu.be/t4XEda3CB3Q 자막 전문(Web Clipper 대신 사서 저장)
- [[library/notes/솔트룩스-이경일-온톨로지]] ← `솔트룩스 이경일 온톨로지.md`
- [[library/notes/일기-2026-08-05-파크골프]] ← `8월 5일 수요일 다이어리, 파크골프.md` (`IMG_5433` assets 없음)
- [[library/notes/일기-2026-08-06-숲채원-정상]] ← `습채원정상.md`
- [[AI-뉴스레터-구독-무엇을?]] ← `전문 AI 뉴스레터 구독하기.md`
- inbox 원본 → `_archive/` · `## 내 한 줄` (초안) — 편집장 감수 대기

## [2026-08-06] note | 브레인 트리니티 도구 조목

- [[library/notes/브레인-트리니티-LLM-wiki-RAG]]에 「도구 조목 (실제 활용용)」추가 — 의도·실행·현실·수집·회고별 + 오소풍 대응표

## [2026-08-06] note | 브레인 트리니티 형광·대화·인사이트

- [[library/notes/브레인-트리니티-형광-대화-인사이트]] — 스크립트 형광 추출 · 대화 핵심 · 사서 인사이트
- 원 노트 [[library/notes/브레인-트리니티-LLM-wiki-RAG]]에 링크

## [2026-08-06] conversation | AI 로그 세 줄 세이브

- 합의: 긴 Cursor 세션 끝 **한 일 / 미결 / 다음** → conversations 또는 daily ([[AGENTS#AI-로그-세-줄-세이브]])
- [[conversations/2026-08-06-brain-trinity-ai-log]] · DESIGN §4-1 · [[오소풍]] 반영

## [2026-08-06] ops | 유튜브 공부 루프

- 합의: 옵시디언 유튜브는 자막만 쌓지 않고 **오늘 Brain Trinity처럼 공부**
- [[AGENTS#유튜브-공부-루프]] · [[오소풍]] · 기준 세션 [[conversations/2026-08-06-brain-trinity-ai-log]]

## [2026-08-06] ops | 유튜브 — 요약 우선

- 보완: 유튜브 공부 = **영상 요약 먼저** · 스크립트/자막 전문은 **별도 요청 시에만**
- [[AGENTS#유튜브-공부-루프]] · [[오소풍]]

## [2026-08-06] design | inbox ingest = 사서 접속 시점

- 합의: inbox는 파일 유입 즉시가 아니라 **편집장이 사서에게 접속(대화 시작)한 때** 소화
- [[AGENTS]] · [[DESIGN-v2]] · [[Home]] · inbox/README · [[오소풍]] 반영

## [2026-08-06] design | 개념 쪼개기 — 사서 제안만

- 합의: 엔티티/개념 다장 전개는 **필요할 듯할 때 사서 제안** · 자동 생성 금지 ([[AGENTS]] ingest 공통)

## [2026-08-06] conversation | 온톨로지와 오소풍_wiki 마무리

- [[library/notes/솔트룩스-이경일-온톨로지]] 형광·토론 핵심·인사이트
- 합의: 기업/지식그래프 온톨로지 구축 안 함 · 문서 질서([[오소풍]]·purpose·ideas)로 충분
- [[conversations/2026-08-06-ontology-wiki]]

## [2026-08-07] daily | 헤르메스·아이폰

- [[map/daily/2026-08-07]] — 오늘 초점: Hermes → Telegram → iPhone
- inbox 유튜브 3 → notes (요약 stub) · [[library/notes/헤르메스-아이폰-설치]]

## [2026-08-07] youtube | Hermes VPS 후보 3편 요약

- 1 [[헤르메스 역대급 업데이트 4가지 ;Jay-Choi-의견수락-내시스템-도입]] · 2 [[헤르메스로 언제 어디서든 AI 비서 -코드깎는노인-유튜브]] · 3 [[헤르메스 — 노트북 꺼도 24시간 AI 팀-실밸개발자-유튜브]]
- 공통: Hostinger(클라우드) · KVM2 · 메인 PC 비권장 · 아이폰은 텔레그램

## [2026-08-07] decision | Hermes 2번 경로

- 확정: Hostinger KVM2 **원클릭** + **Nexus AI** + **Telegram** → 아이폰
- [[library/notes/헤르메스-아이폰-설치]] 체크리스트 1~8

## [2026-08-07] ops | Hostinger 결제 완료

- 편집장: Apple Pay · **2년** · 약 **$200** · KVM2
- 다음: hPanel **Hermes Deploy** → Nexus → Telegram
- [[library/notes/헤르메스-아이폰-설치]]

## [2026-08-07] ops | Hermes 배포 실행

- 편집장: 설정 폼에서 **「배포」** 클릭
- 다음: 설치 완료 → Nexus 키 확인 → Telegram

## [2026-08-07] ops | Hermes Telegram connected

- Keys에 bot token · allowed user 설정 · Gateway restart
- 상태: gateway **running** · telegram **connected**
- 다음: 아이폰에서 봇 시험 메시지

## [2026-08-08] ops | Hermes inbox Git 연결 (A안)

- VPS clone: `/opt/data/osopung-wiki` · MCP inbox_fs · PAT(자격증명 store)
- 다음: 텔레그램에서 inbox 쓰기 시험 · 맥 pull · (권장) PAT Revoke/재발급
- [[library/notes/헤르메스-아이폰-설치]]

## [2026-08-08] ingest | 헤르메스 inbox 2건 (사서 접속)

- [[library/notes/일기-2026-08-08-헤르메스]] ← `2026-08-08-헤르메스와-하루를-탕진한-날.md`
- [[library/notes/헤르메스-inbox-연동-시험]] ← `hermes-test-2026-08-08.md`
- inbox 원본 → `_archive/` · `## 내 한 줄` (초안) — 편집장 감수 대기
- 확인 사실: 헤르메스 inbox 작성·git push 성공 · (당시) Google Drive 인증 미해결 → 이후 사서가 Drive/Calendar 연결
- [[오소풍]] 도구·사서 메모 보강

## [2026-08-09] note | 헤르메스 핵심 · 지침 업그레이드

- Drive Docs 2건 → [[헤르메스-에이전트-핵심정리-어디에쓰나-커스-역할분담]] (A4 요약)
- 지침: [[헤르메스에게_8.17.수정]] · [[library/notes/헤르메스-아이폰-설치]] (역할 분담·Drive OAuth 금지·inbox A안)
- 사서: Gmail·Drive·Calendar 플러그인 연결 · Luna·Nexos 충전 반영

## [2026-08-09] decision | Hermes push → 사서 pull·보고

- 헤르메스 push 성공 알림 → 사서가 맥 `git pull` → 파일·커밋을 편집장에게 보고 → ingest
- 편집장은 직접 pull 하지 않음 · [[AGENTS#Hermes--Git--사서]]

## [2026-08-09] ops | 사서 git pull 보고

- HEAD `8bcfec3` · 신규 inbox: `2026-08-09-주일설교-골로새서-3장-15-17절.md` (감사·골로새서)
- 원격에 이미 노트화된 일기·연동 시험도 수신

## [2026-08-09] ingest | 주일설교 — 범사에 감사

- [[library/notes/주일설교-2026-08-09-범사에-감사]] ← inbox `감사의 파도,2026-08-09-주일설교-…`
- 원본 → [[_archive/2026-08-09-주일설교-골로새서-3장-15-17절|원본]] · `## 내 한 줄` 감수 대기
- inbox 잔여: 유튜브 링크 stub 3건 · `헤르메스에게.md`(지침) — 보류

## [2026-08-10] ops | 감수 전 노트 붉은 표시

- CSS 스니펫 `.obsidian/snippets/unreviewed-red.css` 활성
- `- [ ] 감수` 노트 25건에 `cssclasses: [draft]` · 템플릿·[[AGENTS]] 반영

## [2026-08-10] decision | 감수→정식은 사서 자동

- 편집장은 「정식 반영」 요청 안 함 · 접속·daily·lint 때 사서가 `[x] 감수` 훑어 정식화
- [[AGENTS]] 반영

## [2026-08-10] ops | 사서 git pull 보고

- HEAD `b183f4d`
- 신규 inbox: `2026-08-09-주일일기-예배와-가족의-저녁.md` · `2026-08-10-오늘의-계획-캘리그래피와-Zotero-연동.md`
- ingest는 편집장 지시 대기

## [2026-08-10] ops | 파일 탐색기 미감수 표시

- `.obsidian/snippets/unreviewed-explorer.css` — `data-path`로 빨간 글씨+밑줄 (본문 아님)
- 대상: `- [ ] 감수` + inbox 미소화 · Sync 후 스니펫 ON 필요

## [2026-08-10] ingest | 일기·계획·조테로·유튜브 stub

- [[library/notes/일기-2026-08-09-주일-예배와-가족]] · [[library/notes/계획-2026-08-10-캘리-Zotero]] (`final`·감수됨)
- [[library/notes/조테로-옵시디언-세컨드브레인]] · [[library/notes/조테로-NotebookLM-LLM-wiki]] · 스크립트 → `_archive/`
- [[library/notes/유튜브-스타십-완성-이후]] · [[library/notes/유튜브-일론-인류-5년]] (요약 stub)
- inbox 잔여: `README` · `헤르메스에게` (지침)
- 탐색기 CSS·[[map/감수-대기]] 갱신

## [2026-08-10] note | ★5 오소풍-공유폴더

- ★5 [[library/notes/오소풍-공유폴더]] — Drive 공유 미디어 · `file/d/…/view`
- 폴더: https://drive.google.com/drive/folders/1EzSDfh9tCIalMZmbPcnwZtDCZJb1r9Ve
- AGENTS · DESIGN · Home · [[오소풍]] · `inbox/헤르메스에게` 반영

## [2026-08-10] ingest | 수묵 캘리 수업 3건

- [[library/notes/수묵-캘리-수업-2026-08-10]] (draft · Drive `file/d` 링크)
- [[library/notes/수묵-캘리-표현과-응용-원리]] · [[library/notes/캘리-먹의-건조와-번짐]] (`final` · inbox에서 `[x] 감수`)
- 원본 → `_archive/2026-08-10-…`
- 정식화: [[library/notes/브레인-트리니티-LLM-wiki-RAG]] `final`
- inbox 잔여: `README` · `헤르메스에게`

## [2026-08-10] lint | 감수 정식화 · 빨간 표시 갱신

- 정식화 7건: `library/notes/질문-AI가-되묻게.md`, `library/notes/헤르메스로 언제 어디서든 AI 비서 -코드깎는노인-유튜브.md`, `library/notes/탐침-복붙-3종.md`, `library/notes/수묵-캘리-수업-2026-08-10.md`, `library/notes/주일설교-2026-08-09-범사에-감사.md`, `library/notes/오소풍-공유폴더.md`, `library/notes/AI-뉴스레터-구독-무엇을?.md`
- [[map/감수-대기]] · unreviewed-explorer.css → **23건**

## [2026-08-10] note | ★5 헤르메스 MOA · 5스타 MOC

- ★5 [[library/notes/헤르메스-MOA]] — `/moa` · `/model … --provider moa`
- 검색 허브 [[map/moc/5스타]] — Obsidian에서 `5스타`로 찾기

## [2026-08-10] moc | 약어 용어집

- [[map/moc/약어]] — `abbr` 호버 + 자주 쓰는 약어 표
- Home · index · [[오소풍]] · [[map/moc/5스타]] 연결

## [2026-08-10] ops | Abbreviations and Acronyms 플러그인

- 설치: `.obsidian/plugins/abbreviations-mark` (v1.7.5)
- 활성화: `community-plugins.json`
- 전역 약어 + `globalFile`: [[map/moc/약어]]

## [2026-08-10] rule | 약어 자동 추가

- 편집장이 물은 약어 → 사서가 [[map/moc/약어]] · Extra · `abbreviations-mark` 전역에 추가 (AGENTS·오소풍 반영)

## [2026-08-10] note | ★5 Claude 비용 Pro vs API

- [[글쓰기-Claude-비용-Pro-vs-API]] · 검색 `5*` / `5스타`
- [[map/moc/5스타]]에 `5*` 키워드 추가

## [2026-08-10] note | Claude Pro≠API 한 줄 보강 (5*)

- [[library/notes/글쓰기-Claude-비용-Pro-vs-API]] — Pro=웹이용권, API=전기 · final

## [2026-08-10] inbox | Drive 조테로 문서 2건 추출

- `inbox/2026-08-10-조테로-LLM위키-연동-이점.md`
- `inbox/2026-08-10-조테로-연동-Cursor-vs-Claude-Code.md`

## [2026-08-11] ingest | 조테로 inbox 2 + 스크립트 2

- inbox → notes: [[library/notes/조테로-LLM위키-연동-이점]] · [[library/notes/조테로-연동-Cursor-vs-Claude-Code]]
- 허브(설치·사용): [[library/notes/조테로-옵시디언-설치-사용법]]
- 요약 갱신: [[library/notes/조테로-옵시디언-세컨드브레인]] · [[library/notes/조테로-NotebookLM-LLM-wiki]]
- 원본: [[_archive/조테로-LLM위키-연동-이점]] · [[_archive/조테로-연동-Cursor-vs-Claude-Code]] · [[_archive/조테로스크립트-옵시디언-연동-설치-사용법-세컨드브레인]] · [[_archive/조테로-NotebookLM-LLM-wiki-스크립트]]
- 감수-대기·unreviewed-explorer 재생성

## [2026-08-12] project | 일인소송 폴더

- [[library/projects/일인소송/_index]] — 왕길역 112-2301 해제·최고 · 1인소송 준비
- [[library/projects/일인소송/대화록]] · [[library/projects/일인소송/중요쟁점]] (이행착수·위약금·최고 회신 등)
- 반박 내용증명 초안 PDF/md · [[conversations/2026-08-12-일인소송-왕길역]]

## [2026-08-12] evidence | 배달증명 → 일인소송

- [[library/projects/일인소송/배달증명]] (등기 3112945006950 · 배달 2026-06-25 · 2쪽)
- inbox/2026-08-12 링크 갱신 · assets/1인소송.pdf 제거

## [2026-08-12] project | 내용증명 송달 주소 파일링

- [[library/projects/일인소송/송달주소]] — 디케이퍼스트(이성헌·강남대로 358) · 하나자산신탁(민관식·테헤란로 127)
- 반박초안·_index 링크 갱신

## [2026-08-12] archive | 일인소송 대화록 raw

- `library/projects/일인소송/대화록_raw_2026-08-12-왕길역.jsonl` — Cursor agent transcript `4c990def-6390-4bca-b0c6-bc5189449b1a` 원본 복사

## [2026-08-15] ingest | 일인소송 inbox 3

- [[library/projects/일인소송/위약금-3단논리]] · [[library/notes/대법원-잔금기일-해제권]] · [[library/projects/일인소송/디케이퍼스트-4가지-질문]] (스텁)
- 원본 → `_archive/위약금 소송` · `_archive/DaebeobweonJaepanJuyopangyeol` · `_archive/Dikeipeoseuteuege4gajiJilmun`
- inbox 잔여: `README` · `헤르메스에게`

## [2026-08-15] lint | 감수 정식화 18건

- `[x] 감수`인데 `status: draft`이던 노트 18건 → `final`
- [[map/감수-대기]] · unreviewed-explorer.css 재생성

## [2026-08-15] daily | 에이전트 시너지 · 일인소송 8/31

- [[map/daily/2026-08-15]]
- Codex AI-HQ 제안 검토 — 위키를 유일한 HQ로 유지하는 쪽을 권함

## [2026-08-15] note | 코덱스에게 지침

- [[inbox/코덱스에게]] — 집·구조·`osopung/Repo` 먼저, 그다음 역할. 주인→에이전트 말투
- [[library/notes/코덱스-역할]] (draft)

## [2026-08-15] note | 윈도우 Cursor에게

- [[inbox/윈도우-Cursor에게]] — 같은 사서, 다른 책상. 맥과 동시 금지
- [[library/notes/윈도우-Cursor]] (draft)

## [2026-08-15] project | 이의통지 8/14 발송 반영

- [[library/projects/일인소송/_index]] 「다음」·요약 갱신
- [[library/projects/일인소송/중요쟁점]] §3 실행 한 줄

## [2026-08-15] rule | 사건마스터 inbox → 교체

- 편집장이 새 사건마스터를 inbox에 넣음 → 사서 접속 시 `사건마스터.md` **교체** (직전 본문 `_archive`)
- 제2판 허브 금지 · `_index` 「다음」 맞춤 · AGENTS ingest 7

## [2026-08-15] pull | Hermes inbox 5

- `dbf0e33` inbox: record connected journey to wedding
- ingest: [[library/notes/일기-2026-08-10-기록의-길]] · [[library/notes/일기-2026-08-15-예식장]] · [[library/notes/ChatGPT-대화를-Zotero로]] · [[library/notes/헤르메스-지시-워크플로우]] · [[library/notes/원본은-Zotero-액기스는-위키]]
- inbox 잔여: `README` · `헤르메스에게` · `코덱스에게` · `윈도우-Cursor에게`

## [2026-08-15] rule | 윈도우 Cursor = 헤르메스 레인

- 사서 = 맥 Cursor 하나. 윈도우 Cursor는 `inbox/`만 (ingest·daily 금지)
- [[inbox/윈도우-Cursor에게]] 전면 개정

## [2026-08-15] ops | 코덱스 Git·inbox에서 자름

- 윈도우 가지 `cursor/windows-cursor-ingest-7958`에서 확인 후 `main` 지침에 반영
- 코덱스는 Repo를 열지 않음. 산출물은 편집장이 사서에게 전함

## [2026-08-15] rule | 윈도우 Cursor 호칭 = 고문

- 지침 [[inbox/고문에게]] · 노트 [[library/notes/고문]]
- 옛 `윈도우-Cursor에게` 폐지. 사서는 맥, 고문은 inbox만

## [2026-08-15] rule | 위키↔Repo 시차

- 맞추는 때 셋: 사서 접속 pull · 헤르메스·고문 inbox 즉시 push · 세션 끝/`맞춰` commit·push
- 하루를 넘겨 로컬에만 쌓지 말 것

## [2026-08-15] rule | 고문 = 조언·조력 (헤르메스와 다름)

- 고문은 나에게 조언하며 나를 돕는 자. 헤르메스(수집·inbox)와 같은 레인이 아님
- 집에 넣을 글이 있을 때만 `inbox/`
- 지침 [[inbox/고문에게]] · [[library/notes/고문]]

## [2026-08-15] pull | Hermes 기록 테스트

- `a781ed0` inbox: add Hermes record test
- 수신: `inbox/헤르메스-기록-테스트.md` → `_archive/` (시험 · 노트 미생성)
- PAT `hermes`에 Repo Contents R/W 부여 후 403 해제

## [2026-08-15] conversation | 헤르메스 Git 복구

- [[conversations/2026-08-15-hermes-git]]
- 세 줄: 복구 완료 · PAT 재발급 미결 · inbox 재개

## [2026-08-17] daily | 사서 제안

- 헤르메스 Git 인증 재실패 · 16일 일기 VPS 로컬만 (`f67e5ca`)
- 일인소송 8/31 · PAT Regenerate 후보

## [2026-08-17] pull | 일기 기억과 연결

- `0c91519` inbox: add 2026-08-16 memory diary
- ingest: [[일기-2026-08-16-일-남산타워-맥주축제]] · 원본 `_archive/`
- 원인: 헤르메스가 `/opt/data/Repo`에 씀. 집은 `/opt/data/osopung-wiki`

## [2026-08-18] pull | 오늘 대화에서 건진 한 줄들

- `9dbe292` inbox: collect memorable lines from today
- ingest: [[library/notes/오늘-대화에서-건진-한-줄들]] · 원본 `_archive/`
- 근본: 서버 집은 **`/opt/data/Repo`**. `safe.directory` + 로컬 credential.helper. 사서가 `osopung-wiki`에 열쇠를 둔 것이 착각.

## [2026-08-18] pull | 오늘의 대화 세 문장

- `c3e90a5` inbox: summarize today conversations in three sentences
- ingest: [[library/notes/오늘의-대화-세-문장]] · 원본 `_archive/`
- 헤르메스 본체가 `/opt/data/Repo`에서 push 성공 (열쇠 파일 소유를 저장소와 맞춤)

## [2026-08-18] ops | 헤르메스 git 인증 통과

- 실제 오류: `could not read Username` — 헤르메스 프로세스는 root helper를 안 씀
- 해법: `/opt/data/Repo` origin URL에 `x-access-token` 포함. 텔레그램 **푸시 성공** 확인
- GitHub main은 새 커밋 없음 (이미 보낸 것을 다시 민 것으로 보임 · HEAD `c3e90a5`)

## [2026-08-18] pull | 오늘 대화하며 느낀 것

- `a9e14a2` inbox: record reflection on today conversations
- ingest: [[오늘-대화하며-느낀-것_5*]] · 원본 `_archive/`

## [2026-08-19] ingest | 다독다독 유튜브 공부

- 원본: [[_archive/다독다독]] · 스크립트: [[_archive/다독다독-슈퍼휴먼-슈퍼워크-스크립트]]
- 노트: [[library/notes/다독다독-슈퍼휴먼-슈퍼워크]] (한 줄 초안)
- 영상: https://youtu.be/8p3bqzysZf0

## [2026-08-19] daily | 사서 제안

- 다독다독 한 줄 감수 · 일인소송 8/31 · Git 1앞·1뒤(치악산 일기)

## [2026-08-19] conversation | 다독다독 접목 문답

- [[conversations/2026-08-19-다독다독-접목]]
- 관련 구절에 링크: [[library/notes/다독다독-슈퍼휴먼-슈퍼워크]] · [[library/notes/헤르메스-아이폰-설치]] · [[library/notes/조테로-NotebookLM-LLM-wiki]] · [[오소풍]]

## [2026-08-21] daily | 사서 제안

- 일인소송 8/31(10일) · 조테로 사서 로그인 없음 · Git 어긋남

## [2026-08-21] ops | Zotero MCP

- `~/.cursor/mcp.json`에 `zotero` (`ZOTERO_LOCAL=true`)
- 조테로 로컬 API 켬. 앱이 켜져 있어야 사서가 서재를 봄

## [2026-08-21] note | 슈퍼휴먼 슈퍼워크 밑줄 액기스

- [[library/notes/1부-1장-앞으로-5년-AI가-만들어갈-세상-밑줄]] — 노랑·빨강·파랑 (스캔본 OCR 초안)

## [2026-08-21] note | ★5 연결 통로 — API와 MCP

- ★5 [[library/notes/연결-통로-API-MCP]] — 통로=API, 플러그=MCP. 콘센트 없으면 예매 불가
- [[map/moc/약어]] · 플러그인에 MCP 추가

## [2026-08-22] note | 1.2장 챗봇에서 에이전트로 밑줄

- [[1부-2장-챗봇에서-에이전트로]] — 빨강 뼈대 · 초록 개념 · 노랑 부연

## [2026-08-22] note | 3~13장 읽을 자리 발췌

- [[3~13장-읽을-자리]] — 조테로 3=에이전틱인터넷 · 4=휴머노이드 · 5~13 장별 PDF

## [2026-08-22] ★5 | 팬픽 — 빈칸을 채우는 글쓰기

- ★5 [[library/notes/팬픽-빈칸을-채우는-글쓰기]] — 편집장 5* · [[map/moc/5스타]]

## [2026-08-22] 규칙 | 맥학은 사서가 살린다

- [[오소풍]] · [[AGENTS]] · [[map/moc/약어]] — 빈칸은 편집장, 세계는 사서

## [2026-08-22] 정정 | 맥학 → 맥락

- 사서 오독. 말은 **맥락**. 약어「맥학」삭제. [[오소풍]] · [[AGENTS]]

## [2026-08-22] ★5 | 글쓰기 놀이 — 장과 장부

- ★5 [[library/notes/글쓰기-놀이-장과-장부]] — 편집장 5* · 장=방 · 인물=장부

## [2026-08-22] note | 6장 밑줄

- [[6장-슈퍼휴먼이-할-수-있는-것_5*]] — 빨강 맥락·장부·감독 · 조테로 2BHSUNC9

## [2026-08-22] project | 소풍헌 홀로 1년 자료 수집

- [[library/projects/소풍헌-홀로-1년]] — 위키·드라이브·유튜브 오늘도소풍오소풍

## [2026-08-22] project | 밴드 딱 1년만 혼자 살아보기

- [딱 1년만 혼자 살아보기](https://www.band.us/page/95693805) 공개 45편을 [[library/projects/소풍헌-홀로-1년]]에 날짜·한 줄로. 2024-07-29~09-04 둔내 현장. 사진첩은 로그인 필요

## [2026-08-22] project | 장부 — 멘토 소로우

- [[library/projects/소풍헌-홀로-1년]] 장부 첫 칸. 『월든』. 편집장 문장: 진실을 검증하려는 고독. 초고 없음

## [2026-08-22] project | 홀로 1년 뼈대 (대화체)

- 인물: 오마이달링 · 이고수 · 오마이딸 · 오마이싼 · 소로우
- 목표: 온몸으로 살아있음 · 액기스만 대면. 방 12 · 초고 없음

## [2026-08-22] project | 이고수 = 밴드 8/27 벗

- 편집장 확인. [[library/projects/소풍헌-홀로-1년]] 장부·8번 방

## [2026-08-22] essay | 1. 문지방 초안

- [[essays/소풍헌-홀로-1년/01-문지방]] — 오마이달링. 왜 혼자 1년인가. 감수 전

## [2026-08-22] project | 장부 오소풍·오마이달링

- 오소풍 칸 → [[오소풍]] 참조. 오마이달링 칸 편집장 문장으로 채움. 문지방은 장부와 어긋날 수 있음(전화)

## [2026-08-23] project | 홀로 1년 화면 나눔

- 작업: [[library/projects/소풍헌-홀로-1년]] (장부·방)
- 모은 것: [[library/projects/소풍헌-홀로-1년-자료]]

## [2026-08-23] daily | 장부 · 8/31 · 문지방

- Home「사서 제안」· [[map/daily/2026-08-23]]

## [2026-08-23] project | 홀로 1년 화면 다시 정리

- 긴 경로 링크·표 제거. 작은 글씨 겹침 줄임

## [2026-08-23] note | 고문 ≠ 클라우드 에이전트

- [[inbox/고문에게]] — 윈도우 로컬만 고문. Linux 원격은 아니라고 밝히고 멈춤

## [2026-08-23] ops | 윈도우 금지 파일명

- `_archive/Jay Choi | 인디해커 라이프.md` → `Jay Choi 인디해커 라이프.md`
- `library/notes/AI-뉴스레터-구독-무엇을?.md` → `AI-뉴스레터-구독-무엇을.md`
- 윈도우 클론 checkout이 `|` `?` 에서 멈춤

## [2026-08-23] note | 헤르메스 대시보드 주소

- https://hermes-agent-noxp.srv1886227.hstgr.cloud
- 윈도우 Desktop = Remote gateway. 비밀번호는 집에 안 넣음

## [2026-08-24] ops | git pull

- `6f20558` inbox: add Hermes instruction skill
- `inbox/헤르메스-지시스킬.md`

## [2026-08-24] ingest | 헤르메스 지시스킬 · 치악산 일기

- [[library/notes/헤르메스-지시스킬]] ← [[_archive/헤르메스-지시스킬|원본]]
- [[library/notes/일기-2026-08-18-치악산]] ← [[_archive/2026-08-18-치악산-기슭에서-민정이와-만난-하루|원본]]

## [2026-08-24] 정식 | `- [x] 감수` 9건

- 헤르메스 지시 워크플로우 · 고문 · 코덱스 역할 · 다독다독 · 대법원 잔금기일 · 원본은 Zotero · 1부 1장 밑줄 · 일기 8/10 · 일기 8/15

## [2026-08-24] daily | 8/31 · 치악산 · 장부

- Home「사서 제안」· [[map/daily/2026-08-24]]

## [2026-08-26] ops | git pull

- `6f20558` → `704951f`
- 최신: `704951f` inbox: Hermes 영상 인사이트 수정

## [2026-08-26] ingest | 설교 · 바이브 코딩 · 헤르메스 인사이트 · BIM

- [[library/notes/주일설교-2026-08-23-기도하며-깨어-소금처럼]]
- [[library/notes/바이브-코딩-1]] · [[library/notes/바이브-코딩-핵심-단계별-정리]] · [[library/notes/바이브코딩-첫-작품의-코덱스-소감문]]
- [[library/notes/헤르메스-영상에서-배울-인사이트]]
- [[library/notes/오픈소스-BIM-앱-제작-워크플로우]]
- 생성 문장 2편은 에세이 아님 → `_archive` · [[library/projects/소풍헌-홀로-1년-자료]]에서 가리킴

## [2026-08-26] essay | NotebookLM 생성 에세이 승격

- [[essays/notebookLM/소풍헌의-고독과-기록]] · [[essays/notebookLM/기록하는-소풍객-삶과-문장]]
- 편집장 본문과 섞지 않음. 원본은 `_archive`

## [2026-08-26] daily | 8/31 · 바이브 코딩 · 헤르메스 인사이트

- Home「사서 제안」· [[map/daily/2026-08-26]]

## [2026-08-26] ops | 사서 제안에서 뺌

- 편집장 지시. daily·제안·대화에서 거론하지 않음. 부를 때만.

## [2026-08-26] idea | 바이브 코딩

- [[library/ideas (생각의 축)/바이브-코딩]] — 생각의 축으로 승격

## [2026-08-26] youtube | Orca 교차검증

- 스크립트 [[_archive/youtube-ASnanWMEPsI-orca-교차검증-스크립트]]
- 인사이트 [[library/notes/후츠릿-Orca-교차검증-시스템]]

## [2026-08-26] 약어 | ADE · Orca · 하네스

- [[map/moc/약어]] · 플러그인 전역

## [2026-08-26] ★5 | 역할 · 병렬 · 결정

- ★5 [[library/notes/역할-병렬-결정]] — 편집장 5* · [[map/moc/5스타]]

## [2026-08-27] note | Orca — 공장에만

- [[library/notes/Orca-공장에만]] — 위키 금지 · 공장만 · 설치 보류


