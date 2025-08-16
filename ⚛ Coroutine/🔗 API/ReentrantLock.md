---
importance: Lowest
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Java
  - API
  - class
learned:
---
##### 🖋️ Signature
---
```Java
public class ReentrantLock implements Lock, Serializable
```

##### ℹ️ Description
---
- [임계 영역](임계%20영역.md)을 만드는 객체

##### ➕ Extra
---
- 다른 [스레드](스레드.md)에 의해 락이 걸려있다면 락이 해제될 때까지 호출한 [스레드를 블로킹](스레드%20블로킹.md)하고 대기함
- 코루틴에서는 [Mutex](Mutex.md) 객체를 사용하는 것이 권장됨
