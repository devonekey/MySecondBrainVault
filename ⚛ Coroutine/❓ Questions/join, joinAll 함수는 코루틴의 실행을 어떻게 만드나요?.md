---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
answered by:
  - Book
prev page: "[[코루틴 빌더 함수를 통해 생성하는 것은 무엇인가요?]]"
next page: "[[코루틴 순차 처리가 필요한 경우를 예를 들어 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[join](Job.join.md) 함수는 먼저 처리돼야 하는 [코루틴](코루틴.md)의 실행이 완료될 때까지 호출부의 코루틴을 [일시 중단](일시%20중단.md)하도록 만들어, 코루틴의 실행을 순차 처리할 수 있도록 만듭니다.

[joinAll](joinAll.md) 함수는 다수의 코루틴 실행이 완료될 때까지 호출부의 코루틴을 일시 중단하도록 만듭니다.
