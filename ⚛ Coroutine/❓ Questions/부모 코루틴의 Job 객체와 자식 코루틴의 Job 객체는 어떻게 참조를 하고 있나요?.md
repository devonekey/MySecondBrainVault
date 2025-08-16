---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[왜 실행 환경을 상속할 때 Job 객체를 상속하지 않을까요?]]"
next page: "[[루트 코루틴에 대해 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[부모 코루틴](부모%20코루틴.md)은 `children` 프로퍼티에 [자식 코루틴](자식%20코루틴.md)을 `Sequence<Job>`타입으로 가지고 자식 코루틴은 `parent`프로퍼티에 부모 코루틴을 `Job?`으로 가져, 양방향으로 참조를 하여 구조화를 이루고 있습니다.
