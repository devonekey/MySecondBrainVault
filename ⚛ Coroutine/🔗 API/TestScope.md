---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
  - GPT
parent pages:
  - "[[CoroutineScope]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - interface
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public sealed interface TestScope : CoroutineScope
```

```Kotlin
@Suppress("FunctionName")  
public fun TestScope(context: CoroutineContext = EmptyCoroutineContext): TestScope
```

##### ℹ️ Description
---
- 테스트 전용 [CoroutineScope](CoroutineScope.md)

##### 🧪 How to test?
---
```Kotlin
@Test
fun `시간 흐름에 따라 변화하는 값 테스트`() {
	val scope = TestScope()
	var actual = 0

	scope.launch {
		delay(5_000L)

		actual = 1

		delay(10_000L)

		actual = 2

		delay(10_000L)

		actual = 3
	}

	assertEquals(0, actual)
	
	scope.advanceTimeBy(3_000L)
	
	assertEquals(0, actual)
	
	scope.advanceTimeBy(8_000L)
	
	assertEquals(1, actual)
	
	scope.advanceTimeBy(11_000L)
	
	assertEquals(2, actual)
	
	scope.advanceUntilIdle()
	
	assertEquals(3, actual)
}
```

##### ➕ Extra
---
- 내부적으로 [TestCoroutineScheduler](TestCoroutineScheduler.md)와 [TestDispatcher](TestDispatcher.md)를 사용해 가상 시간 기반의 [코루틴](코루틴.md) 실행을 제어
