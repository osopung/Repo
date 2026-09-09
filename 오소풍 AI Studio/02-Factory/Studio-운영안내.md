---
title: "Studio 운영 안내"
type: note
domain: other
status: final
updated: 2026-09-09
media: []
source: "https://docs.google.com/document/d/1cQ0eq_kZ9T6nOLfupPRIfXKVAeiAfo4L6zjv1KTa3QE/edit"
---

# Studio 작업 안내

Factory 경로: `studio/README.md`

`studio/`는 회사 기준문서와 에이전트별 업무를 관리한다.

## 내 한 줄

inbox에서 받아 work에서 만들고 outbox에 올린다. 방은 건너뛰지 않는다.

- [x] 감수

```text
studio/
├── company/      회사 기준문서
├── templates/    공용 작업 양식
└── agents/
    ├── cursor/  출판 제작실
    ├── gemini/   수묵 제작실
    ├── codex/    AI 제품 개발실
    └── hermes/   조사·운영실
```

각 방:

- `inbox/` — 기획실장이 발행하고 오소풍이 착수를 정한 작업지시서
- `work/` — 담당자만 수정하는 작업 파일
- `outbox/` — 결과물과 완료 보고

첫 단계에서는 다른 에이전트의 방으로 직접 파일을 옮기지 않는다. 담당자는 자기 `outbox/`에 결과를 두고, 다음 담당자에게 전달할 작업은 기획실장이 새 지시서로 발행한다.

## 작업 순서

1. 작업지시서를 담당자 `inbox/`에 등록한다.
2. 담당자는 상태를 `작업 중`으로 바꾸고 자기 `work/`에서 작업한다.
3. 결과와 확인 내용을 `outbox/`에 두고 상태를 `검토 요청`으로 바꾼다.
4. 오소풍이 승인하면 상태를 `승인`으로 기록한다.

모든 변경은 `work/<agent>/<task-id>` 브랜치에서 진행한다.

## 연결

- [[오소풍 AI Studio/02-Factory/구조-지도]] · [[오소풍 AI Studio/_index]]
