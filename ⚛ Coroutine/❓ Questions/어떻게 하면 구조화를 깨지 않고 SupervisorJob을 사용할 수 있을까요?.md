---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[SupervisorJob 객체로 예외 전파를 제한하는 것은 어떤 한계점을 지니고 있나요?]]"
next page: "[[SupervisorJob을 CoroutineScope와 같이 사용하면 구조는 어떻게 변하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[SupervisorJob](SupervisorJob.md) 객체를 추가할 때 `parent` 매개변수에 부모 [Job](Job.md) 객체를 넘기면, 구조화를 깨지 않을 수 있습니다.
