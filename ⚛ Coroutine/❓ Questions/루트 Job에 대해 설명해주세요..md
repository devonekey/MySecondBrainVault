---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[활성화 상태를 확인하는 CoroutineScope.isActive는 내부적으로 어떻게 구현돼 있나요?]]"
next page: "[[Job 구조화를 깨는 방법들을 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[루트 Job](루트%20Job.md)은 부모 [Job](Job.md)이 없는(`null`) `Job`으로, 구조화의 시작점 역할을 합니다.
