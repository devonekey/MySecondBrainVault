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
    DEFAULT
}
```

##### ℹ️ Description
---
- [코루틴 빌더](코루틴%20빌더.md) 함수의 `start` 인자로 아무런 값이 전달되지 않을 때의 기본 실행 옵션

##### ➕ Extra
---
- 코루틴 빌더 함수를 호출한 즉시 [코루틴](코루틴.md)의 실행을 [CoroutineDispatcher](CoroutineDispatcher.md) 객체에 예약하며, 코루틴 빌더 함수를 호출한 코루틴은 계속해서 실행을 이어나감
