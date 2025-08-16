---
importance: Low
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
parent pages:
  - "[[Mutex]]"
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
public suspend fun lock(owner: Any? = null)
```

##### ℹ️ Description
---
- [임계 영역](임계%20영역.md) 시작 지점임을 표시하는 [일시 중단](일시%20중단.md) 함수

##### ➕ Extra
---
- 락을 획득함
- 해당 임계 영역은 다른 [스레드](스레드.md)에서 접근 불가능하게 만들기 때문에 락을 획득한 후에는 꼭 해제해야 함
