---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
parent pages: 
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
package kotlinx.coroutines

public actual typealias CancellationException
```

```Kotlin
@Suppress("FunctionName")  
public actual fun CancellationException(message: String?, cause: Throwable?) : CancellationException
```

##### ℹ️ Description
---
- [부모 코루틴](부모%20코루틴.md)으로 [전파](예외%20전파.md)되지 않는 [예외](예외.md)

##### ➕ Extra
---
- [JobCancellationException](JobCancellationException.md)
- [TimeoutCancellationException](TimeoutCancellationException.md)
