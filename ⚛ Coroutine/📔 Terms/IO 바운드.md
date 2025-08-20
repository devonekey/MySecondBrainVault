---
aliases:
  - I/O-bound
importance: Medium
originated from:
  - "[[📘 코틀린 동시성 프로그래밍/1장 - Hello, Concurrent World!]]"
answered by:
  - Book
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
- 프로그램 또는 작업의 성능이 입출력(I/O) 장치의 속도에 의해 제한되는 상태

##### 👀 Example
---
- 파일 시스템에서의 파일 읽기/쓰기, 데이터베이스 쿼리, 네트워크 요청 등

##### 💪 How to enhance?
---
- 비동기 I/O나 [멀티 스레드 프로그래밍](멀티%20스레드%20프로그래밍.md)을 사용해 I/O 작업이 완료될 때까지 기다리는 대신 다른 작업을 처리
- 더 빠른 I/O 장치 사용
