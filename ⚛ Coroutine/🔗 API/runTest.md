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
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public fun runTest(  
    context: CoroutineContext = EmptyCoroutineContext,  
    timeout: Duration = DEFAULT_TIMEOUT.getOrThrow(),  
    testBody: suspend TestScope.() -> Unit  
): TestResult
```

##### ℹ️ Description
---
- 테스트 [코루틴](코루틴.md)을 실행하는 메인 진입점

##### 🧪 How to test?
---
```Kotlin
@Test  
fun `시간 흐름에 따라 변화하는 값 테스트`() = runTest {  
    var actual = 0  
  
    launch {  
        delay(5_000L)  
  
        actual = 1  
  
        delay(10_000L)  
  
        actual = 2  
  
        delay(10_000L)  
  
        actual = 3  
    }  
  
    assertEquals(0, actual)  
  
    advanceTimeBy(3_000L)  
  
    assertEquals(0, actual)  
  
    advanceTimeBy(8_000L)  
  
    assertEquals(1, actual)  
  
    advanceTimeBy(11_000L)  
  
    assertEquals(2, actual)  
  
    advanceUntilIdle()  
  
    assertEquals(3, actual)  
}
```

##### ➕ Extra
---
- 내부적으로 [TestScope](TestScope.md)를 생성
- 테스트 완료 후, [실행 완료 중](실행%20완료%20중.md) 상태에서 일정 시간(10초) 뒤에도 미완료된 코루틴이 있으면 [UncompletedCoroutinesError](UncompletedCoroutinesError.md) 예외를 던짐
- [join](Job.join.md) 함수를 호출하면 가상 시간이 흘러 [advanceUntilIdle](advanceUntilIdle.md) 함수를 호출한 효과와 동일해짐
