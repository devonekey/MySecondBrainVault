---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
prev page: "[[스레드 기반 작업과 비교해서 코루틴을 사용할 때 왜 CPU 작업에서는 성능이 개선되지 않을까요?]]"
next page: "[[Dispatchers.Default와 Dispatchers.IO가 limitedParallelism 함수를 사용함에 있어서 어떤 차이가 있는지 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[디스패처](디스패처.md)를 직접 생성하는 방식은 별도의 [스레드 풀](스레드%20풀.md)을 생성하고, 미리 정의된 디스패처를 사용하는 방식은 [공유 스레드 풀](공유%20스레드%20풀.md)을 사용합니다.
