---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
  - OpenAI
parent pages:
  - "[[CancellationException]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - class
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public class TimeoutCancellationException internal constructor(
    message: String,
    @JvmField @Transient internal val coroutine: Job?
) : CancellationException(message), CopyableThrowable<TimeoutCancellationException>
```

```Kotlin
internal fun TimeoutCancellationException(
    time: Long,
    delay: Delay, 
    coroutine: Job
) : TimeoutCancellationException
```

##### ℹ️ Description
---
- 제한된 시간에 끝나지 않은 [코루틴](코루틴.md)을 멈추기 위한 [예외](예외.md)

##### ➕ Extra
---
- 예외가 [부모 코루틴](부모%20코루틴.md)으로 [전파](예외%20전파.md)되지 않고 해당 예외가 발생한 코루틴만 취소함
