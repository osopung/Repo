---
title: "헤르메스로 언제 어디서든 AI 비서 — 코드깎는노인"
type: note
domain: other
status: final
updated: 2026-08-07
media: []
source: "https://youtu.be/LMBX5qZ-DuA"
---

## 내 한 줄

Hostinger 원클릭 + Nexus AI면 API 키 없이 바로, 텔레그램만 붙이면 폰 비서가 된다. 그래서 나도 이같이 만들었다.

- [x] 감수

## 영상

- [헤르메스 에이전트로 언제 어디서든 나와 함께하는 AI비서 만들기 | 코드깎는노인](https://youtu.be/LMBX5qZ-DuA)

## 요약 (VPS·설치 관점)

1. **왜 VPS** — 일반 사용자는 PC 자원·네트워크·명령어가 부담 → Hostinger가 「3분 카레」식 **준비된 Hermes**.
2. **플랜** — 본인 **KVM2** (Hermes에 넉넉) · 기간은 **짧게 먼저** 써 보라.
3. **모델** — Hostinger **Nexus AI**로 Claude·GPT 등 골라 쓰기 → **API 키 발급 없이** 연동 가능. 직접 API도 가능.
4. **설치 흐름** — VPS → Manage → Deploy catalog → **Hermes Agent** → 계정/비번 → Deploy (Docker 컨테이너).
5. **아이폰** — 웹 UI보다 **텔레그램**: BotFather 토큰 + 내 numeric user id → Channels에서 Telegram config → Restart → 폰에서 대화.
6. **고급** — VPS 터미널에서 Docker 이미지로 직접 설치·설정 가능.
7. **편집장 메모(inbox)** — Nexus로 모델 설정 단순화 · 나중에 ==MCP(예: 법률정보) 붙이면 전문 비서화 ==가능 → **오늘은 설치·텔레그램이 먼저**.

## 오소풍에

「클라우드 + 텔레그램 + 아이폰」절차가 **가장 구체적**. Hostinger 원클릭이 진입로로 유력.

## 연결

- [[_archive/코드깎는노인|원본]]
- [[library/notes/헤르메스-아이폰-설치]]
- 이전: [[헤르메스 역대급 업데이트 4가지 ;Jay-Choi-의견수락-내시스템-도입]] · 다음: [[헤르메스 — 노트북 꺼도 24시간 AI 팀-실밸개발자-유튜브]]
