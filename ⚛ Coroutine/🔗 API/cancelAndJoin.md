---
importance: Medium
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
  - suspend
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public suspend fun Job.cancelAndJoin()
```

##### ℹ️ Description
---
- `cancelAndJoin` 함수의 대상이 되는 [코루틴](코루틴.md)이 취소 완료될 때까지 호출부의 코루틴을 [일시 중단](일시%20중단.md)하는 함수
