---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[Job에 부모를 명시적으로 설정한 경우, 어떤 점을 주의해야 하나요?]]"
next page: "[[runBlocking 함수의 차단과 스레드 블로킹에서의 차단에 대해 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[runBlocking](runBlocking.md) 함수는 호출부의 [스레드](스레드.md)를 [차단](차단.md)하고 사용하지만, [launch](CoroutineScope.launch.md) 함수는 호출부의 스레드를 차단하지 않는 차이가 있습니다.
