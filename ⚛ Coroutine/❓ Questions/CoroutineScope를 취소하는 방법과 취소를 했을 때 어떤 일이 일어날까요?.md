---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[코루틴은 Job 객체를 갖지만, 그 역으로는 성립되지 않는 이유는 무엇인가요?]]"
next page: "[[활성화 상태를 확인하는 CoroutineScope.isActive는 내부적으로 어떻게 구현돼 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineScope](CoroutineScope.md)의 확장 함수로 [cancel](CoroutineScope.cancel.md) 함수를 호출하여 취소하면, 범위 내 실행 중인 하위 [코루틴](코루틴.md)까지 취소가 요청됩니다.
