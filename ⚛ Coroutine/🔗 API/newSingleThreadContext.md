---
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
  - "[[📘 코틀린 동시성 프로그래밍/1장 - Hello, Concurrent World!]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineDispatcher]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public fun newSingleThreadContext(name: String): CloseableCoroutineDispatcher
```

##### ℹ️ Description
---
- 사용할 수 있는 [스레드](스레드.md)가 하나인 [CoroutineDispatcher](CoroutineDispatcher.md) 객체를 생성하는 함수 ^desc-1

##### ➕ Extra
---
- 내부적으로 [newFixedThreadPoolContext](newFixedThreadPoolContext.md) 함수를 사용
- [공유 상태](공유%20상태.md)에 접근할 때 하나의 스레드만 사용하도록 강제하여, 공유 상태에 동시에 접근하는 문제를 해결할 수 있음
	- 대신 [limitedParallelism](limitedParallelism.md) 함수를 사용할 수 있음
