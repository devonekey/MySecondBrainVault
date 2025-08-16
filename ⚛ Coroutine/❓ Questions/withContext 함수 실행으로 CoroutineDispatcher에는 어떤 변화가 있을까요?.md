---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
prev page: "[[여러 작업이 실행돼야 하는 상황에서 withContext 함수를 사용하면 어떤 문제가 발생할 수 있을까요?]]"
next page: "[[launch 함수와 async 함수의 매개변수로 어떤 것들이 들어가나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[withContext](withContext.md) 함수는 [CoroutineDispatcher](CoroutineDispatcher.md) 객체와 함께 사용하면, 자유롭게 [스레드](스레드.md)를 변경할 수 있습니다.
`withContext` 함수를 통해 바뀐 `CoroutineDispatcher`가 유효한 범위는 블록 내부입니다.
`withContext` 블록을 벗어나면, 이전의 `CoroutineDispatcher`로 전환된니다.
