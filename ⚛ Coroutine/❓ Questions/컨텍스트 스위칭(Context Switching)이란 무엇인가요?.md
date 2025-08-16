---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
prev page: "[[async-await를 대체할 수 있는 것과 그것이 async-await와는 어떤 차이가 있는지 설명해주세요.]]"
next page: "[[여러 작업이 실행돼야 하는 상황에서 withContext 함수를 사용하면 어떤 문제가 발생할 수 있을까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[withContext](withContext.md) 함수가 호출되면 실행 중인 [코루틴](코루틴.md)의 [실행 환경](실행%20환경.md)을 `withContext` 함수의 인자 값으로 변경해 실행하는 데, 이를 [컨텍스트 스위칭](컨텍스트%20스위칭.md)이라 합니다.

##### ➕ Extra
---
```kotlin
fun main() = runBlocking {
    withContext(context = Dispatcher.IO) {
        // do something...
    }
}
```

[메인 스레드](메인%20스레드.md)에서 실행되던 코루틴을 [Dispatchers.IO](Dispatchers.IO.md)의 [작업 대기열](작업%20대기열.md)에 적재하고, `Dispatcher.IO`가 사용할 수 있는 [스레드](스레드.md)로 보내 코루틴을 실행한다.
