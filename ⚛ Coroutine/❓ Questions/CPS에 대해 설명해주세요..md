---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
prev page: "[[CoroutineStart.UNDISPATCHED와 무제한 디스패처는 어떤 차이를 가지나요?]]"
next page: "[[Continuation이란 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[코루틴](코루틴.md)이 [일시 중단](일시%20중단.md)되고 [재개](재개.md)하기 위해서는 코루틴의 실행 정보를 어딘가 저장해야 합니다.
그래서 코틀린은 실행 정보를 저장하고 전달하는 데 CPS(Continuation Programming Style)이라는 프로그래밍 방식을 채택합니다.
CPS는 [Continuation](Continuation.md)을 전달하는 스타일이라는 뜻입니다.
