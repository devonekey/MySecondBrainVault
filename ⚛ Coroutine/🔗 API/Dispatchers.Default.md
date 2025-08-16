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
  - val
learned:
---
##### 🖋️ Signature
---
```Kotlin
public actual val Default: CoroutineDispatcher
```

##### ℹ️ Description
---
- CPU를 많이 사용하는 연산 작업을 위한 [CoroutineDispatcher](CoroutineDispatcher.md)
- [CPU 바운드 작업](CPU%20바운드%20작업.md)이 필요할 때 사용하는 [CoroutineDispatcher](CoroutineDispatcher.md)

##### ➕ Extra
---
- [공유 스레드 풀](공유%20스레드%20풀.md)을 사용
