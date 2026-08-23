---
title: "헤르메스 Git 복구"
type: conversation
topics: [ops]
date: 2026-08-15
agents: [cursor]
updated: 2026-08-15
---

## 맥락

헤르메스 inbox push가 GitHub 인증 오류로 막혀 있었다. 키 문자열을 서버에 넣은 뒤에도 403이 났고, 원인은 PAT `hermes`에 저장소 권한이 비어 있던 것이었다.

## 세 줄 세이브 (AI 로그)

- **한 일:** PAT `hermes`에 Repo Contents R/W를 넣고 VPS credential helper를 맞춘 뒤, 헤르메스 push 복구 (`a781ed0`). 시험 파일은 `_archive/`. 고문 = 조언·조력으로 지침 정리.
- **미결:** 키가 채팅·콘솔 기록에 노출됨 → `hermes` Regenerate/Revoke. `반박내용증명_초안_사서.md`는 루트에 미커밋.
- **다음:** 텔레그램 inbox 쓰기는 이 키로 됨. 안정화되면 키만 갈아끼우기.

## 합의 · 결정

- 헤르메스 Git 열쇠는 VPS `/opt/data/.git-credentials`만. 채팅·텔레그램에 키를 넣지 않는다.
- Fine-grained PAT `hermes`는 **Repo** + **Contents Read and write**가 있어야 push가 된다. 권한 없는 키는 403 (`denied to osopung`).
- 컨테이너 이름: `hermes-agent-noxp-hermes-agent-1`

## 연결

- [[library/notes/헤르메스-아이폰-설치]]
- [[헤르메스에게_8.17.수정]]
- [[library/notes/고문]]
