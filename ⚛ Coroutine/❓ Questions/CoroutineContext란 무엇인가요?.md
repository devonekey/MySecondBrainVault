---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
prev page: "[[launch 함수와 async 함수의 매개변수로 어떤 것들이 들어가나요?]]"
next page: "[[CoroutineContext의 구성 요소와 각 구성 요소는 어떤 역할을 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineContext](CoroutineContext.md)는 [코루틴](코루틴.md)을 실행하는 [실행 환경](실행%20환경.md)을 관리하는 인터페이스입니다.
`CoroutineContext` 객체는 [CoroutineDispatcher](CoroutineDispatcher.md), [CoroutineName](CoroutineName.md), [Job](Job.md), [CoroutineExceptionHandler](CoroutineExceptionHandler.md)를 조합하여 실행 환경을 설정합니다.
