---
importance: Low
originated from:
  - "[[📘 코틀린 코루틴의 정석/1장 - 스레드 기반 작업의 한계와 코루틴의 등장]]"
answered by:
  - Book
prev page: "[[스레드를 직접 다루는 방식의 한계점은 무엇인가요?]]"
next page: "[[ExecutorService의 구조와 동작에 대해 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
Executor 프레임워크는 [[스레드 풀]]을 사용하며, 요청받은 작업을 적절한 [스레드](스레드.md)에 할당하는 시스템입니다.
개발자가 직접 스레드 생성과 관리에 대한 문제를 해결하기 위해 등장했고, 사용한 스레드를 종료하는 것이 아닌 재사용함으로써 스레드 생성에 대한 부담을 감소시킵니다.
