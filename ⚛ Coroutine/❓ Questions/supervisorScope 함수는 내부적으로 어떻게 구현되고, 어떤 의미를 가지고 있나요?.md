---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[SupervisorJob을 사용할 때 어떤 점을 유의해서 사용해야 하나요?]]"
next page: "[[코루틴의 예외를 처리할 때 CoroutineContext의 어떤 구성 요소를 사용하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[supervisorScope](supervisorScope.md) 함수는 [SupervisorJob](SupervisorJob.md) 객체를 가진 [CoroutineScope](CoroutineScope.md) 객체를 생성하며, `SupervisorJob` 객체는 `supervisorScope` 함수를 호출한 [코루틴](코루틴.md)의 [Job](Job.md)을 부모로 가집니다.

이것은 복잡한 설정없이 구조화를 깨지 않고 [예외 전파를 제한](예외%20전파%20제한.md)할 수 있는 의미를 가집니다.
