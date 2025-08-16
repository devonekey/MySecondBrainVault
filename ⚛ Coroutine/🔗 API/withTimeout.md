---
importance: High
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
public suspend fun <T> withTimeout(timeMillis: Long, block: suspend CoroutineScope.() -> T): T
```

```Kotlin
public suspend fun <T> withTimeout(timeout: Duration, block: suspend CoroutineScope.() -> T): T
```

##### ℹ️ Description
---
- 시간 제한을 두고 작업을 실행하는 함수

##### ➕ Extra
---
- 작업(`block`)이 주어진 시간(`timeMillis`) 내에 완료되지 않으면, [TimeoutCancellationException](TimeoutCancellationException.md) 예외 발생
	- 해당 [코루틴](코루틴.md)만 취소함
	- `try`-`catch`문을 통해 처리할 수 있음
```Kotlin
try {
    withTimeout(1_000L) {
	    delay(2_000L)
	    println("코루틴 실행")
    }
} catch (e: TimeoutCancellationException) {
    println(e)
}
```
