---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/7장 - 구조화된 동시성]]"
answered by:
  - Book
prev page: "[[루트 Job에 대해 설명해주세요.]]"
next page: "[[생성한 Job에 부모를 명시적으로 설정하는 방법을 설명해주세요.]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[CoroutineScope](CoroutineScope.md) 함수를 통해 `CoroutineScope` 객체가 생성되면, 새로운 [루트 Job](루트%20Job.md)이 생성돼 구조화를 깰 수 있습니다. 
또는 [코루틴 빌더](코루틴%20빌더.md) 함수를 통해 [코루틴](코루틴.md)을 생성할 때, `context` 매개변수에 명시적으로 루트 `Job` 객체를 추가하는 방법으로도 벗어날 수 있습니다.
