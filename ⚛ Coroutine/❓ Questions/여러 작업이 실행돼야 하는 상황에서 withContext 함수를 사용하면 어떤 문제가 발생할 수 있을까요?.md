---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
prev page: "[[컨텍스트 스위칭(Context Switching)이란 무엇인가요?]]"
next page: "[[withContext 함수 실행으로 CoroutineDispatcher에는 어떤 변화가 있을까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[withContext](withContext.md) 함수는 [코루틴](코루틴.md)을 유지한 채로 [스레드](스레드.md)만 변경하는 것이기 때문에 동기적으로 실행됩니다.
병렬적으로 결괏값을 받아야 하는 상황에서는 성능에 문제를 일으킬 수 있습니다.
