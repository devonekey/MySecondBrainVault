---
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/2장 - 코루틴 개발 환경 설정]]"
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
  - OpenAI
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public fun <T> runBlocking(
    context: CoroutineContext = EmptyCoroutineContext,
    block: suspend CoroutineScope.() -> T
): T
```

##### ℹ️ Description
---
- 해당 함수를 호출한 [스레드](스레드.md)를 사용해 [코루틴](코루틴.md)을 만드는 [코루틴 빌더](코루틴%20빌더.md) 함수 ^desc-1

##### 🧪 How to test on `runBlocking`
---
![[일시 중단 함수.md#^desc-1]]

##### ➕ Extra
---
- 코루틴과 관련없는 다른 작업이 스레드를 [[점유]]하지 못하게 막음
- 해당 함수로 인해 코루틴이 생성될 경우, [루트 Job](루트%20Job.md) 객체를 생성함
- 실행이 완료될 때까지 호출부의 스레드를 [차단](차단.md)하고 사용
- 일반적인 코드와 코루틴 사이의 연결점 역할을 하기 위해 만들어졌기 때문에, 코루틴 내부에서 다시 `runBlocking` 함수를 호출하는 것은 삼가야 함
