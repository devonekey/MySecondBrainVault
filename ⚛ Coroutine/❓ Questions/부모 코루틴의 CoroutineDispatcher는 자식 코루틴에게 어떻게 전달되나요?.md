---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
prev page: "[[생성한 디스패처를 어떻게 실행할 수 있나요?]]"
next page: "[[newFixedThreadPoolContext 함수를 사용해 CoroutineDispatcher 객체를 생성하면 왜 경고를 출력할까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[부모 코루틴](부모%20코루틴.md)에서 [자식 코루틴](자식%20코루틴.md)을 생성할 때, `context` 인자에 [CoroutineDispatcher](CoroutineDispatcher.md) 객체를 넣어 전달하고, 별도로 지정하지 않으면 부모 코루틴의 CoroutineDispatcher 객체를 사용합니다.
