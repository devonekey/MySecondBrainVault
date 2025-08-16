---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/8장 - 예외 처리]]"
answered by:
  - Book
prev page: "[[try-catch문으로 예외를 처리할 때 어떤 점을 주의해야 하나요?]]"
next page: "[[async 코루틴 빌더 함수에 대해 예외를 처리할 때 주의할 점은 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[async](CoroutineScope.async.md) [코루틴 빌더](코루틴%20빌더.md) 함수는 다른 코루틴 빌더 함수와 달리 결괏값을 [Deferred](Deferred.md) 객체로 감싸고 [await](Deferred.await.md) 함수 호출 시점에 결괏값을 노출합니다. 그래서 [코루틴](코루틴.md) 실행 도중 [예외](예외.md)가 발생해 결과값을 갖지 못하면, `await` 함수가 호출될 때 예외가 노출됩니다.
