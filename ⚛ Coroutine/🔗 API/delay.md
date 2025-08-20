---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
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
public suspend fun delay(timeMillis: Long)
```

```Kotlin
public suspend fun delay(duration: Duration): Unit
```

##### ℹ️ Description
---
- 작업의 실행을 일정 시간 지연 시키는 [일시 중단](일시%20중단.md) 함수
- 특정 시간만큼 호출부의 [코루틴](코루틴.md)을 일시 중단하게 만드는 함수

##### ➕ Extra
---
- 상태를 추적하고 제어하는 데 사용
- 코루틴을 사용하던 [스레드](스레드.md)를 [양보](양보.md)하고 일정 시간 동안 코루틴을 일시 중단시킴
- 해당 함수가 실행되는 동안 스레드는 다른 코루틴을 사용할 수 있음
