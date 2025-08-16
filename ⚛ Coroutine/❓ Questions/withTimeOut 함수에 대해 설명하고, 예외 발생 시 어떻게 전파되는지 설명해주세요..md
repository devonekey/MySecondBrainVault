---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[CancellationException은 왜 부모 코루틴으로 예외가 전파되지 않나요?]]"
next page: "[[일시 중단 함수란 무엇이고 어떤 경우에 사용하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[withTimeout](withTimeout.md) 함수는 시간 제한을 두고 작업을 실행할 수 있도록 만드는 함수입니다.
주어진 시간(`timemillis`)과 작업(`block`)을 매개변수로 갖고 있습니다.
주어진 시간 내에 작업을 처리하지 못하면 [CancellationException](CancellationException.md)의 서브 클래스인 [TimeoutCancellationException](TimeoutCancellationException.md) [예외](예외.md)가 발생하는 데, 해당 함수를 호출한 [코루틴](코루틴.md)만 취소시키고 [부모 코루틴](부모%20코루틴.md)으로는 [예외가 전파](예외%20전파.md)되지 않습니다.
