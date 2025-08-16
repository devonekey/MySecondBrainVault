---
aliases:
  - start
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
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
    public fun start(): Boolean
}
```

##### ℹ️ Description
---
- [지연 코루틴](지연%20코루틴.md)을 직접 실행하는 함수
