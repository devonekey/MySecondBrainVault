---
importance: Low
originated from:
  - "[[📘 코틀린 코루틴의 정석/1장 - 스레드 기반 작업의 한계와 코루틴의 등장]]"
answered by:
  - Book
prev page: "[[Executor 프레임워크란 무엇이고, 왜 등장하게 됐나요?]]"
next page: "[[멀티 스레드 프로그래밍의 한계점은 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[ExecutorService](ExecutorService.md)는 [스레드 풀](스레드%20풀.md)을 관리하는 객체로, [작업 대기열](작업%20대기열.md)과 스레드 풀로 구성된 구조를 가지고 있습니다.

요청받은 작업을 작업 대기열에 적재하고, 스레드 풀에서 유휴 중인 [스레드](스레드.md)에 작업을 할당합니다.
