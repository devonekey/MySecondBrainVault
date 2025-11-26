---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - GPT
parent pages:
  - "[[TestCoroutineScheduler]]"
  - "[[TestScope]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - Test
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public class TestCoroutineScheduler : AbstractCoroutineContextElement(TestCoroutineScheduler), 
    CoroutineContext.Element {
	public fun advanceUntilIdle(): Unit
}
```

```Kotlin
@ExperimentalCoroutinesApi  
public fun TestScope.advanceUntilIdle(): Unit
```

##### ℹ️ Description
---
- 현재 대기 중인 모든 지연·예약 작업을 전부 실행할 때까지 가상 시간을 진행시키는 함수
