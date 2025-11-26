---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
  - GPT
parent pages:
  - "[[TestDispatcher]]"
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
@Suppress("FunctionName")
public fun StandardTestDispatcher(
    scheduler: TestCoroutineScheduler? = null,
    name: String? = null
): TestDispatcher
```

##### ℹ️ Description
---
- 테스트 전용 [디스패처](디스패처.md) 구현체

##### 🧪 How to test?
---
```Kotlin
@Test
fun `시간 흐름에 따라 변화하는 값 테스트`() {
	val scheduler = TestCoroutineScheduler()
	val dispatcher: TestDispatcher = StandardTestDispatcher(scheduler = scheduler)
	val scope = CoroutineScope(context = dispatcher)
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
	
	scheduler.advanceTimeBy(3_000L)
	
	assertEquals(0, actual)
	
	scheduler.advanceTimeBy(8_000L)
	
	assertEquals(1, actual)
	
	scheduler.advanceTimeBy(11_000L)
	
	assertEquals(2, actual)
	
	scheduler.advanceUntilIdle()
	
	assertEquals(3, actual)
}
```

##### ➕ Extra
---
- [advanceTimeBy](advanceTimeBy.md)나 [advanceUntilIdle](advanceUntilIdle.md) 함수 호출 전까지 작업이 실행되지 않음
