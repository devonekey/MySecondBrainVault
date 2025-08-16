---
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
  - "[[📘 코틀린 코루틴의 정석/9장 - 일시 중단 함수]]"
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
public suspend fun <R> supervisorScope(block: suspend CoroutineScope.() -> R): R
```

##### ℹ️ Description
---
- [SupervisorJob](SupervisorJob.md) 객체를 가진 [CoroutineScope](CoroutineScope.md)를 생성하는 함수

##### ⛔️ How to prevent Exception Propagation?
---
- [supervisorScope](supervisorScope.md)를 사용한 [예외 전파 제한](예외%20전파%20제한.md) ^desc-1
	- 다른 방법들과 다르게 복잡한 설정 없이도 구조화를 깨지 않고 [예외 전파](예외%20전파.md)를 제한할 수 있음
```Kotlin
supervisorScope().apply {
    launch(CoroutineName("Coroutine1")) {
        throw Exception("예외 발생")
    }
    launch(CoroutineName("Coroutine2")) {
        // 해당 코루틴은 취소되지 않음
    }
}
```
^code-1

##### 🏃‍♂️ How to run Coroutines on Suspend Function?
---
```Kotlin
suspend fun suspendFun(): List<String> = supervisorScope {
    val deferred1 = async { getFromDB() }
    val deferred2 = async { getFromServer() }

	return@supervisorScope awaitAll(deferred1, deferred2)
}
```
^code-2

##### ➕ Extra
---
![[SupervisorJob.md#^desc-3]]
