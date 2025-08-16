---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/2장 - 코루틴 개발 환경 설정]]"
answered by:
  - Book
prev page: "[[코루틴 내에서 실행 중인 스레드를 출력할 때, 메시지는 어떻게 출력되나요?]]"
next page: "[[어떻게 코루틴에 이름을 추가할 수 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineScope](CoroutineScope.md)의 확장 함수인 [launch](CoroutineScope.launch.md) 함수나 `async` 함수, 또 다른 [runBlocking](runBlocking.md) 함수같은 코루틴 빌더 함수를 호출하여 [코루틴](코루틴.md)을 추가합니다.
