---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/2장 - 코루틴 개발 환경 설정]]"
answered by:
  - Book
prev page: "[[멀티 스레드 프로그래밍에 비해 코루틴은 어떤 장점들을 가지고 있나요?]]"
next page: "[[코루틴 이름을 출력하려면 IDE에 어떤 옵션을 넣어야 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[runBlocking](runBlocking.md) 함수는 일반 코드와 [코루틴](코루틴.md) 코드를 연결하는 [코루틴 빌더](코루틴%20빌더.md) 함수로, `runBlocking` 함수를 호출한 [스레드](스레드.md)를 [차단](차단.md)하고 코루틴을 만들어 실행하는 함수입니다.
