---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[일반적인 상황에서 무제한 디스패처를 사용하는 것은 왜 권장되지 않을까요?]]"
next page: "[[CPS에 대해 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineStart.UNDISPATCHED](CoroutineStart.UNDISPATCHED.md) 실행 옵션이 적용된 [코루틴](코루틴.md)과 [Dispatchers.Unconfined](Dispatchers.Unconfined.md) [무제한 디스패처](무제한%20디스패처.md)를 사용한 코루틴 모두 호출자의 [스레드](스레드.md)에서 즉시 실행되는 공통점을 가집니다.

`CoroutineStart.UNDISPATCHED` 실행 옵션이 적용된 코루틴은 자신을 실행한 [CoroutineDispatcher](CoroutineDispatcher.md) 객체를 사용해 재개되는 반면, `Dispatcher.Unconfined` 무제한 디스패처를 가진 코루틴은 자신을 [재개](재개.md)시키는 스레드에서 재개됩니다.
