---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[Continuation이란 무엇인가요?]]"
next page: "[[일반적인 일시 중단 함수를 테스트하기 위해 무엇을 준비해야 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[suspendCancellableCoroutine](suspendCancellableCoroutine.md) 함수는 [코루틴](코루틴.md)을 [일시 중단](일시%20중단.md)하고 [CancellableContinuation](CancellableContinuation.md) 수신 객체로 코루틴의 실행 정보를 받습니다.
`resume` 함수로 재개되고 `T`를 반환합니다.
