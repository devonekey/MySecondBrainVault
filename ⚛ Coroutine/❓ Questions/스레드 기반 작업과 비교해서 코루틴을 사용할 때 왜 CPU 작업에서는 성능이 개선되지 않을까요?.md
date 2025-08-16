---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
prev page: "[[Dispatchers.IO가 사용할 수 있는 스레드의 개수는 몇개인가요?]]"
next page: "[[디스패처를 직접 생성하는 방식의 스레드 풀과 Dispatchers.IO, Dispatchers.Default가 사용하는 스레드 풀에는 어떤 차이가 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
입출력 작업에서는 결과를 기다리는 동안 [스레드](스레드.md) 사용 권한을 [양보](양보.md)하여 다른 작업을 할 수 있는 반면, CPU 작업은 스레드가 지속적으로 사용되기 때문입니다.
