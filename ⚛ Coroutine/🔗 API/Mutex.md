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
  - interface
  - fun
learned:
---
##### 🖋️ Signature
---
```Kotlin
public interface Mutex
```

```Kotlin
@Suppress("FunctionName")  
public fun Mutex(locked: Boolean = false): Mutex =  
    MutexImpl(locked)
```

##### ℹ️ Description
---
- [임계 영역](임계%20영역.md)을 만드는 객체

##### ➕ Extra
---
- 동시 접근을 제한하는 방법
- 공유 변수의 변경 가능 지점을 임계 영역으로 만들어 동시 접근을 제한함
- 락이 해제될 때까지 다른 [코루틴](코루틴.md)이 해당 임계 영역에 진입할 수 없음
- 다른 코루틴에 의해 락이 걸려있으면 락이 해제될 때까지 [스레드](스레드.md)를 [양보](양보.md)하고 [일시 중단](일시%20중단.md) 함
