---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineStart]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - enum
  - val
learned:
---
##### 🖋️ Signature
---
```Kotlin
public enum class CoroutineStart {
    UNDISPATCHED
}
```

##### ℹ️ Description
---
- [CoroutineDispatcher](CoroutineDispatcher.md) 객체의 [작업 대기열](작업%20대기열.md)을 거치지 않고 호출부의 [스레드](스레드.md)에서 즉시 실행되는 실행 옵션

##### ➕ Extra
---
- 처음 [코루틴 빌더](코루틴%20빌더.md) 함수가 호출됐을 때만 `CoroutineDispatcher` 객체를 거치지 않고 실행됨
	- 만약 [코루틴](코루틴.md) 내부에서 [일시 중단](일시%20중단.md) 후 [재개](재개.md)되면 `CoroutineDispatcher` 객체를 거쳐 실행됨
