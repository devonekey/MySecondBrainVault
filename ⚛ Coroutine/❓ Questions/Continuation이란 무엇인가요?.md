---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[CPS에 대해 설명해주세요.]]"
next page: "[[suspendCancellableCoroutine 함수의 동작에 대해 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[Continuation](Continuation.md)은 이어서 실행해야 하는 작업을 말합니다.
`Continuation` 객체는 [코루틴](코루틴.md)의 [일시 중단](일시%20중단.md) 시점에 코루틴의 실행 상태를 저장하며, 다음에 실행해야 하는 작업에 대한 정보가 포함됩니다.
