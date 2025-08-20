---
importance: Highest
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - abstract
  - class
learned:
---
##### 🖋️ Signature
---
```Kotlin
public abstract class CoroutineDispatcher : AbstractCoroutineContextElement(ContinuationInterceptor), ContinuationInterceptor
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)의 실행을 관리하는 객체
- 코루틴을 보내는 객체

##### 🔗 API
---
- [newSingleThreadContext](newSingleThreadContext.md)
  ![[newSingleThreadContext.md#^desc-1]]
- [newFixedThreadPoolContext](newFixedThreadPoolContext.md)
  ![[newFixedThreadPoolContext#^desc-1]]
- [Dispatchers.Default](Dispatchers.Default.md)
  ![[Dispatchers.Default#^desc-1]]
- [Dispatchers.IO](Dispatchers.IO.md)
  ![[Dispatchers.IO#^desc-1]]
- [Dispatchers.Unconfined](Dispatchers.Unconfined.md)
  ![[Dispatchers.Unconfined#^desc-1]]
- [Dispatchers.Default.limitedParallelism](limitedParallelism.md)
  ![[limitedParallelism#^desc-1]]
- [Dispatchers.IO.limitedParallelism](limitedParallelism.md)
  ![[limitedParallelism#^desc-1]]

##### ➕ Extra
---
- 코루틴을 [스레드](스레드.md)로 보내 실행시키는 역할
- 코루틴을 시작하거나 [재개](재개.md)할 스레드를 결정하기 위해 사용됨
- [작업 대기열](작업%20대기열.md)을 포함
```Kotlin
public abstract class CoroutineDispatcher : AbstractCoroutineContextElement(ContinuationInterceptor), ContinuationInterceptor {
    @ExperimentalStdlibApi  
    public companion object Key : AbstractCoroutineContextKey<ContinuationInterceptor, CoroutineDispatcher>(
        ContinuationInterceptor,  
        { it as? CoroutineDispatcher })
}
```
![[CoroutineContext.md#^desc-1]]
