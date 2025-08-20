---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
prev page: "[[디스패처를 직접 생성하는 방식의 스레드 풀과 Dispatchers.IO, Dispatchers.Default가 사용하는 스레드 풀에는 어떤 차이가 있나요?]]"
next page: "[[코루틴 빌더 함수를 통해 생성하는 것은 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[Dispatchers.Default](Dispatchers.Default.md)의 경우, 가지고 있는 [스레드](스레드.md)들 중에서 개수를 제한하는 반면, [Dispatchers.IO](Dispatchers.IO.md)의 경우, [공유 스레드 풀](공유%20스레드%20풀.md)에서 스레드를 생성하는 차이가 있습니다.
  
##### ➕ Extra
---
- `Dispatchers.IO`인 경우, 스레드를 생성하므로 해당 함수를 남용해서는 안됩니다.
