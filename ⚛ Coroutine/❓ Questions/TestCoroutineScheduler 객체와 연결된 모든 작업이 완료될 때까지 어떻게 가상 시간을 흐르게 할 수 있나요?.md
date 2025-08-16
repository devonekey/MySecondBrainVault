---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
prev page: "[[TestCoroutineScheduler로 어떻게 가상 시간이 흐르도록 만들 수 있나요?]]"
next page: "[[runTest 함수의 매개변수인 TestScope를 수신 객체로 갖는 람다식에서, 새롭게 생성되는 코루틴에 대해서 자동으로 시간을 흐르게 하려면 어떻게 해야 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[advanceUntilIdle](advanceUntilIdle.md) 함수를 사용하면 [CoroutineScope](CoroutineScope.md)의 모든 [코루틴](코루틴.md)들이 완료되도록 만들 수 있습니다.
