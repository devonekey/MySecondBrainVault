---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/4장 - 코루틴 빌더와 Job]]"
answered by:
  - Book
prev page: "[[코루틴의 각 상태에 대해 설명해주세요.]]"
next page: "[[코루틴으로부터 결괏값을 수신하려면 어떤 코루틴 빌더 함수를 사용해야 하며, 어떻게 결괏값을 수신하나요?]]"
tags:
  - Coroutine
  - 코루틴
  - Questions
  - 예상_질문
learned:
---
##### 💬 Answer
---
[Job](Job.md) 객체는 [코루틴](코루틴.md)의 상태 변수들을 외부로 공개합니다.
코루틴의 상태들은 간접적으로만 파악할 수 있습니다.

- [isActive](Job.isActive.md): 코루틴이 활성화됐는지 여부를 나타내는 변수입니다.
- [isCancelled](Job.isCancelled.md): 코루틴이 취소 요청됐는지 여부를 나타내는 변수입니다.
- [isCompleted](Job.isCompleted.md): 코루틴이 실행 완료됐는지 여부를 나타내는 변수입니다.
