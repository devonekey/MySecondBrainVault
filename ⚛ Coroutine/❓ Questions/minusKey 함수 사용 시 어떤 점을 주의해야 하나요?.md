---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
prev page: "[[CoroutineContext에 설정된 구성 요소들을 어떻게 제외할 수 있을까요?]]"
next page: "[[구조화된 동시성의 원칙이란 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
구성 요소를 추가할 때와는 달리, 기존의 [CoroutineContext](CoroutineContext.md)는 유지되고 구성 요소가 제거된 새로운 `CoroutineContext`가 반환됩니다.
