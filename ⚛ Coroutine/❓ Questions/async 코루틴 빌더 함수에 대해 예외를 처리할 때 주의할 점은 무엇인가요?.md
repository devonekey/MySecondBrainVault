---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[async 코루틴 빌더 함수는 언제 예외가 발생해 노출되나요?]]"
next page: "[[CancellationException은 왜 부모 코루틴으로 예외가 전파되지 않나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[await](Deferred.await.md) 함수 호출부 뿐만 아니라, [async](CoroutineScope.async.md) [코루틴 빌더](코루틴%20빌더.md) 함수에서도 [부모 코루틴](부모%20코루틴.md)으로 [예외가 전파](예외%20전파.md)될 수 있어서 이 부분 모두 [예외 처리](예외%20처리.md)를 해야 하는 점입니다.
결과를 [Deferred](Deferred.md)로 받지 않았다면, 부모 코루틴으로 예외가 전파됩니다.
