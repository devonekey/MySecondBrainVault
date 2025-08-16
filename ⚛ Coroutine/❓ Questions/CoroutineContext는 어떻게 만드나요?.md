---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
prev page: "[[CoroutineContext의 구성 요소들은 CoroutineContext 내에 어떻게 존재하고 있나요?]]"
next page: "[[구성 요소가 없는 CoroutineContext는 어떻게 만드나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineContext](CoroutineContext.md)는 각 키에 객체를 직접 대입하는 방법을 쓰지 않습니다.
대신 [CoroutineDispatcher](CoroutineDispatcher.md), [CoroutineName](CoroutineName.md), [Job](Job.md), [CoroutineExceptionHandler](CoroutineExceptionHandler.md)를 더하기 연산자(`+`)를 통해 조합하여 구성합니다.
