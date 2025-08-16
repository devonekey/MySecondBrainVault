---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[자식 코루틴에서 예외가 발생했을 때 자식 코루틴에 설정한 CoroutineExceptionHandler는 왜 동작하지 않을까요?]]"
next page: "[[CoroutineExceptionHandler를 사용할 때 어떤 점을 주의해야 하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineExceptionHandler](CoroutineExceptionHandler.md)를 사용할 때는 [코루틴](코루틴.md)이 완료된 상태이기 때문에 복구될 수 없습니다. 그래서 [예외](예외.md)를 로깅하거나 오류 메시지를 표시하기 위해 사용합니다.
