---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[Job 객체로 어떻게 예외 전파를 제한하나요?]]"
next page: "[[SupervisorJob이란 무엇이고, 그것이 예외 전파를 어떻게 만드나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned: 
---
##### 💬 Answer
---
[Job](Job.md) 객체로 구조화를 깨면 예외 전파를 제한할 수 있지만, 동시에 [취소 전파](취소%20전파.md)를 받지 못하는 문제가 있습니다.
또, [비동기 처리](비동기%20작업.md)를 불안정하게 만듦니다.
