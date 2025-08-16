---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
prev page: "[[CoroutineContext에 Job을 직접 추가할 땐 어떤 점을 주의해야 하나요?]]"
next page: "[[CoroutineContext에 설정된 구성 요소들을 어떻게 제외할 수 있을까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineContext](CoroutineContext.md)의 `get` 인자로 구성 요소의 키를 넘겨 접근할 수 있습니다. 키로는 각 구성 요소의 동반 객체에 정의된 `Key` , 구성 요소 자체 또는 각 구성 요소의 `key` 프로퍼티가 있습니다.
