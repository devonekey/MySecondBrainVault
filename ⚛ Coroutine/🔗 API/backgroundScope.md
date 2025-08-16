---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
parent pages:
  - "[[TestScope]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - val
learned:
---
##### 🖋️ Signature
---
```Kotlin
public sealed interface TestScope : CoroutineScope {
	public val backgroundScope: CoroutineScope
}
```

##### ℹ️ Description
---
- [runTest](runTest.md) [코루틴](코루틴.md)의 모든 코드가 실행되면 자동으로 취소되는 백그라운드 전용 범위

##### ➕ Extra
---
- 테스트가 무한히 실행되는 것을 방지
