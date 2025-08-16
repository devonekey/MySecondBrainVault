---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
prev page: "[[부모 코루틴의 CoroutineDispatcher는 자식 코루틴에게 어떻게 전달되나요?]]"
next page: "[[CoroutineDispatcher를 직접 생성했을 때의 문제를 해결하고자, 코루틴 라이브러리에서는 미리 정의된 디스패처를 제공하는 데, 어떤 디스패처들이 있는지 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
사용자가 직접 [스레드](스레드.md) 개수를 지정하여 [CoroutineDispatcher](CoroutineDispatcher.md) 객체를 생성하는 방법은 스레드가 부족하거나 과하게 생성돼 비효율적으로 동작할 가능성이 있기 때문입니다. 

##### ➕ Extra
---
코루틴 라이브러리는 개발자가 직접 생성했을 때의 문제를 해결하고자 미리 정의된 `CoroutineDispatcher`를 제공합니다.
