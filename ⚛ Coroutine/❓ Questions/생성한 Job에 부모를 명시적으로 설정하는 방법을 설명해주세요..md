---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[Job 구조화를 깨는 방법들을 설명해주세요.]]"
next page: "[[Job에 부모를 명시적으로 설정한 경우, 어떤 점을 주의해야 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
자식 [Job](Job.md)을 생성할 때 `parent` 매개변수에 부모 `Job`을 넘김으로써 설정합니다.
