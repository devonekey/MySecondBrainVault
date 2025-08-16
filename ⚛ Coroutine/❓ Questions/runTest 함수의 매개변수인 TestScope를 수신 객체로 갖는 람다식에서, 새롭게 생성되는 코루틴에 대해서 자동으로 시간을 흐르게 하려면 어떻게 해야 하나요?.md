---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/12장 - 코루틴 단위 테스트]]"
answered by:
  - Book
prev page: "[[TestCoroutineScheduler 객체와 연결된 모든 작업이 완료될 때까지 어떻게 가상 시간을 흐르게 할 수 있나요?]]"
next page: "[[일시 중단 함수가 아닌 함수 내부에서 새로운 코루틴을 실행하는 객체에 대해 테스트를 어떻게 할까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[runTest](runTest.md) 함수는 람다식 내부에서 실행된 [일시 중단 함수](일시%20중단%20함수.md)에 대해서만 가상 시간을 흐르게 만듭니다.
새로 생성된 [코루틴](코루틴.md)들에 대해서 시간을 흐르게 만들려면 [advanceUntilIdle](advanceUntilIdle.md) 함수를 호출해야 합니다.
