---
title: "헤르메스 MOA — 쓰는 방법"
type: note
domain: other
status: final
star: 5
importance: 5
keywords:
  - 5스타
  - MOA
  - 헤르메스
tags:
  - 5스타
  - MOA
updated: 2026-08-10
media: []
---

# 헤르메스 MOA — 쓰는 방법 ★5

> 키워드: **5스타** · **MOA** · Mixture of Agents

## 내 한 줄

어려운 일은 `/moa`로 여러 모델 의견을 모아 한 번에 본다.

- [x] 감수

## MOA란

**Mixture of Agents** — 참고 모델이 먼저 의견을 내고, **종합 모델(aggregator)**이 실제 답·도구를 담당한다. 한 모델만 쓸 때보다 관점이 넓어진다. 크레딧·시간은 더 든다.

공식: [Mixture of Agents | Hermes](https://hermes-agent.nousresearch.com/docs/user-guide/features/mixture-of-agents)

## 쓰는 방법 (구체)

### 1. 한 번만 (추천 · 가장 쉬움)

텔레그램/CLI:

```text
/moa 여기에 질문을 쓴다
```

→ 기본 MoA 프리셋으로 **그 한 턴만** 돌리고, 끝나면 **원래 모델로 복귀**.  
빈 `/moa`만 치면 사용법.

### 2. 세션 내내 MoA

모델 피커에서 **Mixture of Agents** 프리셋 선택:

```text
/model default --provider moa
```

다시 일반 모델로: 평소 `/model …` 로 전환.

### 3. 프리셋 설정 (VPS)

```bash
hermes moa list
hermes moa configure          # 기본
hermes moa configure review   # 이름 있는 프리셋
```

또는 Dashboard / Desktop → Models → Mixture of Agents.  
참고 모델·종합 모델이 Nexos(또는 해당 provider)에 열려 있어야 한다.

## 언제

| 씀 | 안 씀 |
|----|------|
| 설계·리뷰·관점이 갈릴 때 | 짧은 메모·리마인드·단순 확인 |

## 연결

- 5스타 목록: [[map/moc/5스타|5스타]]
- [[library/notes/헤르메스 역대급 업데이트 4가지 ;Jay-Choi-의견수락-내시스템-도입|Jay Choi — 먼저 MOA]]
- [[library/notes/헤르메스-아이폰-설치|헤르메스 · 아이폰]] · [[헤르메스-에이전트-핵심정리-어디에쓰나-커스-역할분담|헤르메스 핵심]]
- [[오소풍]] · [[inbox/헤르메스에게|헤르메스에게]]
