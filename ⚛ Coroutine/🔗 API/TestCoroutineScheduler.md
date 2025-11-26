---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
  - GPT
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - Test
  - class
learned:
---
##### 🖋️ Signature
---
```Kotlin
public class TestCoroutineScheduler : AbstractCoroutineContextElement(TestCoroutineScheduler),
    CoroutineContext.Element
```

##### ℹ️ Description
---
- 테스트에서 가상 시간을 제어하는 스케줄러

##### 🧪 How to test?
---
```Kotlin
@Test
fun `시간 흐름 테스트`() {
	val scheduler = TestCoroutineScheduler()

	scheduler.advanceTimeBy(5_000L)

	assertEquals(5_000L, scheduler.currentTime)
}
```
