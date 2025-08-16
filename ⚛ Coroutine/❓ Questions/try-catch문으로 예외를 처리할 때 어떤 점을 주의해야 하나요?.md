---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[CoroutineExceptionHandler를 사용할 때 어떤 점을 주의해야 하나요?]]"
next page: "[[async 코루틴 빌더 함수는 언제 예외가 발생해 노출되나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[코루틴 빌더](코루틴%20빌더.md) 함수에 대한 [예외는 처리](예외%20처리.md)하지 못하고, 코루틴 빌더 함수 자체 실행만 체크합니다. 
왜냐하면, 람다식의 실행은 [CoroutineDispatcher](CoroutineDispatcher.md)에 의해 [스레드](스레드.md)에 분배될 때 일어나기 때문입니다.
try-catch문을 사용하려면, 람다식 내부에서 사용해야 합니다.
