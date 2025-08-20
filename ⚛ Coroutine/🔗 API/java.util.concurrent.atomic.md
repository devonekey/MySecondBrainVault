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
  - Kotlin
  - API
learned:
---
##### 🖋️ Signature
---
```Java
package java.util.concurrent.atomic;
```

##### ℹ️ Description
---
- [원자성](원자성.md)이 있는 데이터 구조를 제공하는 패키지

##### ➕ Extra
---
- `AtomicInteger`, `AtomicReference` 등의 클래스를 사용하여, 원자성을 부여하고 `getAndUpdate`, `incrementAndGet` 등의 함수를 사용하여 [경쟁 상태](경쟁%20상태.md) 문제를 해결함
- 다른 [스레드](스레드.md)의 [코루틴](코루틴.md)이 해당 객체에 대한 연산을 실행 중인 경우, 코루틴은 [스레드를 블로킹](스레드%20블로킹.md)하고 연산 중인 스레드가 연산을 모두 수행할 때까지 대기함
  ⋍ [ReentrantLock](ReentrantLock.md)을 사용하는 것과 비슷함
