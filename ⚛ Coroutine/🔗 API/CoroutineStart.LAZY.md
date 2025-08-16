---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
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
    LAZY
}
```

##### ℹ️ Description
---
- 나중에 실행돼야 할 [코루틴](코루틴.md)을 미리 생성하는 실행 옵션

##### ➕ Extra
---
- [launch](CoroutineScope.launch.md) 함수의 `start` 인자로 `CoroutineStart.LAZY`를 넘겨 코루틴에 시작 옵션을 적용
