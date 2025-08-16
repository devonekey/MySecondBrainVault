---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[코루틴의 구조화를 깨는 방법은 왜 최대한 지양해야 할까요?]]"
next page: "[[CoroutineScope를 취소하는 방법과 취소를 했을 때 어떤 일이 일어날까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[코루틴](코루틴.md)을 생성하면 이를 추상화한 [Job](Job.md) 객체를 생성하지만, 직접 `Job`을 생성하더라도 실행할 수 있는 코루틴 코드가 없을 수도 있기 때문입니다.
