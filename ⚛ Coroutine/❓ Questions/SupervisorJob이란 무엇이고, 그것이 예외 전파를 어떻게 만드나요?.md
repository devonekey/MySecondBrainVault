---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[Job 객체로 예외 전파를 제한하는 것은 어떤 한계점을 지니고 있나요?]]"
next page: "[[SupervisorJob 객체로 예외 전파를 제한하는 것은 어떤 한계점을 지니고 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[SupervisorJob](SupervisorJob.md) 객체는 [자식 코루틴](자식%20코루틴.md)으로부터 [예외를 예외 전파](예외%20전파.md)받지 않는 특수한 [Job](Job.md) 객체입니다.

그렇기에, 하나의 자식 코루틴에서 발생한 [예외](예외.md)가 다른 자식 코루틴에 영향을 미치지 못하도록 만듭니다.
