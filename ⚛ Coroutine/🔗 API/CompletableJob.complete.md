---
aliases:
  - complete
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
parent pages:
  - CompletableJob
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface CompletableJob : Job {
    public fun complete(): Boolean
}
```

##### ℹ️ Description
---
- 명시적으로 [Job](Job.md)을 완료하는 함수
