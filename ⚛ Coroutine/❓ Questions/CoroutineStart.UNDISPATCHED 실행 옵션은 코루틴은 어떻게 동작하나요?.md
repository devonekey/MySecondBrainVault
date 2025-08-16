---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[CoroutineStart.ATOMIC 실행 옵션을 적용한 코루틴은 어떻게 동작하나요?]]"
next page: "[[무제한 디스패처는 무엇이고 코루틴을 어떻게 실행되도록 만드나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineStart.UNDISPATCHED](CoroutineStart.UNDISPATCHED.md) 실행 옵션을 적용한 [코루틴](코루틴.md)은 [CoroutineDispatcher](CoroutineDispatcher.md) 객체를 거치지 않고 호출부의 [스레드](스레드.md)에서 즉시 실행되게 만듭니다.

해당 옵션은 [코루틴 빌더](코루틴%20빌더.md)가 호출됐을 때만 적용됩니다.
