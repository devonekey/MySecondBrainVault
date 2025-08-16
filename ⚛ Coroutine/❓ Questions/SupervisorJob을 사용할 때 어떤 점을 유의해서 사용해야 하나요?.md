---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[SupervisorJob을 CoroutineScope와 같이 사용하면 구조는 어떻게 변하나요?]]"
next page: "[[supervisorScope 함수는 내부적으로 어떻게 구현되고, 어떤 의미를 가지고 있나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned: 
---
##### 💬 Answer
---
[SupervisorJob](SupervisorJob.md) 객체를 [launch](CoroutineScope.launch.md) 함수의 `parent` 매개변수에 추가할 때, `launch`로 생성되는 [예외 전파 제한](예외%20전파%20제한.md) 대상 [Job](Job.md)보다 앞서서 추가됩니다.
이 때, 전파 제한 대상의 `Job`에 [자식 코루틴](자식%20코루틴.md)을 생성할 경우, `SupervisorJob`의 상위 [코루틴](코루틴.md)으로 [예외가 전파](예외%20전파.md)되는 것은 막을 수 있겠으나, 자식 코루틴에서 시작된 예외 전파가 다른 자식 코루틴을 취소합니다.

직접 [Job](Job.md) 객체를 생성하는 것이므로, [complete](CompletableJob.complete.md) 함수를 호출하여 완료 처리해야 합니다.
