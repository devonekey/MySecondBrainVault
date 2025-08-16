---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[CoroutineScope를 생성하는 방법을 설명해주세요.]]"
next page: "[[어떻게 하면 CoroutineScope에서 벗어날 수 있을까요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[코루틴 빌더](코루틴%20빌더.md) 함수로 [코루틴](코루틴.md)을 생성할 때, 기존에 설정된 [실행 환경](실행%20환경.md)에 `context` 인자로 넘어오는 [CoroutineContext](CoroutineContext.md) 객체로 실행 환경을 덮어씁니다. 
그리고 생성된 `CoroutineContext`에, 생성되는 [Job](Job.md) 객체를 더해 실행 환경을 설정합니다.
