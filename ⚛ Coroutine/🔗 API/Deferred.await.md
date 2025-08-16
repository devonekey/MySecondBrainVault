---
aliases:
  - await
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
  - OpenAI
parent pages:
  - "[[Deferred]]"
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
suspend fun <T> Deferred<T>.await(): T
```

##### ℹ️ Description
---
- `await`의 대상이 된 [Deferred](Deferred.md) [코루틴](코루틴.md)이 [실행 완료](실행%20완료.md)될 때까지 `await` 함수를 호출한 코루틴을 [[일시 중단]]하도록 만드는 함수

##### ➕ Extra
---
- 코루틴이 실행 완료되면 결괏값을 반환하고 호출부의 코루틴을 [재개](재개.md)함
- [예외](예외.md) 발생 시 `await` 함수 호출 시점에 예외를 던짐
