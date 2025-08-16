---
aliases:
  - invokeOnCompletion
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
parent pages:
  - "[[Job]]"
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
public interface Job : CoroutineContext.Element {
    public fun invokeOnCompletion(handler: CompletionHandler): DisposableHandle
}
```

```Kotlin
public interface Job : CoroutineContext.Element {
    public fun invokeOnCompletion(  
        onCancelling: Boolean = false,  
        invokeImmediately: Boolean = true,  
        handler: CompletionHandler
    ): DisposableHandle
}
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)이 [실행 완료](실행%20완료.md)되거나 [취소 완료](취소%20완료.md)됐을 때 실행되는 [콜백](콜백.md)을 등록하는 함수
