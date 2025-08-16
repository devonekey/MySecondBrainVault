---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[경쟁 상태 문제를 해결하기 위해 어떤 것을 사용하고 어떻게 문제를 해결하는지 설명해주세요.]]"
next page: "[[공유 상태에 접근할 때 하나의 전용 스레드만 사용하면 동시에 접근하는 문제를 해결할 수 있는 데, 어떻게 해결할 수 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[ReentrantLock](ReentrantLock.md) 객체 역시 [Mutex](Mutex.md) 객체처럼 동일한 기능을 하지만, `Mutex`는 락을 획득했을 때 다른 [코루틴](코루틴.md)이 락을 획득할 때까지 [스레드](스레드.md)를 [양보](양보.md)하고 [일시 중단](일시%20중단.md)하는 것에 비해, `ReentrantLock`은 락을 획득했을 때 `lock`을 호출한 [스레드를 블로킹](스레드%20블로킹.md)하여 다른 코루틴이 스레드를 사용할 수 없는 차이가 있습니다.

이런 특성으로, 코루틴에서는 `ReentrantLock` 객체 대신 `Mutex` 객체를 사용하는 것을 권장합니다.
