---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[CoroutineScope란 무엇인지 설명해주세요.]]"
next page: "[[CoroutineScope가 코루틴에게 실행 환경을 제공하는 방식에 대해 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineScope](CoroutineScope.md) 인터페이스를 구현해 생성하는 방법과 `CoroutineScope` 함수를 사용하여 생성하는 방법이 있습니다.
만약, `CoroutineScope` 함수의 인자로 넘길 [CoroutineContext](CoroutineContext.md)에 [Job](Job.md) 객체가 포함돼 있지 않으면, 새로운 `Job` 객체를 생성합니다.
