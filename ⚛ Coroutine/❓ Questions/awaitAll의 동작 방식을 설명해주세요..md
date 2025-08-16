---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
prev page: "[[여러 Deferred로부터 결괏값을 수신하는 방법을 설명해주세요.]]"
next page: "[[async-await를 대체할 수 있는 것과 그것이 async-await와는 어떤 차이가 있는지 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[awaitAll](awaitAll.md) 함수는 가변 인자로 [Deferred](Deferred.md) 객체를 받아 모든
`Deferred` [코루틴](코루틴.md)으로부터 결괏값을 받을 때까지, 해당 함수를 호출한 코루틴을 일시 중단합니다. 
모든 `Deferred` 코루틴으로부터 결괏값을 받으면 해당 함수를 호출한 코루틴을 [재개](재개.md)합니다. 

##### ➕ Extra
---
참고로 코루틴 라이브러리는 `Collection` 인터페이스에
`awaitAll`을 확장 함수로 제공합니다.
