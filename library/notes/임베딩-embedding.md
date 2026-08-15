---
title: "임베딩 Embedding"
type: note
domain: other
status: final
updated: 2026-08-10
media:
  - "assets/IMG_8839-embedding.png"
---

## 내 한 줄

임베딩은 내 자료를 AI가 닮은꼴로 찾을 수 있게, 숫자 벡터로 옮기는 일이다.

- [x] 감수

## 공부 자료

![[IMG_8839-embedding.png]]

출처: weaviate (그림)

## 한눈에

```mermaid
flowchart LR
  A[텍스트 · 오디오 · 영상] --> B[embedding model]
  B --> C[숫자 벡터]
```

## 정의 (그림 속 문장)

**임베딩(Embedding)**  
AI가 원래 학습 데이터에 갖고 있지 않은 **『나의 정보』**를, AI가 잘 이해하고 활용할 수 있도록 **특별한 숫자 형태(벡터)**로 변환하는 과정.

## 풀어서


| 단계  | 무엇                             |
| --- | ------------------------------ |
| 입력  | 글·소리·영상 등 내 자료                 |
| 모델  | embedding model이 의미를 숫자 배열로 압축 |
| 출력  | 벡터 — 비슷한 뜻끼리 숫자 공간이 가까움        |


그래서 Smart Composer·사서의 **볼트 검색(RAG)** 은, 키워드만이 아니라 **의미가 가까운 노트**를 고를 수 있다.

## 오소풍과의 연결

- 위키 노트 → (임베딩) → “지금 질문과 닮은 기록” 찾기  
- [[library/notes/옵시디언-지식-꺼내쓰기-구요한|꺼내 쓰기]] · [[library/ideas (생각의 축)/입구로서의-inbox|inbox]] · [[오소풍]]



## 연결

- 원본 이미지: `assets/IMG_8839-embedding.png`

