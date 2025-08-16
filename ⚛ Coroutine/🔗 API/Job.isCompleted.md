---
aliases:
  - isCompleted
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
  - val
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface Job : CoroutineContext.Element {
    public val isCompleted: Boolean
}
```

##### ℹ️ Description
---
- [코루틴](코루틴.md) 실행이 완료됐는지 여부
