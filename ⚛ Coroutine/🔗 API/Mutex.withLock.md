---
importance: Medium
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
@OptIn(ExperimentalContracts::class)  
public suspend inline fun <T> Mutex.withLock(owner: Any? = null, action: () -> T): T
```

##### ℹ️ Description
---
- [임계 영역](임계%20영역.md)을 지정하는 일시 중단 함수

##### ➕ Extra
---
- 코드가 복잡해질 수록 [lock](Mutex.lock.md)-[unlock](Mutex.unlock.md) 쌍을 사용하면 휴먼 에러를 일으킬 가능성이 커지기 때문에 해당 함수를 사용하는 것이 안전함
