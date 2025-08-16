---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[코루틴에 어떻게 실행 옵션을 줄 수 있을까요?]]"
next page: "[[CoroutineStart.ATOMIC 실행 옵션을 적용한 코루틴은 어떻게 동작하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineStart.DEFAULT](CoroutineStart.DEFAULT.md) 실행 옵션은 `start` 인자로 아무것도 넘겨주지 않으면 자동 설정되는 옵션입니다.

[코루틴 빌더](코루틴%20빌더.md)를 생성한 즉시 [CoroutineDispatcher](CoroutineDispatcher.md) 객체로 하여금 실행을 예약하고, 코루틴 빌더 함수를 호출한 [코루틴](코루틴.md)을 계속 실행하게 만듭니다.
