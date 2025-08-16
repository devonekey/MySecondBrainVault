---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
answered by:
  - Book
prev page: "[[코루틴 순차 처리가 필요한 경우를 예를 들어 설명해주세요.]]"
next page: "[[코루틴을 미리 생성하고 나중에 실행하는 하는 방법에 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[delay](delay.md) 함수와 [sleep](sleep.md) 함수는 작업을 일정 시간 지연시킨다는 점에서 공통점을 지니고 있습니다.
`sleep` 함수는 해당 함수를 호출하는 [스레드](스레드.md)를 [스레드 블로킹](스레드%20블로킹.md)하지만, `delay` 함수는 해당 함수가 실행되는 동안 호출부의 스레드는 다른 [코루틴](코루틴.md)이 사용할 수 있습니다.
