---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[어떻게 하면 구조화를 깨지 않고 SupervisorJob을 사용할 수 있을까요?]]"
next page: "[[SupervisorJob을 사용할 때 어떤 점을 유의해서 사용해야 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineScope](CoroutineScope.md) 함수를 통해 `CoroutineScope` 객체가 생성되면 [SupervisorJob](SupervisorJob.md)을 [루트 Job](루트%20Job.md)으로 삼기에, 부모 [Job](Job.md)과 구조가 깨집니다.
