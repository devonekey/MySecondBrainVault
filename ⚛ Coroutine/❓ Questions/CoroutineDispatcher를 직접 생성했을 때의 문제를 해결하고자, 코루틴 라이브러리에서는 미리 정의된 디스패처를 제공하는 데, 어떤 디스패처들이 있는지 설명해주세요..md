---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
prev page: "[[newFixedThreadPoolContext 함수를 사용해 CoroutineDispatcher 객체를 생성하면 왜 경고를 출력할까요?]]"
next page: "[[Dispatchers.IO가 사용할 수 있는 스레드의 개수는 몇개인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
- [Dispatchers.IO](Dispatchers.IO.md): 네트워크, DB 등 입출력 관련 작업을 진행할 때 사용하는 디스패처
- [Dispatchers.Default](Dispatchers.Default.md): CPU 연산이 많이 필요한 작업에 사용되는 디스패처
- [Dispatchers.Main](Dispatchers.Main.md):  UI 작업에 필요한 메인 스레드 디스패처
- [Dispatchers.Unconfined](Dispatchers.Unconfined.md): 무제한 디스패처
