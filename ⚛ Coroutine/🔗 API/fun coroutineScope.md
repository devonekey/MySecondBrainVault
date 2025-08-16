---
aliases:
  - coroutineScope
importance: Medium
originated from:
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
public suspend fun <R> coroutineScope(block: suspend CoroutineScope.() -> R): R
```

##### ℹ️ Description
---
- 새로운 [CoroutineScope](CoroutineScope.md) 객체를 생성하는 일시 중단 함수

##### ⭐️ Feature
---
- 구조화를 깨지 않고 `CoroutineScope` 객체를 생성함

##### 🏃‍♂️ How to run Coroutines on Suspend Function?
---
```Kotlin
suspend fun suspendFun(): List<String> = coroutineScope {
    val deferred1 = async { getFromDB() }
    val deferred2 = async { getFromServer() }

	return@coroutineScope awaitAll(deferred1, deferred2)
}
```
^code-1
