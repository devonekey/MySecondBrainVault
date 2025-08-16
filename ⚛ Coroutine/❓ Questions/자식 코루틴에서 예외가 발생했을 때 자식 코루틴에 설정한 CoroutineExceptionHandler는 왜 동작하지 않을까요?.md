---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[코루틴의 예외를 처리할 때 CoroutineContext의 어떤 구성 요소를 사용하나요?]]"
next page: "[[CoroutineExceptionHandler는 언제 사용해야 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineExceptionHandler](CoroutineExceptionHandler.md)는 처리되지 않은 [예외만 처리](예외%20처리.md)합니다.
[자식 코루틴](자식%20코루틴.md)에서 [예외](예외.md)가 발생하면 [부모 코루틴](부모%20코루틴.md)으로 [예외가 전파](예외%20전파.md)되는 데, 이를 자식 코루틴에서는 예외가 처리된 것으로 간주하여 `CoroutineExceptionHandler`가 동작하지 않습니다.
