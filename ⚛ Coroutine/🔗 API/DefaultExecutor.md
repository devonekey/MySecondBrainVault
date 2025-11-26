---
importance: Medium
originated from:
  - "[[📘 코틀린 코루틴의 정석/11장 - 코루틴 심화]]"
answered by:
  - Book
  - GPT
parent pages: 
tags:
  - Coroutine
  - 코루틴
  - Kotlin
  - API
learned:
---
##### 🖋️ Signature
---
```Kotlin
internal object DefaultExecutor : EventLoopImplBase(), Runnable
```

##### ℹ️ Description
---
- [delay](delay.md) 함수를 실행하는 [스레드](스레드.md)

##### ➕ Extra
---
- `delay` 함수가 [일시 중단](일시%20중단.md)을 종료하고 [코루틴](코루틴.md)을 재개할 때 사용하는 스레드
- 코루틴 내부에서 사용되는 싱글톤 스케줄러(지연 실행, `delay`, [withTimeout](withTimeout.md) 등을 스케줄링할 때 사용)
