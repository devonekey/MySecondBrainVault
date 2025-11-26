---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - GPT
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - class
learned:
---
##### 🖋️ Signature
---
```Kotlin
@ExperimentalCoroutinesApi  
internal class UncompletedCoroutinesError(message: String) : AssertionError(message)
```

##### ℹ️ Description
---
- [runTest](runTest.md) 종료 시점에 완료되지 않은 [코루틴](코루틴.md)이 존재하면 발생하는예외

##### ➕ Extra
---
- 테스트 내에서 모든 코루틴이 완료됐는지 검증하는 역할
