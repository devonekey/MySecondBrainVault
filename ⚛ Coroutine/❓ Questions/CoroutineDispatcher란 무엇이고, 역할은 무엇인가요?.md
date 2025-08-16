---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
prev page: "[[어떻게 코루틴에 이름을 추가할 수 있나요?]]"
next page: "[[제한된 디스패처와 무제한 디스패처의 차이를 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineDispatcher](CoroutineDispatcher.md)란 [코루틴](코루틴.md)을 [스레드](스레드.md)로 보내 실행시키도록 만드는 주체입니다.
요청된 코루틴을 [작업 대기열](작업%20대기열.md)에 적재하고, 실행할 수 있는 스레드에 코루틴을 할당해 실행될 수 있게 만드는 역할을 합니다.
