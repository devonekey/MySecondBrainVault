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

##### ➕ Extra
---
- 코루틴을 [스레드](스레드.md)로 보내 실행시키는 역할
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
