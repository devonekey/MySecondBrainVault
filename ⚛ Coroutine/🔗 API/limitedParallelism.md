---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
parent pages:
  - "[[Dispatchers.IO]]"
  - "[[Dispatchers.Default]]"
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
public abstract class CoroutineDispatcher : AbstractCoroutineContextElement(ContinuationInterceptor), ContinuationInterceptor {
    public open fun limitedParallelism(parallelism: Int): CoroutineDispatcher
}
```

##### ℹ️ Description
---
- 미리 정의된 [디스패처](디스패처.md)가 일부의 [스레드](스레드.md)만 사용해 특정 연산을 실행하도록 하는 함수 ^desc-1

##### ➕ Extra
---
- [Dispatchers.IO](Dispatchers.IO.md)의 `limitedParallelism` 함수는 [공유 스레드 풀](공유%20스레드%20풀.md)의 스레드로 구성된 새로운 [스레드 풀](스레드%20풀.md)을 만듦
  그러기에 해당 함수를 남용하지 않아야 함
- [Dispatchers.Default](Dispatchers.Default.md)의 `limitedParallelism` 함수는 만들어 낼 수 있는 스레드에 제한이 있음
