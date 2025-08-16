---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
prev page: "[[CoroutineContext에 같은 구성 요소들을 추가하면 어떻게 설정되나요?]]"
next page: "[[어떻게 CoroutineContext의 구성 요소들에 접근할 수 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineContext](CoroutineContext.md)에 [Job](Job.md) 객체를 추가할 때 `Job`의 `parent` 인자를 넘겨주지 않으면, 구조화가 깨지기 때문에 주의해야 합니다.
