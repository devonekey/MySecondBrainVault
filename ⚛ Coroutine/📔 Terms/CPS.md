---
aliases:
  - Continuation-Passing Style
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - OpenAI
tags:
  - Coroutine
  - 코루틴
  - Terms
  - 주요_개념
learned:
---
##### ℹ️ Description
---
- 함수가 결과를 직접 반환하지 않고, 결과를 처리할 다른 함수(Continuation)를 인자로 받아 호출하는 방식의 프로그래밍 스타일

##### ➕ Extra
---
- `suspend` 함수는 컴파일 시 CPS로 변환돼, [일시 중단](일시%20중단.md) 후 [재개](재개.md)가 가능해짐
