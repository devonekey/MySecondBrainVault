---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
prev page: "[[가상 시간위에서 테스트 하려면 어떤 것들이 준비돼야 할까요?]]"
next page: "[[TestCoroutineScheduler 객체와 연결된 모든 작업이 완료될 때까지 어떻게 가상 시간을 흐르게 할 수 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[TestCoroutineScheduler](TestCoroutineScheduler.md) 객체의 [advanceTimeBy](advanceTimeBy.md) 함수를 호출하여 가상 시간이 흐르도록 만들 수 있습니다.
