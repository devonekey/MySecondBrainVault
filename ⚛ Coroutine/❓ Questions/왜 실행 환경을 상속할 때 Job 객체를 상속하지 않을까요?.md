---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[부모 코루틴은 모든 실행 환경을 왜 항상 상속하는 것은 아닌가요?]]"
next page: "[[부모 코루틴의 Job 객체와 자식 코루틴의 Job 객체는 어떻게 참조를 하고 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[코루틴](코루틴.md) 제어를 하기 위해서는 [Job](Job.md) 객체가 필요한 데, [상속](실행%20환경%20상속.md)된다면 개별 코루틴의 제어에 어려움이 따르기 때문입니다.
