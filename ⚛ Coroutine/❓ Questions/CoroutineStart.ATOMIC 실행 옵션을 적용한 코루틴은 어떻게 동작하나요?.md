---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[CoroutineStart.DEFAULT 실행 옵션은 코루틴이 어떻게 실행되도록 만드나요?]]"
next page: "[[CoroutineStart.UNDISPATCHED 실행 옵션은 코루틴은 어떻게 동작하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[코루틴](코루틴.md)이 생성되고 [스레드](스레드.md)로 분배되기 전, [작업 대기열](작업%20대기열.md)에 머무는 동안 [실행 대기](생성.md) 상태가 됩니다.
이 때 [CoroutineStart.ATOMIC](CoroutineStart.ATOMIC.md) 실행 옵션을 적용한 코루틴이라면, 실행 대기 상태에서 취소되지 않게 됩니다.
