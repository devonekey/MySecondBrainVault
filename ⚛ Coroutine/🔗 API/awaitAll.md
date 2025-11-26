---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
  - GPT
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
public suspend fun <T> awaitAll(vararg deferreds: Deferred<T>): List<T>
```

```Kotlin
public suspend fun <T> Collection<Deferred<T>>.awaitAll(): List<T>
```

##### ℹ️ Description
---
- 복수의 [Deferred](Deferred.md) 객체로부터 결괏값을 수신하기 위한 [[일시 중단]] 함수

##### ➕ Extra
---
- 가변 인자로 `Deferred` 타입의 객체를 받아 모든 `Deferred` [코루틴](코루틴.md)으로부터 결과가 수신될 때까지 호출부의 코루틴을 일시 중단함
- 결과가 모두 수신되면, 결괏값들을 `List`로 만들어 반환하고 호출부의 코루틴을 [재개](재개.md)함
