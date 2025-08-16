---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[CoroutineScope가 코루틴에게 실행 환경을 제공하는 방식에 대해 설명해주세요.]]"
next page: "[[코루틴의 구조화를 깨는 방법은 왜 최대한 지양해야 할까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineScope](CoroutineScope.md) 내에서 `CoroutineScope` 함수를 호출하여 새로운 `CoroutineScope`를 생성하면 기존 계층 구조를 따르지 않는 새로운 [Job](Job.md) 객체가 생성돼 벗어날 수 있습니다.(단, `CoroutineScope` 함수를 호출할 때 기존의 `Job` 객체를 넘기지 않아야 함)
또는 [코루틴 빌더](코루틴%20빌더.md) 함수를 통해 [코루틴](코루틴.md)을 생성할 때, `context` 매개변수에 명시적으로 `Job` 객체를 추가하는 방법으로도 벗어날 수 있습니다.
