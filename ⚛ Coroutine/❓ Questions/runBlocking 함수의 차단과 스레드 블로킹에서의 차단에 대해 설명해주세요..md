---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[runBlocking 함수와 launch 함수의 차이를 설명해주세요.]]"
next page: "[[코루틴 내부에서 runBlocking 함수를 호출하지 않는 이유는 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[스레드 블로킹](스레드%20블로킹.md)은 [스레드](스레드.md)가 어떠한 작업에도 사용될 수 없도록 차단되는 것을 의미하고, [runBlocking](runBlocking.md) 함수의 [차단](차단.md)은 `runBlocking` [코루틴](코루틴.md)과 그 [자식 코루틴](자식%20코루틴.md)을 제외한 다른 작업이 스레드를 사용할 수 없도록 차단된 것을 의미합니다.
