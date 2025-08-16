---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/6장 - CoroutineContext]]"
answered by:
  - Book
prev page: "[[withContext 함수 실행으로 CoroutineDispatcher에는 어떤 변화가 있을까요?]]"
next page: "[[CoroutineContext란 무엇인가요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
두 함수에는 아래 매개변수들이 선언됩니다.
- `context`: [CoroutineContext](CoroutineContext.md)
- `start`: [CoroutineStart](CoroutineStart.md)
- `block`
	- [launch](CoroutineScope.launch.md) 함수에는 `Unit`을 반환하는 람다식
	- [async](CoroutineScope.async.md) 함수에는 제네릭 타입 `T`를 반환하는 람다식
