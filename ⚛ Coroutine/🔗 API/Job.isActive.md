---
aliases:
  - isActive
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
answered by:
  - Book
parent pages:
  - "[[Job]]"
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
public interface Job : CoroutineContext.Element {
	public val isActive: Boolean
}
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)이 활성화됐는지의 여부

##### ➕ Extra
---
- 취소가 요청되거나 실행이 완료된 코루틴은 활성화되지 않은 것으로 간주
