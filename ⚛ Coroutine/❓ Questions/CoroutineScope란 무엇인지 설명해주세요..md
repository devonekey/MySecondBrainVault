---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[부모 코루틴이 자식 코루틴에 대해 완료 의존성을 가진다는 말은 무엇인가요?]]"
next page: "[[CoroutineScope를 생성하는 방법을 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineScope](CoroutineScope.md)란 [CoroutineContext](CoroutineContext.md)를 가진 인터페이스로, 자신의 범위에서 생성된 [코루틴](코루틴.md)들에 [실행 환경](실행%20환경.md)을 제공하거나 코루틴의 실행 범위를 관리하는 역할을 합니다.
