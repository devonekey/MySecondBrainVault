---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/5장 - async와 Deferred]]"
answered by:
  - Book
prev page: "[[코루틴으로부터 결괏값을 수신하려면 어떤 코루틴 빌더 함수를 사용해야 하며, 어떻게 결괏값을 수신하나요?]]"
next page: "[[여러 Deferred로부터 결괏값을 수신하는 방법을 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[Deferred](Deferred.md)는 특수한 형태의 [Job](Job.md)으로, 내부 코드에서는 `Job`을 상속받아 [코루틴](코루틴.md) 결괏값을 반환할 수 있도록 몇가지 기능이 추가됐습니다.

##### ➕ Extra
---
`Job`을 상속받기에 `Job`에 있는 모든 함수와 프로퍼티도 사용할 수 있습니다.
