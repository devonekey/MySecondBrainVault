---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[코루틴에서 예외는 어떻게 전파되나요? 또, 예외를 적절히 처리하지 않으면 어떻게 되나요?]]"
next page: "[[Job 객체로 예외 전파를 제한하는 것은 어떤 한계점을 지니고 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[코루틴 빌더](코루틴%20빌더.md) 함수의 `context` 매개변수에 [Job](Job.md) 객체를 추가하여 구조화를 깹니다.
구조화가 깨졌기 때문에 상위 코루틴에 [예외를 전파](예외%20전파.md)하지 않게 됩니다.
