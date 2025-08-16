---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
prev page: "[[awaitAll의 동작 방식을 설명해주세요.]]"
next page: "[[컨텍스트 스위칭(Context Switching)이란 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[async](CoroutineScope.async.md)-[await](Deferred.await.md)를 순차적으로 실행할 때, [withContext](withContext.md) 함수를 사용하여 대체할 수 있습니다.
`withContext` 함수는 `context` 인자로 받은 [CoroutineContext](CoroutineContext.md) 객체를 실행하여 `block` 람다식을 실행하며, 모두 실행하면 다시 기존의 [CoroutineContext](CoroutineContext.md) 객체를 사용해 [코루틴](코루틴.md)을 [재개](재개.md)시킵니다.

`async`-`await`는 새로운 코루틴을 생성하지만, `withContext` 함수는 실행 중이던 코루틴을 유지한 채로 코루틴의 [실행 환경](실행%20환경.md)만 변경해 작업을 처리합니다.
