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
  - suspend
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public suspend fun <T> withTimeoutOrNull(timeMillis: Long, block: suspend CoroutineScope.() -> T): T?
```

```Kotlin
public suspend fun <T> withTimeoutOrNull(timeout: Duration, block: suspend CoroutineScope.() -> T): T?
```

##### ℹ️ Description
---
- 시간 제한을 두고 작업을 실행하는 함수

##### ➕ Extra
---
- 주어진 시간 내에 완료되면 결괏값 반환, 그렇지 않으면 [TimeoutCancellationException](TimeoutCancellationException.md)을 외부로 전파하는 대신 내부적으로 예외를 처리하고 `null` 반환
