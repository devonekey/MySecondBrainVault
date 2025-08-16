---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[Job 구조화를 깨는 방법들을 설명해주세요.]]"
next page: "[[runBlocking 함수와 launch 함수의 차이를 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
추가하려는 [Job](Job.md)의 `parent` 매개변수에 부모 `Job`을 연결하여 생성했을 때, 부모 `Job`이 실행 취소를 요청하거나 [실행 완료 중](실행%20완료%20중.md)에 있더라도 추가한 `Job`이 자동으로 완료되지 않습니다.
그래서 추가한 `Job`에 [complete](CompletableJob.complete.md) 함수를 직접 호출해야 하기에 주의해야 합니다.
