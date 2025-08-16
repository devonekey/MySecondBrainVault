---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - OpenAI
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
	@ExperimentalCoroutinesApi  
	public fun advanceTimeBy(delayTimeMillis: Long): Unit
}
```

```Kotlin

public class TestCoroutineScheduler : AbstractCoroutineContextElement(TestCoroutineScheduler),  
    CoroutineContext.Element {
	public fun advanceTimeBy(delayTime: Duration)
}
```

```Kotlin
@ExperimentalCoroutinesApi  
public fun TestScope.advanceTimeBy(delayTimeMillis: Long): Unit
```

```Kotlin
@ExperimentalCoroutinesApi  
public fun TestScope.advanceTimeBy(delayTime: Duration): Unit
```

##### ℹ️ Description
---
- 가상 시간을 지정한 시간만큼 진행하는 함수
