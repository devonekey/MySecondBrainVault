---
importance: High
originated from:
  - "[[📘 코틀린 코루틴의 정석/3장 - CoroutineDispatcher]]"
answered by:
  - Book
parent pages:
  - "[[CoroutineDispatcher]]"
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
  - val
learned:
---
##### 🖋️ Signature
---
```Kotlin
public val IO: CoroutineDispatcher
```

##### ℹ️ Description
---
- 네트워크 요청이나 파일 입출력 등의 입출력 작업을 위한 [CoroutineDispatcher](CoroutineDispatcher.md) ^desc-1

##### ➕ Extra
---
- 최대로 사용할 수 있는 [스레드](스레드.md) 수는 [JVM](자바%20가상%20머신.md)에서 사용 가능한 프로세서의 수와 64 중 큰 값으로 설정
- [공유 스레드 풀](공유%20스레드%20풀.md)의 스레드를 사용할 수 있도록 구현
