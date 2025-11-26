---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
  - GPT
parent pages:
  - "[[CancellationException]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - open
  - class
learned:
---
##### 🖋️ Signature
---
```Kotlin
public open class JobCancellationException(
    message: String,
    cause: Throwable?,
    public val job: Job
) : CancellationException(message, cause)
```

##### ℹ️ Description
---
- [코루틴](코루틴.md) 취소에 사용되는 [예외](예외.md)

##### ➕ Extra
---
- [cancel](Job.cancel.md) 함수에 의해 발생
