---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
answered by:
  - Book
parent pages: 
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
public suspend fun joinAll(vararg jobs: Job): Unit
```

```Kotlin
public suspend fun Collection<Job>.joinAll(): Unit
```

##### ℹ️ Description
---
- 복수의 [코루틴](코루틴.md)의 실행이 모두 끝날 때까지 호출부의 코루틴을 [일시 중단](일시%20중단.md)하도록 만드는 함수
