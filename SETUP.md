# 오소풍_wiki — 구축 후 사람 할 일

에이전트가 폴더·규칙·템플릿까지 만들어 둔 상태다.  
아래는 **편집장(사람)** 만 할 수 있는 마무리.

## 1. Obsidian에서 볼트 열기

1. Obsidian → **Open folder as vault**
2. 경로: `/Users/gimjongho/오소풍_wiki`
3. 시작 노트: [[Home]]

설정(이미 넣어둠):

- 새 노트 기본 위치: `inbox/`
- 첨부 기본 위치: `assets/`
- Sync 코어 플러그인: 켜짐 (계정 연결은 사람)

## 2. Obsidian Sync

**올바른 볼트 경로 (한 겹만):**

```
/Users/gimjongho/오소풍_wiki
```

여기 바로 아래에 `DESIGN-v2.md`, `Home.md`, `art/`, `conversations/` 가 보여야 한다.  
`오소풍_wiki/오소풍_wiki/` 처럼 **폴더가 두 겹**이면 잘못된 연결이다.

### 권장 순서 (Mac)

1. Obsidian → **Open folder as vault** → `/Users/gimjongho/오소풍_wiki` (부모 폴더)
2. 설정 → **Sync**
3. 이미 있는 원격 `오소풍_wiki`가 **옛 wiki/ 구조**면  
   - 그 원격에 합치지 말고, **새 원격**을 만들거나  
   - 원격 내용을 비운 뒤 **이 로컬(v2)을 올리기**  
   - (옛 Sync 내용은 필요하면 따로 백업 후 정리)
4. Sync가 초록이면 아이폰에서도 **같은 원격**만 연다
5. 아이폰 `inbox/`에 짧은 메모 하나 → 맥에 나타나는지 확인

### 하지 말 것

- Drive의 `오소풍의 모든것`에 Sync를 다시 걸기  
- `오소풍_wiki` 안에 또 `오소풍_wiki` 폴더를 만들어 Sync 받기  

## 3. Cursor

- 워크스페이스: `~/오소풍_wiki` (이미 이쪽으로 전환됨)
- 규칙 파일: [[AGENTS]] · [[DESIGN-v2]]

자주 쓰는 명령:

| 명령 | 용도 |
|------|------|
| `daily` | 사서 제안 1~3 → Home |
| `ingest inbox/…` | 노트 소화 |
| `대화록` | 합의 정리 |
| `lint` | 검사 |

## 4. 첫 루프 (오늘~이번 주)

- [x] Sync 맥·아이폰 연결
- [x] `inbox/`에 일기·메모 1건
- [x] Cursor에서 `ingest …` 1회 성공
- [x] `daily` 한 번 실행해 Home「사서 제안」확인
- [x] purpose 논지를 내 문장으로 살짝 고치기
- [x] (선택) [[_archive/CHERRY-PICK]] 3개만 체크

## 5. 건드리지 말 것

- `내 드라이브/오소풍의 모든것` — v1 archive (신규 작업 금지)
- 대용량은 `오소풍-미디어-보관` — 판단은 사람
