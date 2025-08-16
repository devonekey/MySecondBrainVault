---
aliases:
  - join
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
  - suspend
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface Job : CoroutineContext.Element {
    public suspend fun join()
}
```

##### ℹ️ Description
---
- [코루틴](코루틴.md)의 실행이 완료될 때까지 호출부의 코루틴을 [일시 중단](일시%20중단.md)하도록 만드는 함수

##### ➕ Extra
---
- `join` 함수를 호출한 코루틴만 일시 중단함
- 코루틴 순차 처리가 필요한 상황에서 쓰임
