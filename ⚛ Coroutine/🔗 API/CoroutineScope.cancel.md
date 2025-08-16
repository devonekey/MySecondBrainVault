---
aliases:
  - cancel
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineScope]]"
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
public fun CoroutineScope.cancel(
    message: String,
    cause: Throwable? = null
): Unit
```

##### ℹ️ Description
---
- [CoroutineScope](CoroutineScope.md) 범위 내에서 실행 중인 모든 코루틴에 취소를 요청하는 함수

##### ➕ Extra
---
- 코드 내부적으로 `coroutineContext` 객체의 구성 요소인 [Job](Job.md) 객체를 취소함
