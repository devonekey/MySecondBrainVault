---
importance: High
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
public actual val Main: MainCoroutineDispatcher
```

##### ℹ️ Description
---
- [메인 스레드](메인%20스레드.md)를 사용하기 위한 [CoroutineDispatcher](CoroutineDispatcher.md)
- UI가 있는 [애플리케이션](애플리케이션.md)에서 메인 스레드의 사용을 위해 사용되는 `CoroutineDispatcher`

##### ➕ Extra
---
- 별도의 라이브러리를 추가해야 해당 객체를 사용할 수 있음
  그렇지 않으면 `IllegalStateException` [예외](예외.md) 발생
