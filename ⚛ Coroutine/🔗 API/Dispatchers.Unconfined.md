---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineDispatcher]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - val
learned:
---
##### 🖋️ Signature
---
```Kotlin
public actual val Unconfined: CoroutineDispatcher
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)을 실행시킨 [스레드](스레드.md)에서 즉시 실행하도록 만드는 [디스패처](디스패처.md) ^desc-1

##### ➕ Extra
---
- [무제한 디스패처](무제한%20디스패처.md)
- 코루틴을 생성한 스레드에서 (스레드 스위칭 없이) 즉시 코루틴이 실행됨
  ⋍ [CoroutineStart.UNDISPATCHED](CoroutineStart.UNDISPATCHED.md) 옵션을 적용했을 때의 동작과 유사 ^desc-2
- 코루틴이 [일시 중단](일시%20중단.md) 후 [재개](재개.md)되면 자신을 재개시키는 스레드에서 실행됨
  ⇒ 어떤 스레드가 재개시키는지 예측하기 어렵기 때문에 일반적인 상황에서 사용하면, [비동기 작업](비동기%20작업.md)이 불안정해짐 ^desc-3
