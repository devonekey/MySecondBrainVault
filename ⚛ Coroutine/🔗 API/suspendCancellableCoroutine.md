---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
parent pages: 
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
public suspend inline fun <T> suspendCancellableCoroutine(  
    crossinline block: (CancellableContinuation<T>) -> Unit  
): T
```

##### ℹ️ Description
---
- 호출부의 [코루틴](코루틴.md)을 [일시 중단](일시%20중단.md)하고, 실행 정보를 [Continuation](Continuation.md) 객체에 저장해 람다식에서 [CancellableContinuation](CancellableContinuation.md) 수신 객체로 제공하는 함수

##### ➕ Extra
---
- [콜백](콜백.md) 기반 [비동기 작업](비동기%20작업.md)을 코루틴으로 변환할 때 사용
- 많이 사용하는 [delay](delay.md)같은 일시 중단 함수들이 이와 비슷하게 구현됨
