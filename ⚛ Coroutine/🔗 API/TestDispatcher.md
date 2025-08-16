---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - OpenAI
parent pages:
  - "[[CoroutineDispatcher]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - Test
  - abstract
  - class
learned:
---
##### 🖋️ Signature
---
```Kotlin
@Suppress("INVISIBLE_REFERENCE")
public abstract class TestDispatcher internal constructor() : CoroutineDispatcher(), Delay, DelayWithTimeoutDiagnostics
```

##### ℹ️ Description
---
- 테스트 환경에서 동작하는 [디스패처](디스패처.md)의 추상 클래스
