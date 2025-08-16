---
importance: Low
originated from:
  - "[[📘 코틀린 코루틴의 정석/1장 - 스레드 기반 작업의 한계와 코루틴의 등장]]"
answered by:
  - Book
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Java
  - API
  - interface
learned:
---
##### 🖋️ Signature
---
```Java
public interface java.util.concurrent.ExecutorService extends java.util.concurrent.Executor
```

##### ℹ️ Description
---
- [스레드 풀](스레드%20풀.md)을 관리하는 객체


##### 🪄 How to create
---
```Kotlin
val executorService = Excutors.newFixedThreadPool(2)
```
