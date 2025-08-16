---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineScope]]"
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
public val CoroutineScope.isActive: Boolean
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)이 활성화됐는지 확인하는 프로퍼티

##### ➕ Extra
---
- 취소 요청을 받으면 해당 프로퍼티 값은 `false`로 변경됨
- 코드 내부적으로 `coroutineContext` 객체의 구성 요소인 [Job](Job.md) 객체의 [Job.isActive](Job.isActive.md)로 활성 여부를 확인함
