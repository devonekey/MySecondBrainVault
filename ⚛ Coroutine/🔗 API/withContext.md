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
public suspend fun <T> withContext(  
    context: CoroutineContext,  
    block: suspend CoroutineScope.() -> T
): T
```

##### ℹ️ Description
---
- 실행 중이던 [코루틴](코루틴.md)을 유지한 채 코루틴의 [실행 환경](실행%20환경.md)만 변경해 작업을 처리하는 [일시 중단](일시%20중단.md) 함수

##### ➕ Extra
---
- 지정된 [코루틴 컨텍스트](코루틴%20컨텍스트.md)로 지정된 일시 중단 블록을 호출하고, 완료될 때까지 일시 중단한 후 결과를 반환함
	1. 인자로 받은 [CoroutineContext](CoroutineContext.md) 객체를 사용해 `block` 람다식을 실행함
	2. `block` 람다식을 모두 실행하면 `CoroutineContext` 객체를 사용해 코루틴을 [재개](재개.md)하면서 결괏값을 반환함
- 코루틴이 유지된 채로 코루틴을 실행하는 [스레드](스레드.md)만 변경되기 때문에 동기적으로 실행됨
- 순차적으로 작업을 실행해야 하는 조건에서 [async](CoroutineScope.async.md)-[await](Deferred.await.md) 작업을 대체할 수 있음
- 순차적으로 실행되기 때문에 성능에 문제를 일으킬 수 있음
- 코루틴이 실행되는 데 사용되는 [CoroutineDispatcher](CoroutineDispatcher.md) 객체는 블록에서만 유효하고, 블록을 벗어나면 이전의 `CoroutineDispatcher` 객체를 사용하게 되며 스레드가 다시 전환됨
