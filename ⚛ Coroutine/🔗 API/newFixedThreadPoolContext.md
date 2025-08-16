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
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public actual fun newFixedThreadPoolContext(
    nThreads: Int,
    name: String
): ExecutorCoroutineDispatcher
```

##### ℹ️ Description
---
- 사용할 수 있는 [스레드](스레드.md)가 한 개 이상인 [CoroutineDispatcher](CoroutineDispatcher.md) 객체를 생성하는 함수

##### ➕ Extra
---
- 내부적으로 [ExecutorService](ExecutorService.md)를 생성하는 함수를 통해 [스레드 풀](스레드%20풀.md)을 생성
- 자신 만의 전용 스레드 풀을 생성
- 생성한 스레드는 모두 데몬 스레드
