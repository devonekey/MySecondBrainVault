---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[무제한 디스패처는 무엇이고 코루틴을 어떻게 실행되도록 만드나요?]]"
next page: "[[일반적인 상황에서 무제한 디스패처를 사용하는 것은 왜 권장되지 않을까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[DefaultExecutor](DefaultExecutor.md) [스레드](스레드.md)는 [delay](delay.md) 함수를 실행하는 스레드로 `delay` 함수가 [일시 중단](일시%20중단.md)을 종료하고 [코루틴](코루틴.md)을 [재개](재개.md)할 때 사용하는 스레드입니다.
