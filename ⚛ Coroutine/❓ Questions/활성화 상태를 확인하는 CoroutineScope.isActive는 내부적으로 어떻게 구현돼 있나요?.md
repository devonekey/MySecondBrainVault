---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[CoroutineScope를 취소하는 방법과 취소를 했을 때 어떤 일이 일어날까요?]]"
next page: "[[루트 Job에 대해 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
코드 내부적으로 `coroutineContext`의 [Job](Job.md)에서 [isActive](Job.isActive.md) 프로퍼티를 확인합니다.
